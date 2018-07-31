---
title: Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: a8123604-c7c0-405d-a0ed-7a9b4a431bfd
description: Erfahren Sie, wie e-Mail als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 23dd35f95b1303ff643e3760aa408e308725cb12
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21354036"
---
# <a name="access-email-as-a-delegate-by-using-ews-in-exchange"></a>Access-e-Mail eine Stellvertretung mithilfe der EWS in Exchange

Erfahren Sie, wie e-Mail als Stellvertreter zugreifen, indem Sie die EWS Managed API oder EWS in Exchange.
  
Sie können die EWS Managed API verwenden oder EWS so erteilen Sie einen Benutzer delegieren des Zugriffs auf eine Postfachbesitzer Posteingangsordner. Die Stellvertretung kann Klicken Sie dann Erstellen von Besprechungsanfragen im Auftrag des Postfachbesitzers, für e-Mails, suchen und abrufen, aktualisieren, und löschen e-Mail aus dem Ordner Posteingang des Postfachbesitzers abhängig von ihren Berechtigungen.
  
Als Stellvertretung verwenden Sie die gleichen Methoden und Vorgänge des Postfachbesitzers zum Zugreifen auf Posteingang, mit denen Sie einen Posteingangsordner ohne Stellvertretungszugriff zugreifen. Der Hauptunterschied ist, dass Sie mithilfe von [expliziten Access](delegate-access-and-ews-in-exchange.md#bk_explicit) suchen oder erstellen ein e-Mail-Element, und klicken Sie dann, nachdem Sie die Element-ID identifiziert haben, können [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) erhalten möchten, aktualisieren und Löschen des Elements. 
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für den Zugriff auf e-Mail als Stellvertreter**

|**Aktion**|**Verwenden Sie diese Methode EWS Managed API...**|**Verwenden Sie diese Operation EWS...**|
|:-----|:-----|:-----|
|Erstellen und Senden einer e-Mails als Stellvertreter  <br/> |[EmailMessage.Save](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) , in dem der [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Ordner "Entwürfe" enthält  <br/> [EmailMessage.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) , in dem der Parameter [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer gesendete Objekte Ordner enthält  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> [Den SendItem](http://msdn.microsoft.com/library/a966da19-b05a-4504-ac98-91acc1667b9a%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Erstellen Sie mehrere e-Mail-Nachrichten als Stellvertreter  <br/> |[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Posteingangsordner enthält  <br/> |[CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Suchen Sie nach oder suchen Sie nach einer e-Mail als Stellvertreter  <br/> |[ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , in dem der Parameter **FolderId** [expliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_explicitewsma) auf den Postfachbesitzer Posteingangsordner enthält  <br/> |[FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) , in dem das [Postfach](http://msdn.microsoft.com/library/befc70fd-51cb-4258-884c-80c9050f0e82%28Office.15%29.aspx) -Element gibt an, die [EmailAddress](http://msdn.microsoft.com/library/922c8b21-04a9-4229-b48c-187c3095422e%28Office.15%29.aspx) des Postfachbesitzers  <br/> |
|Abrufen einer e-Mails als Stellvertreter  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |
|Aktualisieren einer e-Mails als Stellvertreter  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [EmailMessage.Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen Sie eine e-Mail als Stellvertreter  <br/> |[EmailMessage.Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [EmailMessage.Delete](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |
   
Beachten Sie Folgendes im Hinterkopf beim Arbeiten mit e-Mail-Nachrichten als Stellvertreter:
  
- Wenn nur eine Stellvertretung Besprechungsanfragen und-Antworten entwickelt muss, ist die Stellvertretung Zugriff auf den Ordner Posteingang nicht erforderlich. Weitere Informationen finden Sie unter [erforderlichen Aufgaben für den Zugriff auf Kalender als Stellvertreter](how-to-access-a-calendar-as-a-delegate-by-using-ews-in-exchange.md#bk_prereq).
    
- Wenn ein Empfänger eine Nachricht, die im Namen einer Postfachbesitzer gesendet wurde empfängt, ist der Absender " *Delegaten* im Namen *des Besitzers des Zielpostfachs* ." 
    
> [!NOTE]
> In den Codebeispielen in diesem Artikel ist primary@contoso.com der Postfachbesitzer. 
  
## <a name="prerequisite-tasks"></a>Erforderliche Aufgaben
<a name="bk_prereq"> </a>

Bevor ein Benutzer des Postfachbesitzers Posteingangsordner als Stellvertreter zugreifen kann, muss der Benutzer des Postfachbesitzers Posteingangsordner [als Stellvertreter mit Berechtigungen hinzugefügt](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md) . 
  
## <a name="create-and-send-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Erstellen und Senden einer e-Mails eine Stellvertretung mithilfe der EWS Managed API
<a name="bk_createewsma"> </a>

Die EWS Managed API können Sie das Objekt für den Benutzer Delegaten erstellen und Senden von e-Mails im Auftrag des Postfachbesitzers verwenden. In diesem Beispiel wird gezeigt, wie die [Speichern](http://msdn.microsoft.com/en-us/library/dd635209%28v=exchg.80%29.aspx) -Methode, um die Nachricht im Ordner "Entwürfe" des Postfachbesitzers speichern, und klicken Sie dann die [SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/dd634248%28v=exchg.80%29.aspx) -Methode, um die e-Mail-Nachricht senden, und speichern Sie die Nachricht im Ordner des Postfachbesitzers-gesendete Objekte verwendet. 
  
In diesem Beispiel wird davon ausgegangen, die **Service** ist ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objekt für den Delegaten und, die der Stellvertreter die [entsprechenden Berechtigungen für den Postfachbesitzer Posteingang, Entwürfe und gesendete Objekte Ordner](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)gewährt wurde.
  
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

## <a name="create-and-send-an-email-as-a-delegate-by-using-ews"></a>Erstellen und Senden einer e-Mails eine Stellvertretung mithilfe der Exchange-Webdienste
<a name="bk_createews"> </a>

Exchange-Webdienste können Sie das Objekt für den Benutzer Delegaten erstellen und Senden von e-Mails im Auftrag des Postfachbesitzers verwenden. Dieses Beispiel zeigt, wie Sie den [CreateItem](http://msdn.microsoft.com/library/aa4a7c94-f668-4bd2-8079-c855f6ab17e1%28Office.15%29.aspx) -Vorgang verwenden, um eine e-Mail-Nachricht und [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang zum Senden der Zeit und speichern Sie sie im Ordner des Postfachbesitzers-gesendete Objekte erstellen. 
  
Dies ist auch der erste XML-Anforderung, die die EWS Managed API sendet, wenn Sie die **Speichern** -Methode zum [Erstellen und senden eine e-Mail](#bk_createewsma)verwenden.
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die e-Mail-Nachricht erstellt und erfolgreich gespeichert wurde. Die Antwort enthält auch die Element-ID der neu erstellten e-Mail.
  
Der Wert **ItemId** wurde zur besseren Lesbarkeit gekürzt. 
  
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
  <s:Body>
    <m:CreateItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                          xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Verwenden Sie im nächsten Schritt **den SendItem** -Vorgang so senden Sie die Nachricht im Auftrag des Postfachbesitzers und speichern sie im Ordner des Postfachbesitzers-gesendete Objekte. 
  
Der Wert **ItemId** wurde zur besseren Lesbarkeit gekürzt. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **den SendItem** mit einer [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die e-Mail-Nachricht gesendet und gesendete Elemente im Ordner des Postfachbesitzers gespeichert wurde erfolgreich.
  
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
  <s:Body>
    <m:SendItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:SendItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:SendItemResponseMessage>
      </m:ResponseMessages>
    </m:SendItemResponse>
  </s:Body>
</s:Envelope>
```

## <a name="search-for-an-email-as-a-delegate-by-using-the-ews-managed-api"></a>Suchen Sie nach einer e-Mail eine Stellvertretung mithilfe der EWS Managed API
<a name="bk_searchewsma"> </a>

Um eine e-Mail-Nachricht zu suchen, müssen Sie eine der Methoden [ExchangeService.FindItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.finditems%28v=exchg.80%29.aspx) , die einen [FolderId](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.folderid%28v=exchg.80%29.aspx) -Parameter enthält verwenden, damit Sie den Postfachbesitzer Posteingangsordner angeben können. 
  
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

Nach Beendigung des **FindItems** Aufrufs eine Antwort mit einer ID, müssen Sie erhalten können, aktualisieren oder löschen, die per e-Mail mit der ID und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie nicht die SMTP-Adresse des Postfachbesitzers angeben. 
  
## <a name="search-for-an-email-as-a-delegate-by-using-ews"></a>Suchen Sie nach einer e-Mail eine Stellvertretung mithilfe der Exchange-Webdienste
<a name="bk_searchews"> </a>

EWS können Sie mit dem Dienstobjekt für den Benutzer Delegaten-e-Mails zu suchen, die einen Satz von Suchkriterien erfüllen. In diesem Beispiel wird veranschaulicht, wie Sie den Vorgang [FindItem](http://msdn.microsoft.com/library/ebad6aae-16e7-44de-ae63-a95b24539729%28Office.15%29.aspx) zum Suchen von Nachrichten in den Besitzer Posteingangsordner, die das Wort "Fußball" im Betreff enthalten. 
  
Dies ist auch, dass die EWS Managed API, wenn gesendet die XML-Anfrage [Suchen nach einer e-Mail](#bk_searchewsma).
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
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

Der Server antwortet auf die Anforderung **FindItem** mit einer [FindItemResponse](http://msdn.microsoft.com/library/c8b316df-d4ab-49b8-96d4-8e9a016730ef%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Element **noError zurück**, das anzeigt, dass die Suche erfolgreich abgeschlossen wurde. Die Antwort enthält das Element für eine [Nachricht](http://msdn.microsoft.com/library/2400b33c-43b2-4fc2-b6fb-275a99e0e810%28Office.15%29.aspx) für alle e-Mails, die die Suchkriterien erfüllen. In diesem Fall wird nur eine e-Mail-gefunden. 
  
Der Wert des Elements [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) wurde zur besseren Lesbarkeit gekürzt. 
  
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
  <s:Body>
    <m:FindItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                        xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
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

Nun, da Sie die **ItemId** für die e-Mail-Nachricht verfügen, die die Kriterien erfüllt, müssen Sie erhalten können, Update- oder Delete, die mithilfe der **ItemId** und [impliziten Zugriff](delegate-access-and-ews-in-exchange.md#bk_implicit) – und Sie per e-Mail nicht die SMTP-Adresse des Postfachbesitzers angeben. 
  
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-the-ews-managed-api"></a>Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe der EWS Managed API
<a name="bk_geteswma"> </a>

Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen einer e-Mails in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden. Der einzige Unterschied ist, dass das **ExchangeService** -Objekt für den Benutzer Delegat ist. Die Element-ID im Methodenaufruf **binden** enthalten sind, eindeutig identifiziert das Element im Postfachspeicher im Posteingang des Postfachbesitzers. 
  
**In Tabelle 2. Arbeiten mit e-Mail als Stellvertreter EWS Managed API-Methoden**

|**Aufgabe**|**EWS Managed API-Methode**|**Code example**|
|:-----|:-----|:-----|
|E-Mail senden  <br/> |[Bind](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) <br/> |[Abrufen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getewsma) <br/> |
|Aktualisieren einer e-Mails  <br/> |[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Update](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.update%28v=exchg.80%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateewsma) <br/> |
|Löschen einer e-Mails  <br/> |[Binden von](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) gefolgt von [Löschen](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.delete%28v=exchg.80%29.aspx) <br/> |[Löschen eines Elements mithilfe der verwalteten EWS-API](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteewsma) <br/> |
   
## <a name="get-update-or-delete-email-items-as-a-delegate-by-using-ews"></a>Abrufen, aktualisieren oder Löschen von e-Mail-Elementen als Stellvertretung mithilfe der Exchange-Webdienste
<a name="bk_getews"> </a>

Die EWS Managed API können Sie abrufen, aktualisieren oder Löschen einer e-Mails in die gleiche Weise, die Sie diese Aktionen ausführen, wenn Sie Stellvertretungszugriff nicht verwenden. Der einzige Unterschied ist, dass das Objekt für den Benutzer Delegat ist. Die Element-ID, enthalten in der **GetItem** -Anforderung eindeutig identifiziert das Element im Postfachspeicher im Posteingang des Postfachbesitzers. 
  
**Tabelle 3. EWS-Vorgänge für das Arbeiten mit e-Mail als Stellvertreter**

|**Aufgabe**|**EWS-Vorgang**|**Code example**|
|:-----|:-----|:-----|
|E-Mail senden  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) <br/> |[Abrufen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_getews) <br/> |
|Aktualisieren einer e-Mails  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |[Aktualisieren eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_updateews) <br/> |
|Löschen einer e-Mails  <br/> |[GetItem](http://msdn.microsoft.com/library/a41c29c9-c4e6-4aa4-8e28-ccb0b478fee8%28Office.15%29.aspx) gefolgt von [DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |[Löschen eines Elements mithilfe von EWS](how-to-work-with-exchange-mailbox-items-by-using-ews-in-exchange.md#bk_deleteews) <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Stellvertretungszugriff und EWS in Exchange](delegate-access-and-ews-in-exchange.md)    
- [Hinzufügen und Entfernen von Stellvertretungen mithilfe von EWS in Exchange](how-to-add-and-remove-delegates-by-using-ews-in-exchange.md)    
- [Legen Sie Berechtigungen für einen anderen Benutzer mithilfe der EWS in Exchange](how-to-set-folder-permissions-for-another-user-by-using-ews-in-exchange.md)    
- [Kalender und EWS in Exchange](calendars-and-ews-in-exchange.md)
    

