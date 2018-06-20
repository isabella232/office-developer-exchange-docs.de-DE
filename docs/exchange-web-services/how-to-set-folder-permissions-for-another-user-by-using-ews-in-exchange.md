---
title: Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7eb81676-a780-4c56-b4f2-c4ed2697107d
description: Erfahren Sie, wie Berechtigungsstufen für einen Ordner festlegen, indem verwenden die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 5bf570612d6349628e7f3abf858daa33daa13745
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757004"
---
# <a name="set-folder-permissions-for-another-user-by-using-ews-in-exchange"></a>Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange

Erfahren Sie, wie Berechtigungsstufen für einen Ordner festlegen, indem verwenden die EWS Managed API oder EWS in Exchange.
  
Berechtigungen auf Ordnerebene können Benutzer einen oder mehrere Ordner im Postfach eines anderen Benutzers zugreifen. Ordnerberechtigungen ähneln Zugriff delegieren, jedoch unterscheiden sich wie folgt: 
  
- Berechtigungen für Ordner aktivieren ein Benutzers zum "Senden im Auftrag von" und "Senden als" eines anderen Benutzers nicht. Sie ermöglichen nur Zugriff auf Ordner. Benutzer können Elemente in diesen Ordnern erstellen, aber er können nicht gesendet werden.
    
- Sie können Ordnerberechtigungen für alle Ordner im Postfach festlegen, aber Sie können nur eine Stellvertretung den Ordner Kalender, Kontakte, Posteingang, Journal, Notizen und Aufgaben hinzufügen.
    
