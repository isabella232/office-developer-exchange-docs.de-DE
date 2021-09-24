---
title: Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Erfahren Sie, wie Sie Berechtigungsstufen für einen Ordner mithilfe der verwalteten EWS-API oder EWS in Exchange festlegen.
ms.openlocfilehash: 15288af0448a48c176529912604f628ae9bc2f19
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513087"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a>Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange

Erfahren Sie, wie Sie Berechtigungsstufen für einen Ordner mithilfe der verwalteten EWS-API oder EWS in Exchange festlegen.
  
Berechtigungen auf Ordnerebene ermöglichen Benutzern den Zugriff auf einen oder mehrere Ordner im Postfach eines anderen Benutzers. Ordnerberechtigungen ähneln dem Stellvertretungszugriff, unterscheiden sich jedoch auf folgende Weise: 
  
- Ordnerberechtigungen ermöglichen einem Benutzer nicht das "Senden im Auftrag von" oder "Senden als" eines anderen Benutzers. Sie ermöglichen nur den Zugriff auf Ordner. Benutzer können Elemente in diesen Ordnern erstellen, aber sie können sie nicht senden.
    
- Sie können Ordnerberechtigungen für jeden Ordner im Postfach festlegen, aber Sie können nur einen Delegaten zu den Ordnern "Kalender", "Kontakte", "Posteingang", "Journal", "Notizen" und "Aufgaben" hinzufügen.
    
