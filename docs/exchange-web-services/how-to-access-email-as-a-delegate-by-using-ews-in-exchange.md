---
title: Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Informationen zum Zugreifen auf e-Mails als Stellvertretung mithilfe der verwaltete EWS-API oder EWS in Exchange.
ms.openlocfilehash: 0c26f69042c568fe7d877778c7d8f1e689e5b372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528286"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a>Zugreifen auf E-Mails als Stellvertretung mithilfe der EWS in Exchange

Informationen zum Zugreifen auf e-Mails als Stellvertretung mithilfe der verwaltete EWS-API oder EWS in Exchange.
  
Sie können die verwaltete EWS-API oder EWS verwenden, um einem Benutzer Stellvertretungszugriff auf den Posteingangsordner eines Postfachbesitzers zu gewähren. Der Stellvertreter kann dann Besprechungsanfragen im Auftrag des Postfachbesitzers erstellen, nach e-Mails suchen und e-Mails aus dem Posteingang-Ordner des Postfachbesitzers abrufen, aktualisieren und löschen, je nach den Berechtigungen.
  
Als Stellvertretung verwenden Sie dieselben Methoden und Vorgänge, um auf den Posteingangsordner eines Postfachbesitzers zuzugreifen, den Sie für den Zugriff auf einen Posteingangsordner ohne Stellvertretungszugriff verwenden. Der Hauptunterschied besteht darin, dass Sie [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicit) zum Suchen oder Erstellen eines e-Mail-Elements verwenden müssen, und nachdem Sie die Element-ID identifiziert haben, können Sie [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) zum Abrufen, aktualisieren oder Löschen des Elements verwenden. 
  
**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für den Zugriff auf e-Mails als Stellvertretung**

