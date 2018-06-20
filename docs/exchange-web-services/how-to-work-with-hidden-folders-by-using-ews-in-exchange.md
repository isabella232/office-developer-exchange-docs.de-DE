---
title: Arbeiten Sie mit verborgene Ordner im Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7ae7c045-cd90-4c9f-baf5-0464d5058f45
description: Hier erfahren Sie, wie Sie einen Ordner ausgeblendet, und suchen Sie verborgene Ordner durch Verwenden der EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 72efc16ecc247d307b7300526e7d345fe6bdd3ac
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757020"
---
# <a name="work-with-hidden-folders-by-using-ews-in-exchange"></a>Arbeiten Sie mit verborgene Ordner im Exchange mithilfe der Exchange-Webdienste

Hier erfahren Sie, wie Sie einen Ordner ausgeblendet, und suchen Sie verborgene Ordner durch Verwenden der EWS Managed API oder EWS in Exchange.
  
Ordner im Stamm des Exchange-Postfach (der IPM Unterstruktur) werden mit einer Ausnahme vom Benutzer ausgeblendet. Umgekehrt sind alle Ordner in der **MsgFolderRoot** (IPM-Unterstruktur) für den Benutzer sichtbar. So wie ausblenden Sie einen Ordner unterhalb der **MsgFolderRoot**? Es ist nicht das schwierig – es darum, nur einer Eigenschaft, die [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) (0x10F4000B) extended-Eigenschaft. Wenn diese Eigenschaft auf **true**festgelegt ist, wird Outlook oder einem anderen Client, der die-Eigenschaft verwendet, um die Sichtbarkeit der Ordner bestimmen den Ordner aus Sicht der Benutzer ausblenden. Da es sich um eine erweiterte Eigenschaft handelt, ist es schwieriger zu als die durchschnittliche Ordnereigenschaft verwenden, damit Sie in diesem Artikel über die wichtigsten Szenarien durchlaufen wird.
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Arbeit mit verborgene Ordner**

|**Aufgabe**|**EWS Managed API-Methode**|**EWS-Vorgang**|
|:-----|:-----|:-----|
|Ausblenden eines Ordners  <br/> |[Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) gefolgt von [Folder.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) <br/> |[GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) gefolgt von [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) <br/> |
|Hier finden Sie verborgene Ordner  <br/> |[FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) <br/> |[FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) <br/> |
   
Sind Sie wissen, was die einzige Ausnahme ist – d. h., welche Ordner im Stamm für Benutzer sichtbar ist? Es ist die Finder-Ordner (auch bekannt als die **SearchFolders**-[WellKnownFolder](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.wellknownfoldername%28v=exchg.80%29.aspx) -Enumerationswert ab, oder der **Searchfolders**[DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) -Elementwert) der Benutzer die Suchordner enthält. Im Ordner "Finder" erstellten Suchordner sind für Benutzer in Outlook angezeigt. Wenn Sie müssen einen Suchordner erstellen, der für Benutzer nicht sichtbar ist, verschieben Sie es unter dem Stammordner auszublenden. Im Gegensatz zu werden für andere Ordner die **PidTagAttributeHidden** -Eigenschaft auf **true** festlegen keinen Suchordner im Ordner "Finder" ausgeblendet. 
  
## <a name="hide-a-folder-by-using-the-ews-managed-api"></a>Ausblenden eines Ordners mithilfe der EWS Managed API
<a name="bk_hideewsma"> </a>

Sie können [einen bestehenden Ordner stellen](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) einen versteckten Ordner durch Ändern der erweiterten Eigenschaft auf **true fest,** [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) . Erstellen Sie zunächst eine [erweiterten Eigenschaftendefinition für die Eigenschaft](properties-and-extended-properties-in-ews-in-exchange.md). Im nächsten Schritt verwenden Sie die Methode [zu binden](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) auf den Ordner zugreifen und dann aktualisieren Sie den Wert der **PidTagAttributeHidden** -Eigenschaft auf true und die [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.update%28v=exchg.80%29.aspx) -Methode verwenden, um die Änderungen zu speichern. 
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist eine gültige [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) für den Postfachbesitzer-Objekt zurück, der Benutzer wurde an einen Exchange-Server authentifiziert wurden und diese **FolderId** ist eine gültige [Folder.Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.id%28v=exchg.80%29.aspx) , der den Ordner ausblenden identifiziert. 
  
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

## <a name="hide-a-folder-by-using-ews"></a>Ausblenden eines Ordners mithilfe der Exchange-Webdienste
<a name="bk_hideews"> </a>