- Sie können eine Reihe von [Berechtigungen für einen bestimmten Ordner](#bk_folderperms)festlegen. Wenn Sie eine Stellvertretung hinzugefügt haben, können Sie nur [fünf Berechtigungsstufen](delegate-access-and-ews-in-exchange.md#bk_delegateperms)zuweisen.
    
- Sie können legen Sie Berechtigungen für anonyme und Standard-Benutzer. Sie können nur Delegieren des Zugriffs auf ein e-Mail-aktiviertes Konto erteilen.
    
Wenn Sie mit Access Control Entries, (Zugriffssteuerungseinträge ACEs) und Discretionary Access Control Lists () vertraut sind, wissen Sie, dass ein Benutzer nur ein Satz von Berechtigungen für jeden Ordner ausführen kann. Wenn Sie versuchen, eine Reihe von Berechtigungen für einen Benutzer hinzuzufügen, und sie bereits eine Reihe von Berechtigungen besitzen, erhalten Sie einen Fehler. Wenn Sie hinzufügen, entfernen oder aktualisieren Sie die Berechtigungen für einen Ordner, Sie erhalten die aktuelle DACL, hinzufügen oder Entfernen von ACEs, und senden Sie die aktualisierte DACL. Sie können nicht mehrere ACEs für denselben Benutzer hinzufügen. Wenn Sie Berechtigungen mithilfe der EWS Managed API aktualisieren, müssen Sie aktuelle ACE des Benutzers zu entfernen, und fügen Sie ihrer neuen ACE der Auflistung. Wenn Sie Exchange-Webdienste verwenden, ersetzen Sie den vorherigen Satz von ACEs, die nur durch die neue.
  
Wenn Sie mehrere Berechtigung Änderungen in einem einzelnen Ordner durchführen, können Sie batch hinzugefügt, entfernt oder Updates – Beachten Sie, dass Sie benutzeraktualisierungen in mehreren Ordnern batch ist nicht möglich. Ein Anruf ist erforderlich, um die Berechtigungen für einen einzelnen Ordner erhalten möchten, und ein zweiter Aufruf ist erforderlich, um die Berechtigungen für diesen Ordner zu aktualisieren. Wenn Sie hinzufügen, entfernen oder von Benutzerberechtigungen aktualisieren, verwenden Sie die gleichen zwei-Methodenaufrufen oder Vorgänge für jeden Vorgang.
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge zum Festlegen von Berechtigungen für Ordner**

|Aktion|Verwenden Sie diese Methode EWS Managed API...|Verwenden Sie diese Operation EWS...|
|:-----|:-----|:-----|
|Aktivieren, entfernen oder Aktualisieren von Berechtigungen für Ordner  <br/> |[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> |[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Erstellen Sie einen Ordner, und definieren Sie Berechtigungen für Ordner  <br/> |[Folder.Save](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.save%28v=exchg.80%29.aspx) <br/> |[CreateFolder](http://msdn.microsoft.com/library/6f6c334c-b190-4e55-8f0a-38f2a018d1b3%28Office.15%29.aspx) <br/> |
   
## <a name="folder-permissions"></a>Berechtigungen für Ordner
<a name="bk_folderperms"> </a>

Sie haben eine Anzahl von Optionen, wenn es darum geht, Festlegen von Berechtigungen für einen bestimmten Ordner. Setzen Sie eine Berechtigungsstufe für einen Ordner, für jeden Benutzer, die eine Reihe von vordefinierten einzelne Berechtigungen der DACL hinzufügt, oder Sie können einzelne Berechtigungen für einen Ordner festlegen – jedoch nicht möglich, mischen und übereinstimmen.
  
Die folgenden einzelnen Berechtigungen sind verfügbar:
  
- Erstellen können
- Unterordner können erstellen werden.    
- Ist der Besitzer des Ordners    
- Ordner ist sichtbar    
- Ordner Kontakt    
- Elemente bearbeiten    
- Löschen von Elementen    
- Elemente lesen
    
Darüber hinaus stehen die folgenden Berechtigungsstufen, die definieren eine Teilmenge von einzelnen Berechtigungen und Werten, wie in Tabelle 2 gezeigt:
  
- Keine    
- Besitzer    
- Vom Typ PublishingEditor    
- Herausgeber    
- PublishingAuthor    
- Autor    
- NoneditingAuthor    
- Prüfer    
- Mitwirkender   
- Benutzerdefinierte - dieser Wert kann nicht von der Anwendung festgelegt werden. Der Server legt diesen Wert, wenn die Anwendung benutzerdefinierte Zusammenstellung von einzelnen Berechtigungen enthält.    
- FreeBusyTimeOnly - kann dies nur für Kalenderordner festgelegt werden.   
- FreeBusyTimeAndSubjectAndLocation - kann dies nur für Kalenderordner festgelegt werden.
    
Die folgende Tabelle enthält die einzelnen Berechtigungen basierend auf Berechtigungsstufe standardmäßig angewendet werden.
  
**In Tabelle 2. Einzelne Berechtigungen von Berechtigungsstufe**

|Berechtigungsstufe|Elemente können erstellen werden.|Unterordner können erstellen werden.|Ist der Besitzer des Ordners|Ordner ist sichtbar|Ordner Kontakt|Elemente bearbeiten|Löschen von Elementen|Lesen von Elementen|
|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|:-----|
|Keine  <br/> |False  <br/> |False  <br/> |False  <br/> |False  <br/> |False  <br/> |Keine  <br/> |Keine  <br/> |Keine  <br/> |
|Besitzer  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |True  <br/> |Alle  <br/> |Alle  <br/> |FullDetails  <br/> |
|Vom Typ PublishingEditor  <br/> |True  <br/> |True  <br/> |False  <br/> |True  <br/> |False  <br/> |Alle  <br/> |Alle  <br/> |FullDetails  <br/> |
|Herausgeber  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |Alle  <br/> |Alle  <br/> |FullDetails  <br/> |
|PublishingAuthor  <br/> |True  <br/> |True  <br/> |False  <br/> |True  <br/> |False  <br/> |Gehören  <br/> |Gehören  <br/> |FullDetails  <br/> |
|Autor  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |Gehören  <br/> |Gehören  <br/> |FullDetails  <br/> |
|NoneditingAuthor  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |Keine  <br/> |Gehören  <br/> |FullDetails  <br/> |
|Prüfer  <br/> |False  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |Keine  <br/> |Keine  <br/> |FullDetails  <br/> |
|Mitwirkender  <br/> |True  <br/> |False  <br/> |False  <br/> |True  <br/> |False  <br/> |Keine  <br/> |Keine  <br/> |Keine  <br/> |
   
Wenn Sie in der Berechtigungen auf Ordnerebene Anforderung eine nicht benutzerdefinierte Berechtigungsstufe angeben, müssen Sie nicht die einzelnen Berechtigungen angeben. Wenn Sie eine einzelne Berechtigung angeben, wenn Sie eine Berechtigungsstufe festgelegt, wird ein Fehler **ErrorInvalidPermissionSettings** in der Antwort zurückgegeben werden. 
  
## <a name="adding-folder-permissions-by-using-the-ews-managed-api"></a>Hinzufügen von Berechtigungen für Ordner mithilfe der EWS Managed API
<a name="bk_enableewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie die EWS Managed API zu verwenden: 
  
- Erstellen Sie ein neues [FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission%28v=exchg.80%29.aspx) -Objekt für den neuen Benutzer. 
    
- Rufen Sie die aktuellen Berechtigungen für einen Ordner mit der Methode [zu binden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) . 
    
- Fügen Sie der neuen **FolderPermissions** der [Folder.Permissions](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.permissions%28v=exchg.80%29.aspx) -Eigenschaft. 
    
- Rufen Sie die [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) -Methode, um die neuen Berechtigungen auf dem Server zu speichern. 
    
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und, die der Benutzer wurde an einen Exchange-Server authentifiziert wurden. 
  
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

Die folgende Codezeile gibt die Berechtigungsstufe.
  
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

Sie können einige oder alle schreibbaren [Eigenschaften FolderPermission](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermission_properties%28v=exchg.80%29.aspx) festlegen, wenn Sie ein **FolderPermission** -Objekt mit der eine benutzerdefinierte Berechtigungsstufe erstellen. Beachten Sie jedoch, dass die [FolderPermissionLevel](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderpermissionlevel%28v=exchg.80%29.aspx) von der Anwendung nicht explizit auf **Custom** festgelegt ist. Die **FolderPermissionLevel** wird nur, wenn ein **FolderPermission** -Objekt erstellen und Festlegen von einzelnen Berechtigungen zu benutzerdefinierten festgelegt. 
  
## <a name="adding-folder-permissions-by-using-ews"></a>Hinzufügen von Berechtigungen für Ordner mithilfe der Exchange-Webdienste
<a name="bk_enableews"> </a>

Die folgenden EWS-Codebeispiele zeigen, wie zum Hinzufügen von Berechtigungen zu einem bestimmten Ordner durch Abrufen der aktuellen Berechtigungen und senden Sie dann eine Liste der neuen Berechtigungen.
  
Der erste Schritt besteht, senden Sie eine [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung, wobei der Wert [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) gibt den Ordner in dem zum Hinzufügen von Berechtigungen (in diesem Beispiel wird der Ordner "Gesendete Objekte") und der [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) Wert enthält Ordner: PermissionSet. Diese Anforderung wird, werden die berechtigungseinstellungen für den angegebenen Ordner abgerufen. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Bind** -Methode zum [Hinzufügen von Berechtigungen für Ordner](#bk_enableewsma)aufrufen.
  
```XML
  <?xml version="1.0" encoding="utf-8"?>
  <soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                 xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                 xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                 xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **GetFolder** mit einer [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die Werte [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) und [ParentFolderId](http://msdn.microsoft.com/library/258f4b1f-367e-4c7d-9c29-eb775a2398c7%28Office.15%29.aspx) wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Verwenden Sie die **UpdateFolder** -Operation im nächsten Schritt die aktualisierte [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx)senden die die [Berechtigung](http://msdn.microsoft.com/library/b8d0429a-0e58-4480-9847-4901970c7033%28Office.15%29.aspx) für den neuen Benutzer enthält. Beachten Sie, dass das [SetFolderField](http://msdn.microsoft.com/library/8c69db7b-54b5-4ae2-abca-4d6e0937a790%28Office.15%29.aspx) -Element für den jeweiligen Ordner in den Vorgang [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) einschließlich die berechtigungseinstellungen für den Ordner überschrieben werden. Entsprechend wird die Option [DeleteFolderField](http://msdn.microsoft.com/library/f9c2187b-4c60-4358-b4b4-ede50eadae48%28Office.15%29.aspx) des Vorgangs **UpdateFolder** einschließlich auch die berechtigungseinstellungen für den Ordner gelöscht. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Update** -Methode zum [Hinzufügen von Berechtigungen für Ordner](#bk_enableewsma)aufrufen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Die folgende Codezeile gibt die Berechtigungsstufe.
  
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

Der Server antwortet auf die Anforderung **UpdateFolder** mit einer [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich aktualisiert wurde.
  
## <a name="removing-folder-permissions-by-using-the-ews-managed-api"></a>Entfernen von Berechtigungen für Ordner mithilfe der EWS Managed API
<a name="bk_removeewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie die EWS Managed API verwenden, um alle Benutzerberechtigungen für einen bestimmten Ordner, mit Ausnahme der standardmäßigen und anonyme Berechtigungen durch entfernen:
  
1. Abrufen der aktuellen Berechtigungen für einen Ordner mit der Methode **zu binden** . 
    
2. Die **Berechtigungen** -Auflistung durchlaufen, und Entfernen von Berechtigungen für einzelne Benutzer. 
    
3. Aufrufen der **Update** -Methode, um die Änderungen zu speichern. 
    
Dieses Beispiel entfernt alle Benutzerberechtigungen für einen Ordner. Wenn Sie in diesem Beispiel wird zum Entfernen von Berechtigungen für einen bestimmten Benutzer nur ändern möchten, ändern Sie die folgende Codezeile zum Identifizieren entweder des Anzeigenamen oder die SMTP-Adresse des Benutzers.
  
```cs
if (sentItemsFolder.Permissions[t].UserId.DisplayName != null || sentItemsFolder.Permissions[t].UserId.PrimarySmtpAddress != null)
```

In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und, die der Benutzer wurde an einen Exchange-Server authentifiziert wurden. 
  
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

## <a name="removing-folder-permissions-by-using-ews"></a>Entfernen von Berechtigungen für Ordner mithilfe der Exchange-Webdienste
<a name="bk_removeews"> </a>

Die folgenden EWS-Codebeispiele zeigen, wie alle Benutzerberechtigungen für einen bestimmten Ordner, mit Ausnahme der Standard- und anonymen Berechtigungen entfernen.
  
Senden Sie zunächst eine [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung, in dem Ordner, in dem Entfernen von Berechtigungen (in diesem Beispiel wird der Ordner "Gesendete Objekte") gibt den [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Wert und der Wert [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) Ordner: PermissionSet enthält. Diese Anforderung wird die [PermissionSet](http://msdn.microsoft.com/library/6ac1bd17-a089-46bb-b9e6-f5b1dfe1076d%28Office.15%29.aspx) für den angegebenen Ordner abrufen. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Bind** -Methode zum [Entfernen von Ordnerberechtigungen für](#bk_removeewsma)aufrufen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **GetFolder** mit einer [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die Werte der Elemente **FolderId** und **ParentFolderId** wurden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="893"
                         MinorBuildNumber="17"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Im nächsten Schritt verwenden Sie die **UpdateFolder** -Operation, um die aktualisierte **PermissionSet**Versand nicht die **Berechtigung** für den entfernten Benutzer enthalten ist. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Update** -Methode zum [Entfernen von Ordnerberechtigungen für](#bk_removeewsma)aufrufen.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **UpdateFolder** mit einer **UpdateFolderResponse** -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Aktualisierung erfolgreich war.
  
## <a name="updating-folder-permissions-by-using-the-ews-managed-api"></a>Aktualisieren von Berechtigungen für Ordner mithilfe der EWS Managed API
<a name="bk_updateewsma"> </a>

Sie können auch die EWS Managed API Ordnerberechtigungen für einen bestimmten Ordner aktualisieren. So aktualisieren Sie die Berechtigungen: 
  
1. [Entfernen von Berechtigungen für den Ordner](#bk_removeewsma) für die veralteten Berechtigungen, aber rufen Sie nicht die **Update** -Methode (noch). 
    
2. [Berechtigungen für die neue oder geänderte Benutzer hinzufügen](#bk_enableewsma).
    
3. Rufen Sie die **Update** -Methode, um die Änderungen zu speichern. 
    
Wenn Sie versuchen, zwei Sätze von Berechtigungen für den gleichen Benutzer hinzufügen, erhalten Sie eine Fehlermeldung **ServiceResponseException** mit der folgenden Beschreibung: "der angegebenen Berechtigungssatz enthält doppelte Benutzer-IDs". In diesem Fall die aktuellen Berechtigungen aus der **Permission** -Auflistung entfernen und dann die neuen Berechtigungen auf der **Permission** -Auflistung hinzufügen. 
  
## <a name="updating-folder-permissions-by-using-ews"></a>Aktualisieren von Berechtigungen für Ordner mithilfe der Exchange-Webdienste
<a name="bk_updateews"> </a>

Sie können auch Berechtigungen für bestimmte Ordner aktualisieren, mithilfe der EWS durch die Kombination des Prozesses zum Entfernen sowie hinzufügen. So aktualisieren Sie die Berechtigungen: 
  
1. Abrufen von aktuellen Berechtigungen für den Ordner mithilfe des **GetFolder** -Vorgangs. 
    
2. Senden Sie eine aktualisierte Liste von Berechtigungen mithilfe des **UpdateFolder** -Vorgangs. 
    
Dies sind die gleichen zwei Vorgänge, die Sie mithilfe von EWS zum [Aktivieren](#bk_enableews) oder [Entfernen Sie den Zugriff](#bk_removeews) verwenden. Der einzige Unterschied ist, wenn Sie die **GetFolder** -Antwort erhalten, eine **Berechtigung** für Benutzer enthalten soll. Ersetzen Sie einfach, vorhandene **Permission** -Element mit dem neuen **Berechtigung** Element, und senden Sie den Vorgang **UpdateFolder** mit den neuen **Berechtigung** oder Werte. 
  
Wenn Sie versuchen, zwei Sätze von Berechtigungen für den gleichen Benutzer hinzufügen, erhalten Sie **ResponseCode** Wert **ErrorDuplicateUserIdsSpecified**. In diesem Fall entfernen Sie den Wert für veralteten Berechtigung für den Benutzer aus der Anforderung, und wiederholen Sie die Anforderung.

## <a name="next-steps"></a>Nächste Schritte

Nachdem Sie eine Benutzer die Berechtigung in einen bestimmten Ordner erteilen, kann der Benutzer eine Stellvertretung den Ordner zugreifen. Weitere Informationen finden Sie unter folgenden Themen:
  
- [Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange](how-to-access-email-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Zugriff auf einen Kalender als Stellvertretung mithilfe der EWS in Exchange](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md)
    
- [Access-Kontakte als Stellvertretung mithilfe der EWS in Exchange](how-to-access-contacts-as-a-delegate-by-using-ews-in-exchange.md)
    
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)   
- [Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    