|**Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode...**|**Verwenden Sie diesen EWS-Vorgang...**|
|:-----|:-----|:-----|
|Erstellen und Senden einer e-Mail als Stellvertretung  <br/> |[Email Message. Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner "Entwürfe" des Postfachbesitzers bereitstellt  <br/> [Email Message. SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) , wobei der [Folder](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Ordner "Gesendete Elemente" des Postfachbesitzers bereitstellt  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> [SendItem](https://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> |
|Erstellen mehrerer e-Mail-Nachrichten als Stellvertretung  <br/> |[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Posteingangsordner des Postfachbesitzers ermöglicht  <br/> |[CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> |
|Suchen nach oder Suchen einer e-Mail als Stellvertretung  <br/> |[Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , wobei der **Folder** -Parameter den [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Posteingangsordner des Postfachbesitzers ermöglicht  <br/> |[FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , wobei das [Mailbox](https://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) [-Element](https://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) die e-Mail-Post Fach Besitzerin angibt  <br/> |
|Abrufen einer e-Mail als Stellvertretung  <br/> |[EmailMessage.Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren einer e-Mail als Stellvertretung  <br/> |[Email Message. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Email Message. Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen einer e-Mail als Stellvertretung  <br/> |[Email Message. Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Email Message. Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Beachten Sie beim Arbeiten mit e-Mails als Stellvertretung Folgendes:
  
- Wenn eine Stellvertretung nur mit Besprechungsanfragen und-Antworten arbeiten muss, benötigt die Stellvertretung keinen Zugriff auf den Ordner Posteingang. Weitere Informationen finden Sie unter [erforderliche Aufgaben für den Zugriff auf Kalender als Stellvertreter](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).
    
- Wenn ein Empfänger eine Nachricht empfängt, die im Auftrag eines Postfachbesitzers gesendet wurde, wird der Absender als " *Stellvertreter* im Auftrag des *Postfachbesitzers* " angezeigt. 
    
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist Primary@contoso.com der Postfachbesitzer. 
  
## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben
<a name="bk_prereq"> </a>

Bevor ein Benutzer als Stellvertreter auf den Posteingangsordner des Postfachbesitzers zugreifen kann, muss der Benutzer [als Stellvertreter mit Berechtigungen](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) für den Posteingang-Ordner des Postfachbesitzers hinzugefügt werden. 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen und Senden einer e-Mail als Stellvertretung mithilfe der verwaltete EWS-API
<a name="bk_createewsma"> </a>

Mit dem verwaltete EWS-API können Sie das Dienstobjekt für den Stellvertreter verwenden, um e-Mails im Auftrag des Postfachbesitzers zu erstellen und zu senden. In diesem Beispiel wird gezeigt, wie Sie die [Save](https://msdn.microsoft.com/library/dd635209%28v=exchg.80%29.aspx) -Methode verwenden, um die Nachricht im Ordner "Entwürfe" des Postfachbesitzers zu speichern, und dann die [SendAndSaveCopy](https://msdn.microsoft.com/library/dd634248%28v=exchg.80%29.aspx) -Methode zum Senden der e-Mail und Speichern der Nachricht im Ordner "Gesendete Elemente" des Postfachbesitzers. 
  
In diesem Beispiel wird davon ausgegangen, dass **Service** ein gültiges [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für die Stellvertretung ist und dass der Stellvertretung die [entsprechenden Berechtigungen für den Ordner" Posteingang "," Entwürfe "und" Gesendete Elemente "des Postfachbesitzers](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)erteilt wurden.
  
```cs
public static void DelegateAccessCreateEmail(ExchangeService service)
{
    // Create an email message and provide it with connection 
    // configuration information by using an ExchangeService 
    // object named service.
    EmailMessage message = new EmailMessage(service);
    // Set properties on the email message.
    message.Subject = "Company Soccer Team";
    message.Body = "Are you interested in joining?";
    message.ToRecipients.Add("sadie@contoso.com");
    // Save the email to the mailbox owner's Drafts folder.
    // This method call results in a CreateItem call to EWS.
    // The FolderId parameter contains the context for the 
    // mailbox owner's Inbox folder. Any additional actions 
    // taken on this message will be performed in the mailbox 
    // owner's mailbox. 
    message.Save(new FolderId(WellKnownFolderName.Drafts, new Mailbox("primary@contoso.com")));
    // Send the email and save the message in the mailbox owner's 
    // Sent Items folder.
    // This method call results in a SendItem call to EWS.
    message.SendAndSaveCopy(new FolderId(WellKnownFolderName.SentItems, new Mailbox("primary@contoso.com")));
    Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" 
    + message.ToRecipients[0] + "' and saved in the Sent Items folder of the mailbox owner.");
}
```

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a>Erstellen und Senden einer e-Mail als Stellvertretung mithilfe von EWS
<a name="bk_createews"> </a>

EWS ermöglicht die Verwendung des Dienstobjekts für den Stellvertreter Benutzer zum Erstellen und Senden von e-Mails im Auftrag des Postfachbesitzers. In diesem Beispiel wird gezeigt, wie Sie mithilfe des [CreateItem](https://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgangs eine e-Mail und den [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang erstellen, um die Uhrzeit zu senden und im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern. 
  
Dies ist auch die erste XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die **Save** -Methode zum [Erstellen und Senden einer e-Mail](#bk_createewsma)verwenden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die e-Mail erstellt und erfolgreich gespeichert wurde. Die Antwort enthält auch die Element-ID der neu erstellten e-Mail.
  
Der **ItemID** -Wert wurde zur Lesbarkeit gekürzt. 
  
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
  <s:Body>
    <m:CreateItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:CreateItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="iNRaAAA="
                        ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
            </t:Message>
          </m:Items>
        </m:CreateItemResponseMessage>
      </m:ResponseMessages>
    </m:CreateItemResponse>
  </s:Body>
</s:Envelope>
```

Verwenden Sie als nächstes den **SendItem** -Vorgang, um die Nachricht im Auftrag des Postfachbesitzers zu senden und im Ordner "Gesendete Elemente" des Postfachbesitzers zu speichern. 
  
Der **ItemID** -Wert wurde zur Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="iNRaAAA="
                  ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQPU" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **SendItem** -Anforderung mit einer [SendItemResponse](https://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die e-Mail erfolgreich an den Ordner "Gesendete Elemente" des Postfachbesitzers gesendet und gespeichert wurde.
  
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
  <s:Body>
    <m:SendItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Suchen nach einer e-Mail als Stellvertretung mithilfe der verwaltete EWS-API
<a name="bk_searchewsma"> </a>

Um nach einer e-Mail zu suchen, müssen Sie eine der [Datei "ExchangeService. FindItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) -Methoden verwenden, die einen [foldercode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält, sodass Sie den Posteingangsordner des Postfachbesitzers angeben können. 
  
```cs
static void DelegateAccessSearchEmailWithFilter(ExchangeService service)
{
    // Limit the result set to 10 items.
    ItemView view = new ItemView(10);
    // Define the search filter.
    SearchFilter.ContainsSubstring filter = new SearchFilter.ContainsSubstring(ItemSchema.Subject, 
        "soccer", ContainmentMode.Substring, ComparisonMode.IgnoreCase);
    view.PropertySet = new PropertySet(ItemSchema.Subject,
                                       ItemSchema.DateTimeReceived,
                                       EmailMessageSchema.IsRead);
    // Item searches do not support deep traversal.
    view.Traversal = ItemTraversal.Shallow;
    // Sorting.
    view.OrderBy.Add(ItemSchema.DateTimeReceived, SortDirection.Descending);
    try
    {
        // Call FindItems to find matching Inbox items. 
        // The parameters of FindItems must denote the mailbox owner,
        // mailbox, and Inbox folder.
        // This call results in a FindItem call to EWS.
        FindItemsResults<Item> results = service.FindItems(new 
            FolderId(WellKnownFolderName.Inbox, "primary@contoso.com"), 
            filter, view);
        foreach (Item item in results.Items)
        {
            Console.WriteLine("Subject: {0}", item.Subject);
            Console.WriteLine("Id: {0}", item.Id.ToString());
            if (item is EmailMessage)
            {
                EmailMessage message = item as EmailMessage;
                Console.WriteLine("Read: {0}", message.IsRead.ToString());
            }
        }
    }
    catch (Exception ex)
    {
        Console.WriteLine("Exception while enumerating results: {0}", ex.Message);
    }
}
```

Nachdem der **FindItems** -Aufruf eine Antwort mit einer ID zurückgibt, können Sie diese e-Mails abrufen, aktualisieren oder löschen, indem Sie die ID und den [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) verwenden – und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben. 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a>Suchen nach einer e-Mail als Stellvertretung mithilfe von EWS
<a name="bk_searchews"> </a>

Mit EWS können Sie das Dienstobjekt für den Stellvertreter-Benutzer verwenden, um nach e-Mails zu suchen, die eine Reihe von Suchkriterien erfüllen. In diesem Beispiel wird gezeigt, wie Sie mithilfe des [FindItem](https://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) -Vorgangs Nachrichten im Posteingangsordner des Besitzers suchen, die das Wort "Soccer" im Betreff enthalten. 
  
Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie [nach einer e-Mail suchen](#bk_searchewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="https://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version=" Exchange2007_SP1" />
  </soap:Header>
  <soap:Body>
    <m:FindItem Traversal="Shallow">
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
          <t:FieldURI FieldURI="message:IsRead" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:Restriction>
        <t:Contains ContainmentMode="Substring"
                    ContainmentComparison="IgnoreCase">
          <t:FieldURI FieldURI="item:Subject" />
          <t:Constant Value="soccer" />
        </t:Contains>
      </m:Restriction>
      <m:SortOrder>
        <t:FieldOrder Order="Descending">
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:FieldOrder>
      </m:SortOrder>
      <m:ParentFolderIds>
        <t:DistinguishedFolderId Id="inbox">
          <t:Mailbox>
            <t:EmailAddress>primary@contoso.com</t:EmailAddress>
          </t:Mailbox>
        </t:DistinguishedFolderId>
      </m:ParentFolderIds>
    </m:FindItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **FindItem** -Anforderung mit einer [FindItemResponse](https://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Suche erfolgreich abgeschlossen wurde. Die Antwort enthält ein [Message](https://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) -Element für alle e-Mails, die die Suchkriterien erfüllen. In diesem Fall wird nur eine e-Mail gefunden. 
  
Der Wert des [ItemID](https://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) -Elements wurde zur Lesbarkeit gekürzt. 
  
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
  <s:Body>
    <m:FindItemResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:FindItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:RootFolder IndexedPagingOffset="1"
                        TotalItemsInView="1"
                        IncludesLastItemInRange="true">
            <t:Items>
              <t:Message>
                <t:ItemId Id="iNwoAAA="
                          ChangeKey="CQAAABYAAADOilbYa8KaT7ZgMoTz2P+hAAABiQuu" />
                <t:Subject>Soccer team</t:Subject>
                <t:DateTimeReceived>2014-03-10T06:16:55Z</t:DateTimeReceived>
                <t:IsRead>false</t:IsRead>
              </t:Message>
            </t:Items>
          </m:RootFolder>
        </m:FindItemResponseMessage>
      </m:ResponseMessages>
    </m:FindItemResponse>
  </s:Body>
</s:Envelope>
```

Da Sie nun die **ItemID** für die e-Mail haben, die Ihre Kriterien erfüllt, können Sie diese e-Mails mithilfe des **ItemID** -und [impliziten Zugriffs](delegate-access-and-ews-in-exchange.md#bk_implicit) abrufen, aktualisieren oder löschen, und Sie müssen die SMTP-Adresse des Postfachbesitzers nicht angeben. 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a>Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe der verwaltete EWS-API
<a name="bk_geteswma"> </a>

Sie können die verwaltete EWS-API verwenden, um eine e-Mail auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie diese Aktionen ausgeführt werden, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das **Datei "ExchangeService** -Objekt für den Stellvertreter-Benutzer ist. Die im **Bindungs** Methodenaufruf enthaltene Element-ID identifiziert das Element im Postfachspeicher im Posteingangsordner des Postfachbesitzers eindeutig. 
  
**Tabelle 2. Verwaltete EWS-API Methoden, die mit e-Mail als Stellvertretung arbeiten**

|**Aufgabe**|**EWS Managed API-Methode**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen einer e-Mail  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der verwaltete EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Aktualisieren einer e-Mail  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Update](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe der verwaltete EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|Löschen einer e-Mail  <br/> |[Bind](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Delete](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[Löschen eines Elements mithilfe der verwaltete EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a>Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe von EWS
<a name="bk_getews"> </a>

Sie können die verwaltete EWS-API verwenden, um eine e-Mail auf die gleiche Weise abzurufen, zu aktualisieren oder zu löschen, wie diese Aktionen ausgeführt werden, wenn Sie keinen Stellvertretungszugriff verwenden. Der einzige Unterschied besteht darin, dass das Dienstobjekt für den Stellvertreter Benutzer ist. Die in der **GetItem** -Anforderung enthaltene Element-ID identifiziert das Element im Postfachspeicher im Posteingangsordner des Postfachbesitzers eindeutig. 
  
**Tabelle 3. EWS-Vorgänge für das Arbeiten mit e-Mail als Stellvertretung**

|**Task**|**EWS-Vorgang**|**Codebeispiel**|
|:-----|:-----|:-----|
|Abrufen einer e-Mail  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Aktualisieren einer e-Mail  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|Löschen einer e-Mail  <br/> |[GetItem](https://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) , gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[Löschen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)    
- [Hinzufügen und Entfernen von Delegaten mithilfe der EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Festlegen von Ordnerberechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    

