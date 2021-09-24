---
title: Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Alle Anforderungen für Informationen zu öffentlichen Ordnern, die den Inhalt des öffentlichen Ordners betreffen, müssen an das Postfach für öffentliche Ordner weitergeleitet werden, das den Inhalt für den Zielordner enthält. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die Header "X-AnchorMailbox" und "X-PublicFolderMailbox" auf bestimmte Werte festlegen.
ms.openlocfilehash: d5a066a63d9bc3b48c41473545343125538d856b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521102"
---
# <a name="route-public-folder-content-requests"></a>Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner

Alle Anforderungen für Informationen zu öffentlichen Ordnern, die den Inhalt des öffentlichen Ordners betreffen, müssen an das Postfach für öffentliche Ordner weitergeleitet werden, das den Inhalt für den Zielordner enthält. Um die Anforderungen an dieses Postfach weiterzuleiten, müssen Sie die **Header "X-AnchorMailbox"** und **"X-PublicFolderMailbox"** auf bestimmte Werte festlegen. 
  
Die folgende Tabelle enthält eine Übersicht über den Prozess:
  
**Übersicht über öffentliche Ordner**

|Header|Was benöte ich?|Wie erhalte ich es?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |1. [Die X-AnchorMailbox- und X-PublicFolderInformation-Werte ](how-to-route-public-folder-hierarchy-requests.md) für das Postfach der Hierarchie öffentlicher Ordner.<br/><br/>2. Die GUID des Postfachs für öffentliche Ordner, das den Postfachinhalt enthält, der an den AutoErmittlungsdienst gesendet wird.<br/><br/>  Die **AutoDiscoverSMTPAddress** in der AutoErmittlungsantwort wird zum Wert des **X-AnchorMailbox-Headers.**  <br/> ![TODO](media/Ex15_PF_PFContent.png)| 1. Verwenden Sie das Codebeispiel in diesem Artikel, in [dem die verwaltete EWS-API implementiert](#bk_determineguidewsma)wird. Oder [verwenden Sie EWS,](#bk_determineguidews) und konvertieren Sie Ihre Ergebnisse, um eine GUID abzurufen.<br/><br/>2. [Stellen Sie eine AutoErmittlungsanforderung](#bk_makeautodrequest) mithilfe der GUID und des Domänennamens.<br/><br/>3. Verwenden Sie den Wert des **AutoDiscoverSMTPAddress-Elements,** das in der AutoErmittlungsantwort zurückgegeben wird, um [den Wert der Kopfzeilen aufzufüllen.](#bk_setheadervalues)  <br/> |
|**X-PublicFolderMailbox** <br/> |Ihre Arbeit ist abgeschlossen, der X-PublicFolderMailbox-Wert ist identisch mit dem X-AnchorMailbox-Wert!  <br/> |Sie haben es bereits!  <br/> |
   
Nachdem Sie die Headerwerte bestimmt haben, schließen Sie sie [ein, wenn Sie Inhaltsanforderungen](#bk_setheadervalues)für öffentliche Ordner stellen.
  
Die Schritte in diesem Artikel gelten speziell für Anforderungen für Inhalte öffentlicher Ordner. Informationen dazu, ob es sich bei Ihrer Anforderung um eine Hierarchie öffentlicher Ordner oder eine Inhaltsanforderung handelt, finden Sie unter [Routing von Anforderungen für öffentliche Ordner.](public-folder-access-with-ews-in-exchange.md#bk_routing)

<a name="bk_determineguidewsma"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a>Ermitteln der GUID des Postfachs für öffentliche Ordner mithilfe der verwalteten EWS-API


Um die GUID des Postfachs für Öffentliche Ordner-Inhalte zu ermitteln, verwenden Sie das folgende Codebeispiel, in dem Folgendes ausgeführt wird: 
  
- Verwendet die **X-AnchorMailbox-** und **X-PublicFolderInformation-Header,** die Sie durch Weiterleiten von [Anforderungen für die Hierarchie öffentlicher Ordner](how-to-route-public-folder-hierarchy-requests.md)abgerufen haben.
    
- Ruft die [FindFolders-Methode](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) der verwalteten EWS-API auf und enthält eine Anforderung für die **eigenschaft PR_REPLICA_LIST** (0x66980102). 
    
Der **wert PR_REPLICA_LIST** identifiziert die Postfach-GUID des Postfachs für öffentliche Ordner, das den Inhalt für den Ordner enthält. Die **PR_REPLICA_LIST-Eigenschaft** ist ein Bytearray, wird jedoch als GUID für dieses Szenario umgewandelt. Die GUID und der Domänenname sind mit der Adresse verkettet, unter der die AutoErmittlung aufgerufen werden soll. 
  
In diesem Beispiel wird davon ausgegangen, dass es sich um das ExchangeService-Objekt für den Postfachbenutzer handelt. Dabei handelt es sich um `service` die Werte der Header [](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) `PFHAnchorHeader` `PFHMailboxHeader` **X-AnchorMailbox** und **X-PublicFolderMailbox,** und die Domäne ist der domänenname, der vom Mandanten verwendet wird. 
  
```cs
public static string GetMailboxGuidAddress(ExchangeService service, String PFHAnchorHeader, String PFHMailboxHeader, String domain)
{
    // Create a new folder view, and pass in the maximum number of folders to return.
    FolderView view = new FolderView(10);
    // Create an extended property definition for the PR_REPLICA_LIST property.
    ExtendedPropertyDefinition PR_REPLICA_LIST = new ExtendedPropertyDefinition(0x6698, MapiPropertyType.Binary);
    // As a best practice, limit the properties returned to only those required.
    // In this case, return the folder ID, the folder display name, and 
    // the value of the PR_REPLICA_LIST extended property definition.
    view.PropertySet = new PropertySet(BasePropertySet.IdOnly, FolderSchema.DisplayName, PR_REPLICA_LIST);
    service.HttpHeaders.Add("X-AnchorMailbox", PFHAnchorHeader);
    service.HttpHeaders.Add("X-PublicFolderMailbox", PFHMailboxHeader);
    // Add a call to the CertificateValidationCallback method here if needed.
    // ServicePointManager.ServerCertificateValidationCallback = CertificateValidationCallBack;
    // Call FindFolders to retrieve the folder hierarchy, starting with the PublicFolderRoot folder.
    // This method call results in a FindFolder call to EWS.
    FindFoldersResults findResults = service.FindFolders(WellKnownFolderName.PublicFoldersRoot, view);
    string GuidAsString = null;
    List<string> Guids = new List<string>();
    // For each folder under the root, display the name, and copy the value of the 
    // PR_REPLICA_LIST byte array to a string value. 
    foreach (Folder folder in findResults.Folders)
    {
        Console.WriteLine("Public folder display name: {0}", folder.DisplayName);
        byte[] ByteArr = (byte[])folder.ExtendedProperties[0].Value;
        GuidAsString = System.Text.Encoding.ASCII.GetString(ByteArr, 0, 36);
        Guids.Add(GuidAsString);
        Console.WriteLine("Address for Autodiscover: {0}.{1}\r\n", GuidAsString, domain);
    }
    // Concatenate the GUID value of the PR_REPLICA_LIST with the domain name to generate the 
    // SMTP address to use for the AutoDiscover request for the public folder content mailbox.
    string AutoDSMTPAddress = GuidAsString + "@" + domain;
    // Check that all folders have the same GUID value. If they do not, use the GUID value of the
    // folder that you're requesting content for.
    string commonGuid = CompareGuidsForEquality(Guids);
    if (commonGuid == "Not Equal")
    {
        Console.WriteLine("The GUIDs for all the folders in the hierarchy are not the same. Run the Autodiscover sample using the address returned above that is associated with the folder in your hierarchy request.", AutoDSMTPAddress);
        return null;
    }
    else
    {
        Console.WriteLine("The GUIDs for all public folders in the hierarchy are the same. Run the Autodiscover sample using the {0} address.", AutoDSMTPAddress);
        return AutoDSMTPAddress;
    }
}
// Method to compare the GUID for each folder under the public folder root.
// If each GUID is the same, return the GUID.
// If the GUIDs are not the same, return "Not equal".
public static string CompareGuidsForEquality(List<string> list)
{
    string NotEqual = "Not equal";
    string first = list.First();
    return list.All(x => x == first) ? first : NotEqual;
}
```

Wenn Sie die Fehlermeldung "Die Anforderung ist fehlgeschlagen. Die zugrunde liegende Verbindung wurde geschlossen: Es konnte keine Vertrauensstellung für den sicheren SSL/TLS-Kanal hergestellt werden." Sie müssen [einen Aufruf einer Überprüfungsrückrufmethode hinzufügen.](how-to-validate-a-server-certificate-for-the-ews-managed-api.md) Ein Platzhalter und ein Kommentar für diese Methode sind im Codebeispiel enthalten.
  
Wenn die Postfach-GUID für alle öffentlichen Ordner im Stammverzeichnis des öffentlichen Ordners identisch ist, gibt das Beispiel die Adresse an, die beim Aufrufen der [AutoErmittlung](#bk_makeautodrequest) in der Konsolenausgabe und als Rückgabewert verwendet werden soll. Wenn die Postfach-GUID nicht für alle öffentlichen Ordner im Stammverzeichnis öffentlicher Ordner identisch ist, müssen Sie [eine AutoErmittlungsanforderung](#bk_makeautodrequest) für die Adresse vornehmen, die dem Ordner in Ihrer Inhaltsanforderung zugeordnet ist. 

<a name="bk_determineguidews"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a>Ermitteln der GUID des Postfachs für öffentliche Ordner mithilfe von EWS

Das folgende Codebeispiel zeigt, wie der Wert der **PR_REPLICA_LIST** (0x66980102)-Eigenschaft mithilfe des EWS [FindFolder-Vorgangs](https://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) abgerufen wird. Für das [ExtendedFieldURI-Element](https://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) wird das **PropertyTag-Attribut** auf den Dezimalwert (26264) der **PR_REPLICA_LIST-Eigenschaft** festgelegt, und das **PropertyType-Attribut** wird auf **Binary** festgelegt.
  
Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie die **FindFolders-Methode** verwenden, um [die GUID des Postfachs für öffentliche Ordner mithilfe der verwalteten EWS-API](#bk_determineguidewsma)zu ermitteln.
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
Accept: text/xml
User-Agent: ExchangeServicesClient/15.00.0913.015
Accept-Encoding: gzip,deflate
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Cookie: ClientId=KZPBLKA9ZMPXAQDW
Content-Length: 1005
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindFolder Traversal="Shallow">
      <m:FolderShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="folder:DisplayName" />
          <t:ExtendedFieldURI PropertyTag="26264" PropertyType="Binary" />
        </t:AdditionalProperties>
      </m:FolderShape>
      <m:IndexedPageFolderView MaxEntriesReturned="10" Offset="0" BasePoint="Beginning" />
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:ParentFolderIds>
    </m:FindFolder>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **FindFolder-Anforderung** mit einer [FindFolderResponse-Nachricht,](https://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) die den Wert der **PR_REPLICA_LIST** erweiterten Eigenschaft enthält. Beachten Sie, dass der Wert der Eigenschaft in der EWS-Antwort als Zeichenfolgenformat eines Base64-codierten Bytearrays angezeigt wird. Einige Headerwerte in der Antwort werden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="https://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15" MinorVersion="0" MajorBuildNumber="1019" MinorBuildNumber="15" Version="V2_17" xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types" xmlns="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:xsd="http://www.w3.org/2001/XMLSchema" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"/>
  </s:Header>
  <s:Body>
    <m:FindFolderResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindFolderResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="2" TotalItemsInView="2" IncludesLastItemInRange="true">
            <t:Folders>
              <t:ContactsFolder>
                <t:FolderId Id="AAEuAAAAAADL8shaNEKnQYVvRbpoY9vDAQBGDloItRzyTrAt+XVzRr/YAABdofPkAAA=" ChangeKey="AwAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/2h"/>
                <t:DisplayName>My Public Contacts</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
                </t:ExtendedProperty>
              </t:ContactsFolder>
              <t:Folder>
                <t:FolderId Id="AQEuAAADy/LIWjRCp0GFb0W6aGPbwwEARg5aCLUc8k6wLfl1c0a/2AAAAxEAAAA=" ChangeKey="AQAAABYAAABGDloItRzyTrAt+XVzRr/YAABdo/W/"/>
                <t:DisplayName>SampleFolder</t:DisplayName>
                <t:ExtendedProperty>
                  <t:ExtendedFieldURI PropertyTag="0x6698" PropertyType="Binary"/>
                  <t:Value>MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA==</t:Value>
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

Um den Wert der im XML-Code zurückgegebenen **PR_REPLICA_LIST** zu verwenden, muss der Wert in einem Format konvertiert werden, das dem Konvertieren des Werts im Codebeispiel der [verwalteten EWS-API](#bk_determineguidewsma)ähnelt, um die Postfach-GUID zu ermitteln. Die GUID wird dann mit dem Domänennamen verkettet, um eine SMTP-Adresse zu erstellen, die in der [AutoErmittlungsanforderung](#bk_makeautodrequest)enthalten ist.
  
## <a name="make-an-autodiscover-request"></a>Erstellen einer AutoErmittlungsanforderung
<a name="bk_makeautodrequest"> </a>

Verwenden Sie die von der Methode zurückgegebene  `GetMailboxGuidAddress` Adresse, um die AutoErmittlung aufzurufen. Es wird empfohlen, die [Exchange 2013: Abrufen von Benutzereinstellungen mithilfe](https://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) des AutoErmittlungscodebeispiels zum Aufrufen des AutoErmittlungsdiensts zu verwenden, da dadurch der AutoErmittlungsprozess optimiert wird. In diesem Codebeispiel werden die in der folgenden Tabelle aufgeführten Befehlszeilenargumente verwendet, um den POX-AutoErmittlungsdienst aufzurufen, um den [AutoDiscoverSMTPAddress-Wert](https://msdn.microsoft.com/library/office/dn750991%28v=exchg.150%29.aspx) abzurufen, der der Postfach-GUID zugeordnet ist. 

  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|emailAddress  <br/> |Die Adresse, die von der  `GetMailboxGuidAddress` Methode in Determine the [GUID of the public folder mailbox](#bk_determineguidewsma)zurückgegeben wird.  <br/> |
|-skipSOAP  <br/> |Gibt an, dass POX-AutoErmittlungsanforderungen erforderlich sind.  <br/> |
|-auth authEmailAddress  <br/> |Die E-Mail-Adresse des Postfachbenutzers, die für die Authentifizierung verwendet wird. Sie werden aufgefordert, das Kennwort des Postfachbenutzers einzugeben, wenn Sie das Beispiel ausführen.  <br/> |
   
Die Befehlszeilenargumente sollten z. B. wie folgt aussehen:
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Gibt `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` die Adresse an, die von der **GetMailboxGuidAddress-Methode** zurückgegeben wird, und `sonyaf@contoso.com` der Postfachbenutzer. 
  
Wenn Sie die **Exchange 2013 ausführen: Abrufen von Benutzereinstellungen mithilfe** des AutoErmittlungsbeispiels, sollte die letzte AutoErmittlungsantwort erfolgreich sein und alle Benutzereinstellungen enthalten, die der Postfach-GUID zugeordnet sind. Speichern Sie die **AutoDiscoverSMTPAddress-Benutzereinstellung** lokal, wie Sie dies im nächsten Schritt verwenden. 
  
Wenn Sie Exchange **2013** nicht verwenden möchten: Abrufen von Benutzereinstellungen mit dem AutoErmittlungsbeispiel, können Sie die **AutoDiscoverSMTPAddress-Benutzereinstellung** abrufen, indem Sie [eine Liste der AutoErmittlungsendpunkte generieren](how-to-generate-a-list-of-autodiscover-endpoints.md)und dann die folgende POX-AutoErmittlungsanforderung an jede URL senden, bis Sie eine erfolgreiche Antwort erhalten haben.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>https://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Weitere Informationen zum AutoErmittlungsprozess finden Sie unter [AutoErmittlung für Exchange,](autodiscover-for-exchange.md) [Generieren einer Liste von AutoErmittlungsendpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und Abrufen von [Benutzereinstellungen aus Exchange mithilfe der AutoErmittlung.](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Festlegen der Werte der Header "X-AnchorMailbox" und "X-PublicFolderMailbox"
<a name="bk_setheadervalues"> </a>

Legen Sie unter Verwendung des Werts für die **autoDiscoverSMTPAddress,** die sie in [einer AutoErmittlungsanforderung](#bk_makeautodrequest)erworben hat, die Werte der **Header X-AnchorMailbox** und **X-PublicFolderMailbox** in Ihrer Inhaltsanforderung für öffentliche Ordner fest. 
  
Fügen Sie beispielsweise bei einer AutoDiscoverSMTPAddress von NewPublicFolder@contoso.com die folgenden Header ein, wenn Sie Aufrufe der folgenden Methoden oder Vorgänge ausführen.
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

**Aufrufe öffentlicher Ordner, für die die Header X-AncorMailbox und X-PublicFolder erforderlich sind**

|**EWS Managed API-Methoden**|**EWS-Vorgänge**|
|:-----|:-----|
|[Item.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](https://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](https://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](https://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
Um diese Header mithilfe der verwalteten EWS-API hinzuzufügen, verwenden Sie die [HttpHeaders.Add-Methode.](https://msdn.microsoft.com/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

Der folgende Code zeigt eine [GetFolder-Anforderung,](https://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) bei der der **X-AnchorMailbox-** und **X-PublicFolderMailbox-Header** auf die Werte festgelegt ist, die in den Beispielen in diesem Artikel abgerufen werden. 
  
```XML
POST https://outlook.office365.com/EWS/Exchange.asmx HTTP/1.1
Content-Type: text/xml; charset=utf-8
User-Agent: SoapSender1.0
X-AnchorMailbox: NewPublicFolder@contoso.com
X-PublicFolderMailbox: NewPublicFolder@contoso.com
Authorization: Basic c29ueWFmQGNvbnRvc28xMDAwLm9ubWljcm9zb2Z0LmNvbTpFWENIIzIwMTQ=
Host: outlook.office365.com
Content-Length: 688
Expect: 100-continue
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013_SP1" />
  </soap:Header>
  <soap:Body>
    <m:GetFolder>
      <m:FolderShape>
        <t:BaseShape>AllProperties</t:BaseShape>
      </m:FolderShape>
      <m:FolderIds>
        <t:DistinguishedFolderId Id="publicfoldersroot" />
      </m:FolderIds>
    </m:GetFolder>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Zugriff auf Öffentliche Ordner mit EWS in Exchange](public-folder-access-with-ews-in-exchange.md)    
- [AutoErmittlung für Exchange](autodiscover-for-exchange.md)    
- [Generieren einer Liste mit AutoErmittlungs-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)   
- [Abrufen von Benutzereinstellungen von Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
  