- Sie können eine Reihe von [Berechtigungen für einen bestimmten Ordner](#bk_folderperms)festlegen. Wenn Sie einen Delegaten hinzufügen, können Sie eine von nur [fünf Berechtigungsstufen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)zuweisen.
    
- Sie können Ordnerberechtigungen für anonyme und Standardbenutzer festlegen. Sie können nur Stellvertretungszugriff auf ein E-Mail-aktiviertes Konto gewähren.
    
Wenn Sie mit Zugriffssteuerungseinträgen (Access Control Entries, ACEs) und Discretionary Access Control Lists (DACLs) vertraut sind, wissen Sie, dass ein Benutzer nur einen Satz von Berechtigungen für jeden Ordner haben kann. Wenn Sie versuchen, einen Satz von Berechtigungen für einen Benutzer hinzuzufügen, und dieser bereits über eine Reihe von Berechtigungen verfügt, wird ein Fehler angezeigt. Wenn Sie Berechtigungen zu einem Ordner hinzufügen, entfernen oder aktualisieren, erhalten Sie die aktuelle DACL, fügen ACEs hinzu oder entfernen sie und senden dann die aktualisierte DACL. Sie können nicht mehrere ACEs für denselben Benutzer hinzufügen. Wenn Sie Berechtigungen mithilfe der verwalteten EWS-API aktualisieren, müssen Sie den aktuellen Ace des Benutzers entfernen und dann der Sammlung den neuen Ace hinzufügen. Wenn Sie EWS verwenden, ersetzen Sie einfach den vorherigen AcEs-Satz durch die neuen.
  
Wenn Sie mehrere Berechtigungsänderungen an einem einzelnen Ordner vornehmen, können Sie Hinzufügungen, Entfernungen oder Aktualisierungen stapeln . Beachten Sie lediglich, dass Sie Benutzeraktualisierungen nicht in mehreren Ordnern stapeln können. Ein Aufruf ist erforderlich, um die Berechtigungen für einen einzelnen Ordner zu erhalten, und ein zweiter Aufruf ist erforderlich, um die Berechtigungen für diesen Ordner zu aktualisieren. Wenn Sie Benutzerberechtigungen hinzufügen, entfernen oder aktualisieren, verwenden Sie die gleichen beiden Methodenaufrufe oder -vorgänge für jede Aufgabe.
  
**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Vorgänge zum Festlegen von Ordnerberechtigungen**

|Aktion|Verwenden Sie diese verwaltete EWS-API-Methode...|Verwenden Sie diesen EWS-Vorgang...|
|:-----|:-----|:-----|
|Aktivieren, Entfernen oder Aktualisieren von Ordnerberechtigungen  <br/> |[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> |[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Erstellen eines Ordners und Definieren von Ordnerberechtigungen  <br/> |[Folder.Save](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](https://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a>Ordnerberechtigungen
<a name="bk_folderperms"> </a>

Sie haben einige Optionen, wenn es darum geht, Ordnerberechtigungen für einen bestimmten Ordner festzulegen. Sie können eine Berechtigungsstufe für einen Ordner für jeden Benutzer festlegen, wodurch der DACL eine Reihe vordefinierter einzelner Berechtigungen hinzugefügt wird, oder Sie können einzelne Berechtigungen für einen Ordner festlegen , aber Sie können diese nicht kombinieren und abgleichen.
  
Die folgenden einzelnen Berechtigungen sind verfügbar:
  
- Kann erstellen
- Kann Unterordner erstellen    
- Ist Ordnerbesitzer    
- Ist der Ordner sichtbar?    
- Ist Ordnerkontakt    
- Elemente bearbeiten    
- Löschen von Elementen    
- Elemente lesen
    
Darüber hinaus sind die folgenden Berechtigungsstufen verfügbar, die eine Teilmenge der einzelnen Berechtigungen und Werte definieren, wie in Tabelle 2 dargestellt:
  
- Keines    
- Besitzer    
- PublishingEditor    
- Editor    
- PublishingAuthor    
- Ursprung    
- NoneditingAuthor    
- Reviewer    
- Contributor   
- Benutzerdefiniert : Dieser Wert kann von der Anwendung nicht festgelegt werden. Der Server legt diesen Wert fest, wenn die Anwendung eine benutzerdefinierte Sammlung einzelner Berechtigungen enthält.    
- FreeBusyTimeOnly : Dies kann nur für Kalenderordner festgelegt werden.   
- FreeBusyTimeAndSubjectAndLocation : Dies kann nur für Kalenderordner festgelegt werden.
    
Die folgende Tabelle zeigt, welche einzelnen Berechtigungen standardmäßig basierend auf der Berechtigungsstufe angewendet werden.
  
**Tabelle 2. Einzelne Berechtigungen nach Berechtigungsstufe**

|Berechtigungsstufe|Kann Elemente erstellen|Kann Unterordner erstellen|Ist Ordnerbesitzer|Ist der Ordner sichtbar?|Ist Ordnerkontakt|Elemente bearbeiten|Löschen von Elementen|Kann Elemente lesen|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Keines  <br/> |Nicht richtig  <br/> |Nicht richtig  <br/> |Nicht richtig  <br/> |Nicht richtig  <br/> |Nicht richtig  <br/> |Keine  <br/> |Keine  <br/> |Keine  <br/> |
|Besitzer  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |Alle  <br/> |Alle  <br/> |FullDetails  <br/> |
|PublishingEditor  <br/> |True  <br/> |True  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Alle  <br/> |Alle  <br/> |FullDetails  <br/> |
|Editor  <br/> |Richtig  <br/> |Nicht richtig  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Alle  <br/> |Alle  <br/> |FullDetails  <br/> |
|PublishingAuthor  <br/> |True  <br/> |True  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Im besitz  <br/> |Im besitz  <br/> |FullDetails  <br/> |
|Ursprung  <br/> |Richtig  <br/> |Nicht richtig  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Im besitz  <br/> |Im besitz  <br/> |FullDetails  <br/> |
|NoneditingAuthor  <br/> |Richtig  <br/> |Nicht richtig  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Keines  <br/> |Im besitz  <br/> |FullDetails  <br/> |
|Reviewer  <br/> |Nicht richtig  <br/> |Nicht richtig  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Keine  <br/> |Keine  <br/> |FullDetails  <br/> |
|Contributor  <br/> |Richtig  <br/> |Nicht richtig  <br/> |False  <br/> |Wahr  <br/> |Nicht richtig  <br/> |Keine  <br/> |Keine  <br/> |Keine  <br/> |
   
Wenn Sie in der Berechtigungsanforderung auf Ordnerebene eine nicht benutzerdefinierte Berechtigungsstufe angeben, müssen Sie die einzelnen Berechtigungseinstellungen nicht angeben. Wenn Sie beim Festlegen einer Berechtigungsstufe eine einzelne Berechtigung angeben, wird in der Antwort ein **ErrorInvalidPermissionSettings-Fehler** zurückgegeben. 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a>Hinzufügen von Ordnerberechtigungen mithilfe der verwalteten EWS-API
<a name="bk_enableewsma"> </a>

Das folgende Codebeispiel zeigt, wie sie die verwaltete EWS-API verwenden kann: 
  
- Erstellen Sie ein neues [FolderPermission-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) für den neuen Benutzer. 
    
- Rufen Sie die aktuellen Berechtigungen für einen Ordner mithilfe der [Bind-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) ab. 
    
- Fügen Sie die neuen **FolderPermissions** zur [Folder.Permissions-Eigenschaft](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) hinzu. 
    
- Rufen Sie die [Update-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) auf, um die neuen Berechtigungen auf dem Server zu speichern. 
    
In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```cs
static void EnableFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.Permissions);
    // Specify the SMTP address of the new user and the folder permissions level.
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
    
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, WellKnownFolderName.SentItems, propSet);
 
    // Add the permissions for the new user to the Sent Items DACL.
    sentItemsFolder.Permissions.Add(fldperm);
    // This call results in a UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

Die folgende Codezeile gibt die Berechtigungsstufe an.
  
```cs
    FolderPermission fldperm = new FolderPermission("sadie@contoso.com", FolderPermissionLevel.Editor);
```

Wenn Sie die benutzerdefinierte Berechtigungsstufe verwenden möchten, verwenden Sie stattdessen diesen Code.
  
```cs
FolderPermission fldperm = new FolderPermission();
fldperm.UserId = "sadie@Contoso1000.onmicrosoft.com";
fldperm.CanCreateItems = true;
fldperm.CanCreateSubFolders = true;
…
```

Sie können eine oder alle schreibbaren [FolderPermission-Eigenschaften](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) festlegen, wenn Sie ein **FolderPermission-Objekt** mit einer benutzerdefinierten Berechtigungsstufe erstellen. Beachten Sie jedoch, dass [folderPermissionLevel](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) von der Anwendung nie explizit auf **"Benutzerdefiniert"** festgelegt ist. **"FolderPermissionLevel"** wird nur dann auf "Benutzerdefiniert" festgelegt, wenn Sie ein **FolderPermission-Objekt** erstellen und einzelne Berechtigungen festlegen. 
  
## <a name="adding-folder-permissions-by-using-ews"></a>Hinzufügen von Ordnerberechtigungen mithilfe von EWS
<a name="bk_enableews"> </a>

Die folgenden EWS-Codebeispiele zeigen, wie Sie Berechtigungen zu einem bestimmten Ordner hinzufügen, indem Sie die aktuellen Berechtigungen abrufen und dann eine Liste der neuen Berechtigungen übermitteln.
  
Der erste Schritt besteht darin, eine [GetFolder-Anforderung](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) zu senden, wobei der [DistinguishedFolderId-Wert](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) den Ordner angibt, in dem Berechtigungen hinzugefügt werden sollen (der Ordner "Gesendete Elemente" in diesem Beispiel) und der [FieldURI-Wert](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) den Ordner "PermissionSet" enthält. Diese Anforderung ruft die Berechtigungseinstellungen für den angegebenen Ordner ab. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Bind-Methode** aufrufen, um [Ordnerberechtigungen hinzuzufügen.](#bk_enableewsma)
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
    <soap:Header>
      <t:RequestServerVersion Version="Exchange2007_SP1" />
    </soap:Header>
    <soap:Body>
      <m:GetFolder>
        <m:FolderShape>
          <t:BaseShape>IdOnly</t:BaseShape>
          <t:AdditionalProperties>
            <t:FieldURI FieldURI="folder:PermissionSet" />
          </t:AdditionalProperties>
        </m:FolderShape>
        <m:FolderIds>
          <t:DistinguishedFolderId Id="sentitems" />
        </m:FolderIds>
      </m:GetFolder>
    </soap:Body>
  </soap:Envelope>
```

Der Server antwortet auf die **GetFolder-Anforderung** mit einer [GetFolderResponse-Nachricht,](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die [FolderId-](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) und [ParentFolderId-Werte](https://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="CgAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

Verwenden Sie als Nächstes den **UpdateFolder-Vorgang,** um das aktualisierte [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)zu senden, das die [Berechtigung](https://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) für den neuen Benutzer enthält. Beachten Sie, dass durch das Einschließen des [SetFolderField-Elements](https://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) für den entsprechenden Ordner in den [UpdateFolder-Vorgang](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) alle Berechtigungseinstellungen für den Ordner überschrieben werden. Ebenso werden, einschließlich der [DeleteFolderField-Option](https://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) des **UpdateFolder-Vorgangs,** auch alle Berechtigungseinstellungen für den Ordner gelöscht. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Update-Methode** aufrufen, um [Ordnerberechtigungen hinzuzufügen.](#bk_enableewsma)
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="CgAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd1" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
                      </t:UserId>
                      <t:PermissionLevel>Editor</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

Die folgende Codezeile gibt die Berechtigungsstufe an.
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress>sadie@contoso.com</t:PrimarySmtpAddress>
    </t:UserId>
    <t:PermissionLevel>Editor</t:PermissionLevel>
</t:Permission>
```

Wenn Sie die benutzerdefinierte Berechtigungsstufe verwenden möchten, verwenden Sie stattdessen diesen Code.
  
```xml
<t:Permission>
    <t:UserId>
        <t:PrimarySmtpAddress> sadie@contoso.com </t:PrimarySmtpAddress>
    </t:UserId>
    <t:CanCreateItems>true</t:CanCreateItems>
    <t:CanCreateSubFolders>true</t:CanCreateSubFolders>
    <t:IsFolderOwner>false</t:IsFolderOwner>
    <t:IsFolderVisible>false</t:IsFolderVisible>
    <t:IsFolderContact>false</t:IsFolderContact>
    <t:EditItems>None</t:EditItems>
    <t:DeleteItems>None</t:DeleteItems>
    <t:ReadItems>None</t:ReadItems>
    <t:PermissionLevel>Custom</t:PermissionLevel>
</t:Permission>
```

Der Server antwortet auf die **UpdateFolder-Anforderung** mit einer [UpdateFolderResponse-Nachricht,](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass der Ordner erfolgreich aktualisiert wurde.
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a>Entfernen von Ordnerberechtigungen mithilfe der verwalteten EWS-API
<a name="bk_removeewsma"> </a>

Das folgende Codebeispiel zeigt, wie Sie mithilfe der verwalteten EWS-API alle Benutzerberechtigungen für einen bestimmten Ordner mit Ausnahme der Standard- und anonymen Berechtigungen entfernen:
  
1. Abrufen der aktuellen Berechtigungen für einen Ordner mithilfe der **Bind-Methode.** 
    
2. Durchlaufen der **Permissions-Auflistung** und Entfernen von Berechtigungen für einzelne Benutzer. 
    
3. Aufrufen der **Update-Methode** zum Speichern der Änderungen. 
    
In diesem Beispiel werden alle Benutzerberechtigungen für einen Ordner entfernt. Wenn Sie dieses Beispiel so ändern möchten, dass berechtigungen nur für einen bestimmten Benutzer entfernt werden, ändern Sie die folgende Codezeile, um entweder den Anzeigenamen oder die SMTP-Adresse des Benutzers zu identifizieren.
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
```cs
static void RemoveFolderPermissions(ExchangeService service)
{
    // Create a property set to use for folder binding.
    PropertySet propSet = new PropertySet(BasePropertySet.FirstClassProperties, FolderSchema.Permissions);
    // Bind to the folder and get the current permissions. 
    // This call results in a GetFolder call to EWS.
    Folder sentItemsFolder = Folder.Bind(service, new FolderId(WellKnownFolderName.SentItems, "primary@contoso.com"), propSet);
    // Iterate through the collection of permissions and remove permissions for any 
    // user with a display name or SMTP address. This leaves the anonymous and 
    // default user permissions unchanged. 
    if (sentItemsFolder.Permissions.Count != 0)
    {
        for (int t = 0; t < sentItemsFolder.Permissions.Count; t++)
        {
            // Find any permissions associated with the specified user and remove them from the DACL
            if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
            {
                sentItemsFolder.Permissions.Remove(sentItemsFolder.Permissions[t]);
            }
        }
    }
    // This call results in an UpdateFolder call to EWS.
    sentItemsFolder.Update();
}
```

## <a name="removing-folder-permissions-by-using-ews"></a>Entfernen von Ordnerberechtigungen mithilfe von EWS
<a name="bk_removeews"> </a>

Die folgenden EWS-Codebeispiele zeigen, wie Sie alle Benutzerberechtigungen für einen bestimmten Ordner entfernen, mit Ausnahme der standard- und anonymen Berechtigungen.
  
Senden Sie zunächst eine [GetFolder-Anforderung,](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) wobei der [DistinguishedFolderId-Wert](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) den Ordner angibt, in dem Berechtigungen entfernt werden sollen (der Ordner "Gesendete Elemente" in diesem Beispiel) und der [FieldURI-Wert](https://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) den Ordner "PermissionSet" enthält. Diese Anforderung ruft das [PermissionSet](https://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) für den angegebenen Ordner ab. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Bind-Methode** aufrufen, um [Ordnerberechtigungen](#bk_removeewsma)zu entfernen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:PermissionSet" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **GetFolder-Anforderung** mit einer [GetFolderResponse-Nachricht,](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die Werte der **FolderId-** und **ParentFolderId-Elemente** wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Folders>
            <t:Folder>
              <t:FolderId Id="EAAAAA=="
                          ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
              <t:ParentFolderId Id="CQAAAA=="
                                ChangeKey="AQAAAA==" />
              <t:FolderClass>IPF.Note</t:FolderClass>
              <t:DisplayName>Drafts</t:DisplayName>
              <t:TotalCount>0</t:TotalCount>
              <t:ChildFolderCount>0</t:ChildFolderCount>
              <t:EffectiveRights>
                <t:CreateAssociated>true</t:CreateAssociated>
                <t:CreateContents>true</t:CreateContents>
                <t:CreateHierarchy>true</t:CreateHierarchy>
                <t:Delete>true</t:Delete>
                <t:Modify>true</t:Modify>
                <t:Read>true</t:Read>
                <t:ViewPrivateItems>true</t:ViewPrivateItems>
              </t:EffectiveRights>
              <t:PermissionSet>
                <t:Permissions>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Default</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                    </t:UserId>
                    <t:CanCreateItems>false</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>false</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>None</t:EditItems>
                    <t:DeleteItems>None</t:DeleteItems>
                    <t:ReadItems>None</t:ReadItems>
                    <t:PermissionLevel>None</t:PermissionLevel>
                  </t:Permission>
                  <t:Permission>
                    <t:UserId>
                      <t:SID>S-1-5-21-1337771579-694202782-848329751-1535223</t:SID>
                      <t:PrimarySmtpAddress>sadie@Contoso.com</t:PrimarySmtpAddress>
                      <t:DisplayName>Sadie Daniels</t:DisplayName>
                    </t:UserId>
                    <t:CanCreateItems>true</t:CanCreateItems>
                    <t:CanCreateSubFolders>false</t:CanCreateSubFolders>
                    <t:IsFolderOwner>false</t:IsFolderOwner>
                    <t:IsFolderVisible>true</t:IsFolderVisible>
                    <t:IsFolderContact>false</t:IsFolderContact>
                    <t:EditItems>All</t:EditItems>
                    <t:DeleteItems>All</t:DeleteItems>
                    <t:ReadItems>FullDetails</t:ReadItems>
                    <t:PermissionLevel>Editor</t:PermissionLevel>
                  </t:Permission>
                </t:Permissions>
              </t:PermissionSet>
              <t:UnreadCount>0</t:UnreadCount>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

Verwenden Sie als Nächstes den **UpdateFolder-Vorgang,** um das aktualisierte **PermissionSet** zu senden, das nicht die **Berechtigung** für den entfernten Benutzer enthält. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Update-Methode** aufrufen, um [Ordnerberechtigungen](#bk_removeewsma)zu entfernen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:UpdateFolder>
      <m:FolderChanges>
        <t:FolderChange>
          <t:FolderId Id="EAAAAA=="
                      ChangeKey="AQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiRd5" />
          <t:Updates>
            <t:SetFolderField>
              <t:FieldURI FieldURI="folder:PermissionSet" />
              <t:Folder>
                <t:PermissionSet>
                  <t:Permissions>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Default</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                    <t:Permission>
                      <t:UserId>
                        <t:DistinguishedUser>Anonymous</t:DistinguishedUser>
                      </t:UserId>
                      <t:PermissionLevel>None</t:PermissionLevel>
                    </t:Permission>
                  </t:Permissions>
                </t:PermissionSet>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **UpdateFolder-Anforderung** mit einer **UpdateFolderResponse-Nachricht,** die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass das Update erfolgreich war.
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a>Aktualisieren von Ordnerberechtigungen mithilfe der verwalteten EWS-API
<a name="bk_updateewsma"> </a>

Sie können ordnerberechtigungen für einen bestimmten Ordner auch mithilfe der verwalteten EWS-API aktualisieren. So aktualisieren Sie die Berechtigungen: 
  
1. [Entfernen Sie die Ordnerberechtigungen](#bk_removeewsma) für die veralteten Berechtigungen, aber rufen Sie die **Update-Methode** (noch) nicht auf. 
    
2. [Fügen Sie Ordnerberechtigungen für die neuen oder geänderten Benutzer](#bk_enableewsma)hinzu.
    
3. Rufen Sie die **Update-Methode** auf, um die Änderungen zu speichern. 
    
Wenn Sie versuchen, zwei Berechtigungssätze für denselben Benutzer hinzuzufügen, erhalten Sie einen **ServiceResponseException-Fehler** mit der folgenden Beschreibung: "Der angegebene Berechtigungssatz enthält doppelte UserIds". Entfernen Sie in diesem Fall die aktuellen Berechtigungen aus der **Permission -Auflistung,** und fügen Sie dann die neuen Berechtigungen zur **Permission -Auflistung** hinzu. 
  
## <a name="updating-folder-permissions-by-using-ews"></a>Aktualisieren von Ordnerberechtigungen mithilfe von EWS
<a name="bk_updateews"> </a>

Sie können Ordnerberechtigungen für bestimmte Ordner auch mithilfe von EWS aktualisieren, indem Sie den Entfernungs- und Additionsprozess kombinieren. So aktualisieren Sie die Berechtigungen: 
  
1. Rufen Sie die aktuellen Berechtigungen des Ordners mithilfe des **GetFolder-Vorgangs** ab. 
    
2. Senden Sie eine aktualisierte Liste von Berechtigungen mithilfe des **UpdateFolder-Vorgangs.** 
    
Dies sind die gleichen beiden Vorgänge, die Sie zum [Aktivieren](#bk_enableews) oder Entfernen des [Zugriffs](#bk_removeews) mithilfe von EWS verwenden. Der einzige Unterschied besteht darin, dass beim Empfang der **GetFolder-Antwort** ein **Berechtigungssatz** für den Benutzer enthalten ist. Ersetzen Sie einfach das vorhandene **Permission-Element** durch das neue **Permission-Element,** und senden Sie dann den **UpdateFolder-Vorgang** mit dem neuen **Permission-Wert** oder den neuen Werten. 
  
Wenn Sie versuchen, zwei Berechtigungssätze für denselben Benutzer hinzuzufügen, erhalten Sie den **ResponseCode-Wert** **ErrorDuplicateUserIdsSpecified**. Entfernen Sie in diesem Fall den veralteten Berechtigungswert für den Benutzer aus der Anforderung, und wiederholen Sie dann die Anforderung.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie einem Benutzer die Berechtigung für einen bestimmten Ordner erteilt haben, kann der Benutzer als Stellvertreter auf den Ordner zugreifen. Weitere Informationen finden Sie unter:
  
- [Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Zugriff auf einen Kalender als Delegat mithilfe der EWS in Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Zugriff auf Kontakte als Delegat mithilfe der EWS in Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)   
- [Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    