EWS können [stellen einen bestehenden Ordner](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_createfolderewsma) einen versteckten Ordner durch Ändern der erweiterten Eigenschaft auf **true fest,** [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) . Verwenden des [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Vorgangs, um auf den Ordner zugreifen zunächst, einschließlich des [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Elements und Festlegen der **' PropertyTag '** -Wert, der 4340 und die **PropertyType Abrufen der **PidTagAttributeHidden** -Eigenschaft **in einen booleschen Wert. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Bind** -Methode verwenden, um einen Ordner, bevor [es einen versteckten Ordner](#bk_hideewsma)abrufen.
  
Der [Ordner-ID](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -Wert wird zur besseren Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die Anforderung **GetFolder** mit einer [GetFolderResponse](http://msdn.microsoft.com/library/47abeec8-78dd-4297-8525-099174ec880d%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich abgerufen wurde. Die Antwort enthält auch einen [Wert](http://msdn.microsoft.com/library/196278d4-5e77-4e0a-8af6-8ac065610510%28Office.15%29.aspx) für die [ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx). In diesem Beispiel wird der **Wert** auf **false**festgelegt, was bedeutet, dass der Ordner derzeit nicht ausgeblendet ist.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
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

Wenn Sie um den Wert der **ExtendedProperty** auf "true" zu ändern, verwenden Sie die [UpdateFolder](http://msdn.microsoft.com/library/3494c996-b834-4813-b1ca-d99642d8b4e7%28Office.15%29.aspx) -Operation. Enthalten Sie die **ExtendedProperty**, **ExtendedFieldURI**und **Value** -Elemente, für die **PidTagAttributeHidden** erweiterte Eigenschaft, und legen Sie das **Value** -Element auf **true fest,** um den Ordner auszublenden. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **Update** -Methode verwenden, um einen Ordner mit dem [sie einen ausgeblendete Ordner](#bk_hideewsma)aktualisieren.
  
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

Der Server antwortet auf die Anforderung **UpdateFolder** mit einer [UpdateFolderResponse](http://msdn.microsoft.com/library/31f47739-dc9c-46ba-9e3f-cce25dc85e6e%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass der Ordner erfolgreich aktualisiert wurde, und ist jetzt ausgeblendet.
  
## <a name="find-all-hidden-folders-by-using-the-ews-managed-api"></a>Hier finden Sie alle ausgeblendeten Ordner mithilfe der EWS Managed API
<a name="bk_findhiddenewsma"> </a>

Finden Sie unter einem übergeordneten Ordner ausgeblendete Ordner durch Erstellen einer [erweiterten Eigenschaftsdefinition](properties-and-extended-properties-in-ews-in-exchange.md) für die erweiterte Eigenschaft **PidTagAttributeHidden** , und klicken Sie dann mithilfe der Methode [FindFolders](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findfolders%28v=exchg.80%29.aspx) Ordner mit einer **Suchen PidTagAttributeHidden** -Wert, der auf **true**festgelegt ist. In diesem Beispiel wird die MsgFolderRoot, auch als die oberste Ebene des Informationsspeichers oder IPM-Unterstruktur bezeichnet, mit dem übergeordneten Ordner unter Suchen.
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Besitzer des Postfachs und der Benutzer wurde an einen Exchange-Server authentifiziert wurden. 
  
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

## <a name="find-all-hidden-folders-by-using-ews"></a>Hier finden Sie alle ausgeblendeten Ordner mithilfe der Exchange-Webdienste
<a name="bk_findhiddenews"> </a>

Verwenden von EWS ausgeblendete Ordner unter einem vorhandenen Ordner finden, indem Sie den Vorgang [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) aufrufen und Ordner gesucht, deren [PidTagAttributeHidden](http://msdn.microsoft.com/en-us/library/cc433490%28v=exchg.80%29.aspx) erweiterte Eigenschaft auf **true**festgelegt. Dazu gehören Sie eine ["IsEqualTo"](http://msdn.microsoft.com/library/48e7e067-049c-4184-8026-071e6f558e8a%28Office.15%29.aspx)[Einschränkung](http://msdn.microsoft.com/library/77f19014-d112-4999-8e83-ecc32a117a73%28Office.15%29.aspx) , die für das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element für die **PidTagAttributeHidden** -Eigenschaft ( **' PropertyTag '** -Wert, der 4243 und der **PropertyType** Wert in einen booleschen Wert) durchsucht wie in der folgenden Anforderung dargestellt. In diesem Beispiel wird die MsgFolderRoot, auch als die oberste Ebene des Informationsspeichers oder IPM-Unterstruktur bezeichnet, mit dem übergeordneten Ordner unter Suchen. 
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die Methode **FindFolders** , [erhalten alle ausgeblendeten Ordner](#bk_findhiddenewsma)verwenden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **FindFolder** mit einer [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Suche Ordner erfolgreich war, und alle ausgeblendeten der Ordner unter dem Stammordner der Nachricht.
  
Die [FolderId](http://msdn.microsoft.com/library/00d14e3e-4365-4f21-8f88-eaeea73b9bf7%28Office.15%29.aspx) -Werte werden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="898"
                         MinorBuildNumber="23"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Erst, nachdem Sie sind ausgeblendet oder eingeblendet Ordner möglicherweise möchten Sie die Ordnerhierarchie oder [die Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md)möchten. In den Beispielen, die zeigen, dass Sie wie zum [Abrufen einer Ordnerhierarchie mithilfe der EWS Managed API](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyewsma) oder [Abrufen eine Ordnerhierarchie mithilfe der Exchange-Webdienste](how-to-work-with-folders-by-using-ews-in-exchange.md#bk_getfolderhierarchyews) auch welche Ordner in der Hierarchie angeben, werden ausgeblendet. 
  
## <a name="see-also"></a>Siehe auch


- [Ordner und Elemente in EWS in Exchange](folders-and-items-in-ews-in-exchange.md)
    
- [Arbeiten Sie mit Ordnern in Exchange mithilfe der Exchange-Webdienste](how-to-work-with-folders-by-using-ews-in-exchange.md)
    
- [Arbeiten Sie mit Suchordner in Exchange mithilfe der Exchange-Webdienste](how-to-work-with-search-folders-by-using-ews-in-exchange.md)
    

