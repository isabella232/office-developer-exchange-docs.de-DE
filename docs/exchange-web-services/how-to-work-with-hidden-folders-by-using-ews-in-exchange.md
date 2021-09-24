---
title: Arbeiten mit ausgeblendeten Ordnern mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 7ae7c045-cd90-4c9f-baf5-0464d5058f45
description: Erfahren Sie, wie Sie einen Ordner mithilfe der verwalteten EWS-API oder EWS in Exchange ausgeblendet und ausgeblendete Ordner suchen.
ms.openlocfilehash: 722cc09aa62ae4201362c59f7d7d2b4988e25837
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513073"
---
# <a name="work-with-hidden-folders-by-using-ews-in-exchange"></a>Arbeiten mit ausgeblendeten Ordnern mithilfe von EWS in Exchange

Erfahren Sie, wie Sie einen Ordner mithilfe der verwalteten EWS-API oder EWS in Exchange ausgeblendet und ausgeblendete Ordner suchen.
  
Mit einer Ausnahme werden Ordner im Stammverzeichnis eines Exchange Postfachs (die Nicht-IPM-Unterstruktur) für den Benutzer ausgeblendet. Umgekehrt sind alle Ordner in der **MsgFolderRoot** (die IPM-Unterstruktur) für den Benutzer sichtbar. Wie blenden Sie also einen Ordner unter **"MsgFolderRoot" aus?** Es ist nicht so schwierig – es kommt nur auf eine Eigenschaft an, die erweiterte [Eigenschaft PidTagAttributeHidden](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B). Wenn diese Eigenschaft auf **"true"** festgelegt ist, blendet Outlook oder ein anderer Client, der die Eigenschaft verwendet, um die Sichtbarkeit des Ordners zu bestimmen, den Ordner aus der Ansicht des Benutzers aus. Da es sich um eine erweiterte Eigenschaft handelt, ist die Verwendung komplexer als die durchschnittliche Ordnereigenschaft. Daher werden Sie in diesem Artikel durch die hauptszenarien geführt.
  
