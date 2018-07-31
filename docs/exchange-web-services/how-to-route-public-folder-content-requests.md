---
title: Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 59d2f05e-90fb-471e-ac06-70becc15b295
description: Alle Anfragen für Öffentliche Ordnerinformationen, die den Inhalt der öffentlichen Ordner müssen an das Postfach für Öffentliche Ordner weitergeleitet werden betreffen, die den Inhalt für den Zielordner enthält. Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die X-AnchorMailbox und X-PublicFolderMailbox-Header auf bestimmte Werte festgelegt.
ms.openlocfilehash: 64fafecb9882b17a3394e54640df78f7aa180343
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354022"
---
# <a name="route-public-folder-content-requests"></a>Weiterleiten von Anforderungen für Inhalte öffentlicher Ordner

Alle Anfragen für Öffentliche Ordnerinformationen, die den Inhalt der öffentlichen Ordner müssen an das Postfach für Öffentliche Ordner weitergeleitet werden betreffen, die den Inhalt für den Zielordner enthält. Um die Anforderungen an dieses Postfach weiterleiten möchten, müssen Sie die **X-AnchorMailbox** und **X-PublicFolderMailbox-** Header auf bestimmte Werte festgelegt. 
  
Die folgende Tabelle enthält eine Übersicht über den Prozess:
  
**Übersicht über die Öffentliche Ordner**