**Tabelle 1. Verwaltete EWS-API-Methoden und EWS-Vorgänge zum Arbeiten mit ausgeblendeten Ordnern**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Ausblenden eines Ordners  <br/> |[Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Suchen nach ausgeblendeten Ordnern  <br/> |[FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |[FindFolder](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
   
Fragen Sie sich, was die einzige Ausnahme ist – d. a. welcher Ordner im Stammordner ist für Benutzer sichtbar? Es ist der Finder-Ordner (auch bekannt als **SearchFolders**[WellKnownFolder-Enumerationswert](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) oder der **Suchordner**[DistinguishedFolderId-Elementwert),](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) der die Suchordner der Benutzer enthält. Im Ordner "Finder" erstellte Suchordner sind für Outlook Benutzer sichtbar. Wenn Sie einen Suchordner erstellen müssen, der für Benutzer nicht sichtbar ist, verschieben Sie ihn unter den Stammordner, um ihn auszublenden. Im Gegensatz zu anderen Ordnern blendet das Festlegen der **PidTagAttributeHidden-Eigenschaft** auf **"true"** keinen Suchordner im Ordner "Finder" aus. 
  
## <a name="hide-a-folder-by-using-the-ews-managed-api"></a>Ausblenden eines Ordners mithilfe der verwalteten EWS-API
<a name="bk_hideewsma"> </a>

Sie können einen vorhandenen Ordner als ausgeblendeten Ordner [festlegen,](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) indem Sie die erweiterte [PidTagAttributeHidden-Eigenschaft](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) in **"true"** ändern. Erstellen Sie zunächst eine [erweiterte Eigenschaftsdefinition für die Eigenschaft.](properties-and-extended-properties-in-ews-in-exchange.md) Verwenden Sie [](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) als Nächstes die Bind-Methode, um zum Ordner zu gelangen, aktualisieren Sie dann den Wert der **PidTagAttributeHidden-Eigenschaft** auf "true", und verwenden Sie die [Update-Methode,](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) um die Änderungen zu speichern. 
  
In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer ist, dass der Benutzer bei einem Exchange-Server authentifiziert wurde und dass **folderId** ein gültiger [Folder.Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) ist, der den auszublendenden Ordner identifiziert. 
  
```cs
private static void MakeHidden(FolderId folderId, ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    PropertySet propSet = new PropertySet(isHiddenProp);
    // Bind to a folder and retrieve the PidTagAttributeHidden property.
    Folder folder = Folder.Bind(service, folderId, propSet);
    // Set the PidTagAttributeHidden property to true.
    folder.SetExtendedProperty(isHiddenProp, true);
    // Save the changes.
    folder.Update();
}
```

## <a name="hide-a-folder-by-using-ews"></a>Ausblenden eines Ordners mithilfe von EWS
<a name="bk_hideews"> </a>

Sie können EWS verwenden, um einen vorhandenen Ordner zu einem ausgeblendeten Ordner zu [machen,](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) indem Sie die erweiterte [PidTagAttributeHidden-Eigenschaft](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) in **"true"** ändern. Verwenden Sie zunächst den [GetFolder-Vorgang,](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) um zum Ordner zu gelangen, und rufen Sie dann die **PidTagAttributeHidden-Eigenschaft** ab, indem Sie das [ExtendedFieldURI-Element](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) einschließen und den **PropertyTag-Wert** auf 4340 und den **PropertyType-Wert** auf Boolean festlegen. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Bind-Methode** verwenden, um einen Ordner abzurufen, bevor [Sie ihn zu einem ausgeblendeten Ordner machen.](#bk_hideewsma)
  
Der [FolderId-Wert](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) wird zur besseren Lesbarkeit gekürzt. 
  
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
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:FolderIds>
        <t:FolderId Id="IQywAAAA==" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **GetFolder-Anforderung** mit einer [GetFolderResponse-Nachricht,](https://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **"NoError"** enthält, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die Antwort enthält auch einen [Wert](https://msdn.microsoft.com/library/196278d4-5e77-4e0a-8af6-8ac065610510%28Office.15%29.aspx) für [extendedProperty](https://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx). In diesem Beispiel wird der **Wert** auf **"false"** festgelegt, was bedeutet, dass der Ordner derzeit nicht ausgeblendet ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
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
              <t:FolderId Id="IQywAAAA=="
                          ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
              <t:ExtendedProperty>
                <t:ExtendedFieldURI PropertyTag="0x10f4"
                                    PropertyType="Boolean" />
                <t:Value>false</t:Value>
              </t:ExtendedProperty>
            </t:Folder>
          </m:Folders>
        </m:GetFolderResponseMessage>
      </m:ResponseMessages>
    </m:GetFolderResponse>
  </s:Body>
</s:Envelope>
```

Verwenden Sie den [UpdateFolder-Vorgang,](https://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) um den Wert von **ExtendedProperty** in "true" zu ändern. Schließen Sie die Elemente **ExtendedProperty,** **ExtendedFieldURI** und **Value** für die erweiterte **PidTagAttributeHidden-Eigenschaft ein,** und legen Sie das **Value-Element** auf **"true"** fest, um den Ordner auszublenden. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **Update-Methode** verwenden, um einen Ordner zu aktualisieren, um [ihn zu einem ausgeblendeten Ordner](#bk_hideewsma)zu machen.
  
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
          <t:FolderId Id="IQywAAAA=="
                      ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAABED" />
          <t:Updates>
            <t:SetFolderField>
              <t:ExtendedFieldURI PropertyTag="4340"
                                  PropertyType="Boolean" />
              <t:Folder>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="4340"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:SetFolderField>
          </t:Updates>
        </t:FolderChange>
      </m:FolderChanges>
    </m:UpdateFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **UpdateFolder-Anforderung** mit einer [UpdateFolderResponse-Nachricht,](https://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass der Ordner erfolgreich aktualisiert wurde und jetzt ausgeblendet ist.
  
## <a name="find-all-hidden-folders-by-using-the-ews-managed-api"></a>Suchen aller ausgeblendeten Ordner mithilfe der verwalteten EWS-API
<a name="bk_findhiddenewsma"> </a>

Sie können alle ausgeblendeten Ordner unter einem übergeordneten Ordner suchen, indem Sie eine [erweiterte Eigenschaftsdefinition](properties-and-extended-properties-in-ews-in-exchange.md) für die erweiterte **PidTagAttributeHidden** -Eigenschaft erstellen und dann die [FindFolders](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) -Methode verwenden, um Ordner mit einem **PidTagAttributeHidden** -Wert zu suchen, der auf **"true"** festgelegt ist. In diesem Beispiel wird "MsgFolderRoot", auch bekannt als "Top of Information"-Store oder IPM-Unterstruktur, als übergeordneter Ordner verwendet, unter dem gesucht werden soll.
  
In diesem Beispiel wird davon ausgegangen, dass der **Dienst** ein gültiges [ExchangeService-Objekt](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer ist und dass der Benutzer bei einem Exchange Server authentifiziert wurde. 
  
```cs
private static void FindHiddenFolders(ExchangeService service)
{
    // Create an extended property definition for the PidTagAttributeHidden property.
    ExtendedPropertyDefinition isHiddenProp = new ExtendedPropertyDefinition(0x10f4, MapiPropertyType.Boolean);
    // Create a folder view to retrieve up to 100 folders and 
    // retrieve only the PidTagAttributeHidden and the display name.
    FolderView folderView = new FolderView(100);
    folderView.PropertySet = new PropertySet(isHiddenProp, FolderSchema.DisplayName);
    // Indicate a Traversal value of Deep, so that all subfolders are retrieved.
    folderView.Traversal = FolderTraversal.Deep;
    // Find all hidden folders under the MsgFolderRoot.
    // This call results in a FindFolder call to EWS.
    FindFoldersResults findFolder = service.FindFolders(WellKnownFolderName.MsgFolderRoot,
            new SearchFilter.IsEqualTo(isHiddenProp, true), folderView);
    // Display the folder ID and display name of each hidden folder.
    foreach (Folder folder in findFolder)
    {
        Console.WriteLine("FolderId: {0}", folder.Id);
        Console.WriteLine("DisplayName: {0}", folder.DisplayName);
        Console.WriteLine("\r\n");
    }
}
```

## <a name="find-all-hidden-folders-by-using-ews"></a>Suchen aller ausgeblendeten Ordner mithilfe von EWS
<a name="bk_findhiddenews"> </a>

Sie können EWS verwenden, um alle ausgeblendeten Ordner unter einem vorhandenen Ordner zu suchen, indem Sie den [FindFolder-Vorgang](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) aufrufen und nach Ordnern suchen, deren erweiterte [PidTagAttributeHidden-Eigenschaft](https://msdn.microsoft.com/library/cc433490%28v=exchg.80%29.aspx) auf **"true"** festgelegt ist. Fügen Sie hierzu eine [IsEqualTo-Einschränkung](https://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[](https://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) hinzu, die nach dem [ExtendedFieldURI-Element](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) für die **PidTagAttributeHidden-Eigenschaft** sucht ( **PropertyTag-Wert** auf 4243 und der **PropertyType-Wert** auf Boolean), wie in der folgenden Anforderung dargestellt. In diesem Beispiel wird "MsgFolderRoot", auch bekannt als "Top of Information"-Store oder IPM-Unterstruktur, als übergeordneter Ordner verwendet, unter dem gesucht werden soll. 
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **FindFolders** -Methode verwenden, um [alle ausgeblendeten Ordner](#bk_findhiddenewsma)zu finden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2007_SP1" />
    <t:TimeZoneContext>
      <t:TimeZoneDefinition Id="Central Standard Time" />
    </t:TimeZoneContext>
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Deep">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURI FieldURI="folder:DisplayName" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="100"
                               Offset="0"
                               BasePoint="Beginning" />
      <m:Restriction>
        <t:IsEqualTo>
          <t:ExtendedFieldURI PropertyTag="4340"
                              PropertyType="Boolean" />
          <t:FieldURIOrConstant>
            <t:Constant Value="true" />
          </t:FieldURIOrConstant>
        </t:IsEqualTo>
      </m:Restriction>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="msgfolderroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **FindFolder-Anforderung** mit einer [FindFolderResponse-Nachricht,](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) die den [ResponseCode-Elementwert](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** enthält, der angibt, dass die Ordnersuche erfolgreich war, sowie alle ausgeblendeten Ordner unter dem Stammnachrichtenordner.
  
Die [FolderId-Werte](https://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) werden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="https://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="6"
                        TotalItemsInView="6"
                        IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="IBHgAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACz" />
                <t:DisplayName>{06967759-274D-40B2-A3EB-D7F9E73727D7}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHwAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAAC7" />
                <t:DisplayName>{A9E2BC46-B3A0-4243-B315-60D991004455}</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBIQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAADO" />
                <t:DisplayName>GAL Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:ContactsFolder>
                <t:FolderId Id="IBHQAAAA=="
                            ChangeKey="AwAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACa" />
                <t:DisplayName>Recipient Cache</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="HAAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAAAACS" />
                <t:DisplayName>Conversation Action Settings</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
              <t:Folder>
                <t:FolderId Id="IQywAAAA=="
                            ChangeKey="AQAAABYAAAD32nSTjepyT63rYH17n9THAAAeZIBf" />
                <t:DisplayName>TestFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x10f4"
                                      PropertyType="Boolean" />
                  <t:Value>true</t:Value>
                </t:ExtendedProperty>
              </t:Folder>
            </t:Folders>
          </m:RootFolder>
        </m:FindFolderResponseMessage>
      </m:ResponseMessages>
    </m:FindFolderResponse>
  </s:Body>
</s:Envelope>
```

## 
<a name="bk_findhiddenews"> </a>

Nachdem Sie ordner ausgeblendet oder ausgeblendet haben, können Sie die Ordnerhierarchie abrufen oder [die Ordnerhierarchie synchronisieren.](how-to-synchronize-folders-by-using-ews-in-exchange.md) Die Beispiele, die zeigen, wie Sie [eine Ordnerhierarchie mithilfe der verwalteten EWS-API abrufen](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) oder [eine Ordnerhierarchie mithilfe von EWS abrufen,](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) zeigen auch an, welche Ordner in der Hierarchie ausgeblendet sind. 
  
## <a name="see-also"></a>Siehe auch


- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Arbeiten mit Ordnern unter Verwendung von EWS in Exchange](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Arbeiten mit Suchordnern mithilfe von EWS in Exchange](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    