|Kopfzeile|Was muss ich?|Wie erhalte ich es?|
|:-----|:-----|:-----|
|**X-AnchorMailbox** <br/> |1. [die X-AnchorMailbox und X PublicFolderInformation Werte](how-to-route-public-folder-hierarchy-requests.md) für das Postfach für Öffentliche Ordner-Hierarchie.<br/><br/>2. die GUID des Postfachs für Öffentliche Ordner, die den Inhalt von Postfächern enthält, die mit dem AutoErmittlungsdienst gesendet wird.<br/><br/>  Die **AutoDiscoverSMTPAddress** in der Antwort Autodisover wird der Wert der **X-AnchorMailbox** Kopfzeile.  <br/> ![AUFGABEN](media/Ex15_PF_PFContent.png)| 1. verwenden Sie das Codebeispiel in diesem Artikel [implementiert die EWS Managed API](#bk_determineguidewsma). Oder [Verwenden von EWS](#bk_determineguidews) und konvertieren Sie Ihre Ergebnisse, um eine GUID zu erhalten.<br/><br/>2. [eine Anforderung für die AutoErmittlung](#bk_makeautodrequest) , über die GUID und der Domänenname.<br/><br/>3. verwenden Sie den Wert des **AutoDiscoverSMTPAddress** -Elements in der Antwort der AutoErmittlung zum [Auffüllen des Werts der Header](#bk_setheadervalues)zurückgegeben.  <br/> |
|**X-PublicFolderMailbox** <br/> |Ihre Arbeit erfolgt, der X-PublicFolderMailbox-Wert entspricht dem Wert der X-AnchorMailbox!  <br/> |Sie haben bereits es!  <br/> |
   
Nachdem Sie die Werte für die Kopfzeile festgelegt haben, können Sie diese, [Wenn Sie Öffentliche Ordner-inhaltsanforderungen vornehmen](#bk_setheadervalues).
  
Die Schritte in diesem Artikel sind spezifisch für Öffentliche Ordner-inhaltsanforderungen. Um festzustellen, ob es sich bei Ihrer Anforderung einer Hierarchie Öffentlicher Ordner oder Content Anforderung ist, finden Sie unter [Routing für Öffentliche Ordner-Anfragen](public-folder-access-with-ews-in-exchange.md#bk_routing).

<a name="bk_determineguidewsma"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-the-ews-managed-api"></a>Bestimmen Sie die GUID des Postfachs für Öffentliche Ordner mithilfe der EWS Managed API


Um die GUID des Postfachs für Öffentliche Ordner-Inhalt zu bestimmen, verwenden Sie im folgenden Codebeispiel wird, die Folgendes ermöglicht: 
  
- Verwendet die **X-AnchorMailbox** und **X PublicFolderInformation** Header, die Sie von [Öffentliche Ordner-Hierarchie Routinganforderungen](how-to-route-public-folder-hierarchy-requests.md)abgerufen.
    
- Die EWS Managed API [FindFolders](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.folder.findfolders%28v=exchg.80%29.aspx) -Methode aufgerufen, und enthält eine Anforderung für die **PR_REPLICA_LIST** (0x66980102)-Eigenschaft 
    
Der Wert **PR_REPLICA_LIST** identifiziert die Postfach-GUID des Postfachs für Öffentliche Ordner, die den Inhalt für den Ordner verfügt. Die **PR_REPLICA_LIST** -Eigenschaft ist ein Bytearray, aber für dieses Szenario als GUID umgewandelt wird. Die GUID und den Domänennamen werden verkettet, um die Adresse an, die für die AutoErmittlung aufrufen bilden. 
  
In diesem Beispiel wird vorausgesetzt, dass `service` ist das [ExchangeService](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Postfachbenutzer `PFHAnchorHeader` und `PFHMailboxHeader` sind die Werte der **X-AnchorMailbox** und **X-PublicFolderMailbox** Header und Domäne ist der Domänenname wird von verwendet die Mandanten. 
  
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

Wenn Sie die Fehlermeldung "die Anforderung ist fehlgeschlagen. Die zugrunde liegende Verbindung wurde geschlossen: Vertrauensstellung für den geschützten SSL/TLS-Kanal konnte nicht hergestellt werden ", müssen Sie [einen Anruf an eine Rückrufmethode Validierung hinzufügen](how-to-validate-a-server-certificate-for-the-ews-managed-api.md). Einen Platzhalter und einen Kommentar für diese Methode ist im Codebeispiel enthalten.
  
Wenn die Postfach-GUID für die öffentlichen Ordner unter dem Stammverzeichnis der öffentlichen Ordner identisch ist, gibt im Beispiel wird die Adresse zu verwenden, wenn in der Konsole [aufrufen AutoErmittlung](#bk_makeautodrequest) Ausgabe und als Rückgabewert. Wenn die Postfach-GUID nicht für alle öffentlichen Ordner unter dem Stammverzeichnis der Öffentliche Ordner ist, müssen Sie die Adresse, die dem Ordner in Ihrer Anforderung Content zugeordnet, [AutoErmittlung anzufordern](#bk_makeautodrequest) . 

<a name="bk_determineguidews"> </a>

## <a name="determine-the-guid-of-the-public-folder-mailbox-by-using-ews"></a>Bestimmen Sie die GUID des Postfachs für Öffentliche Ordner mithilfe der Exchange-Webdienste

Im folgenden Code wird veranschaulicht abrufen wie den Wert der Eigenschaft **PR_REPLICA_LIST** (0x66980102) mit der EWS [FindFolder](http://msdn.microsoft.com/library/7a9855aa-06cc-45ba-ad2a-645c15b7d031%28Office.15%29.aspx) -Operation. Für das [ExtendedFieldURI](http://msdn.microsoft.com/library/b3c6ea3a-9ead-44b9-9d99-64ecf12bde23%28Office.15%29.aspx) -Element das Attribut **' PropertyTag '** auf den Dezimalwert (26264) der **PR_REPLICA_LIST** -Eigenschaft festgelegt ist, und das Attribut **PropertyType** auf **Binary**festgelegt ist.
  
Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die **FindFolders** -Methode zum [Bestimmen der GUID des Postfachs für Öffentliche Ordner mithilfe der EWS Managed API](#bk_determineguidewsma)verwenden.
  
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

Der Server antwortet auf die Anforderung **FindFolder** mit einer [FindFolderResponse](http://msdn.microsoft.com/library/f5dd813c-9698-4a39-8fca-3a825df365ed%28Office.15%29.aspx) -Meldung, die den Wert der erweiterten Eigenschaft **PR_REPLICA_LIST** enthält. Beachten Sie, dass der Wert der Eigenschaft für die EWS-Antwort mit dem String-Format für eine Base64-codierte Bytearray zurück. Einige Headerwerte in der Antwort werden zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?><s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
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

In den XML-Code, MWVjMmEyMzYtZWQ5My00Zjg4LWI5YzYtMzNlNjNmYTRhYTQ0AA, um den Wert der **PR_REPLICA_LIST** verwenden zurückgegeben ==, um die Postfach-GUID zu ermitteln, muss der Wert in einer GUID in einem Format ähnlich wie in der Wert umgewandelt wird konvertiert werden die [EWS Managed API-Codebeispiel](#bk_determineguidewsma). Die GUID wird dann verkettet wird mit dem Domänennamen, erstellen Sie eine SMTP-Adresse, die in der [Anforderung der AutoErmittlung](#bk_makeautodrequest)enthalten ist.
  
## <a name="make-an-autodiscover-request"></a>Stellen Sie eine autoermittlungsanforderung für die
<a name="bk_makeautodrequest"> </a>

Verwenden Sie die Adresse zurückgegeben, indem die `GetMailboxGuidAddress` Methode, die für die AutoErmittlung aufgerufen. Wir empfehlen die Verwendung der [Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung](http://code.msdn.microsoft.com/exchange/Exchange-2013-Get-user-7e22c86e) Codebeispiel den AutoErmittlungsdienst aufgerufen, da es die AutoErmittlung für Sie vereinfacht. In diesem Codebeispiel verwendet die in der folgenden Tabelle aufgeführten Befehlszeilenargumente zum Aufrufen des POX AutoErmittlungsdiensts zum Abrufen des [AutoDiscoverSMTPAddress](http://msdn.microsoft.com/en-us/library/office/dn750991%28v=exchg.150%29.aspx) -Werts, der die Postfach-GUID zugeordnet. 
  
|**Argument**|**Beschreibung**|
|:-----|:-----|
|emailAddress  <br/> |Die zurückgegebene Adresse der `GetMailboxGuidAddress` -Methode in [Determine die GUID des Postfachs für Öffentliche Ordner](#bk_determineguidewsma).  <br/> |
|-skipSOAP  <br/> |Gibt an, dass POX AutoErmittlung Anforderungen erforderlich sind.  <br/> |
|-Auth authEmailAddress  <br/> |Das des Postfachbenutzers e-Mail-Adresse, die für die Authentifizierung verwendet wird. Sie werden aufgefordert, die beim Ausführen des Beispiels den Postfachbenutzer Kennwort eingeben.  <br/> |
   
Beispielsweise sollte die Befehlszeilenargumente wie folgt aussehen:
  
`1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com -skipSOAP -auth sonyaf@contoso.com`

Wobei `1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com` ist die Adresse, die von der Methode **GetMailboxGuidAddress** zurückgegeben und `sonyaf@contoso.com` der Postfachbenutzer ist. 
  
Beim Ausführen der **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel die letzte AutoErmittlung Antwort erfolgreich und umfassen sollten alle für die Benutzer die Postfach-GUID zugeordnet. Speichern der **AutoDiscoverSMTPAddress** Benutzer lokal festlegen wie Sie, die im nächsten Schritt verwenden. 
  
Alternativ, wenn Sie nicht möchten, verwenden Sie **Exchange 2013: Abrufen von benutzereinstellungen für mit der AutoErmittlung** Beispiel erhalten Sie vom Benutzer **AutoDiscoverSMTPAddress** nach [generieren Sie eine Liste der AutoErmittlung](how-to-generate-a-list-of-autodiscover-endpoints.md)festlegen, und senden Sie dann die folgenden POX Anforderung der AutoErmittlung auf jede URL, bis Sie eine erfolgreiche Antwort erhalten.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Autodiscover xmlns="http://schemas.microsoft.com/exchange/autodiscover/outlook/requestschema/2006">
  <Request>
    <EMailAddress>1ec2a236-ed93-4f88-b9c6-33e63fa4aa44@contoso.com</EMailAddress>
    <AcceptableResponseSchema>http://schemas.microsoft.com/exchange/autodiscover/outlook/responseschema/2006a</AcceptableResponseSchema>
  </Request>
</Autodiscover>
```

Weitere Informationen zu den AutoErmittlung-Prozesses finden Sie unter [AutoErmittlung für Exchange](autodiscover-for-exchange.md), [generieren eine Liste von AutoErmittlung-Endpunkten](how-to-generate-a-list-of-autodiscover-endpoints.md)und [benutzereinstellungen aus Exchange mithilfe der AutoErmittlung erhalten möchten](how-to-get-user-settings-from-exchange-by-using-autodiscover.md).
  
## <a name="set-the-values-of-the-x-anchormailbox-and-x-publicfoldermailbox-headers"></a>Legen Sie die Werte der X-AnchorMailbox und X-PublicFolderMailbox-Header
<a name="bk_setheadervalues"> </a>

Verwenden den Wert für die **AutoDiscoverSMTPAddress** erworben in [AutoErmittlung anzufordern](#bk_makeautodrequest), legen Sie die Werte der **X-AnchorMailbox** und **X-PublicFolderMailbox-** Header in Ihrer öffentlichen Ordner Content-Anforderung. 
  
Ein AutoDiscoverSMTPAddress NewPublicFolder@contoso.com angegeben, beispielsweise die folgenden Kopfzeilen beim Aufrufen der folgenden Methoden oder Vorgänge.
  
`X-AnchorMailbox: NewPublicFolder@contoso.com`<br/>
`X-PublicFolderMailbox: NewPublicFolder@contoso.com`

**Öffentliche Ordner-Anrufe, die die X-AncorMailbox und X-PublicFolder Header erfordern**

|**EWS Managed API-Methoden**|**EWS-Vorgänge**|
|:-----|:-----|
|[Item.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.bind%28v=exchg.80%29.aspx) <br/> [Item.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.update%28v=exchg.80%29.aspx) <br/> [Item.Copy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.copy%28v=exchg.80%29.aspx) <br/> [Item.Move](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.move%28v=exchg.80%29.aspx) <br/> [Item.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.delete%28v=exchg.80%29.aspx) <br/> [Folder.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.bind%28v=exchg.80%29.aspx) <br/> [Folder.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folder.finditems%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/78a52120-f1d0-4ed7-8748-436e554f75b6%28Office.15%29.aspx) <br/> [GetItem](http://msdn.microsoft.com/library/e3590b8b-c2a7-4dad-a014-6360197b68e4%28Office.15%29.aspx) <br/> [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> [CopyItem](http://msdn.microsoft.com/library/bcc68f9e-d511-4c29-bba6-ed535524624a%28Office.15%29.aspx) <br/> [MoveItem](http://msdn.microsoft.com/library/dcf40fa7-7796-4a5c-bf5b-7a509a18d208%28Office.15%29.aspx) <br/> [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) <br/> [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) <br/> |
   
Wenn diese Header mithilfe der EWS Managed API hinzufügen möchten, verwenden Sie die [HttpHeaders.Add](http://msdn.microsoft.com/en-us/library/system.net.http.headers.httpheaders.add%28v=vs.118%29.aspx) -Methode. 
  
```cs
service.HttpHeaders.Add("X-AnchorMailbox", "NewPublicFolder@contoso.com");
service.HttpHeaders.Add("X-PublicFolderMailbox", "NewPublicFolder@contoso.com");
```

Der folgende Code zeigt eine [GetFolder](http://msdn.microsoft.com/library/355bcf93-dc71-4493-b177-622afac5fdb9%28Office.15%29.aspx) -Anforderung mit dem **X-AnchorMailbox** und **X-PublicFolderMailbox** -Header auf die Werte in den Beispielen in diesem Artikel abgerufen festgelegt. 
  
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
- [Abrufen von benutzereinstellungen aus Exchange mithilfe der AutoErmittlung](how-to-get-user-settings-from-exchange-by-using-autodiscover.md)
    

