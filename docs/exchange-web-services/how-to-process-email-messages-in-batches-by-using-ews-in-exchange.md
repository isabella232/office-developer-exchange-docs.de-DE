---
title: Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.assetid: 96390f92-cab1-4de6-9ec2-a55678fc20af
description: In diesem Artikel erfahren Sie, wie Sie Batches von e-Mail-Nachrichten in einem einzigen Aufruf mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen, abrufen, aktualisieren und löschen können.
localization_priority: Priority
ms.openlocfilehash: 2592076c9c5b57356d96872f006dd7b0abfc328a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527775"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a>Verarbeiten von E-Mails in Batches mithilfe von EWS in Exchange

In diesem Artikel erfahren Sie, wie Sie Batches von e-Mail-Nachrichten in einem einzigen Aufruf mithilfe der verwaltete EWS-API oder EWS in Exchange erstellen, abrufen, aktualisieren und löschen können.

Sie können die verwaltete EWS-API oder EWS verwenden, um mit Batches von e-Mail-Nachrichten zu arbeiten, um die Anzahl der Anrufe zu reduzieren, die ein Client an einen Exchange-Server tätigt. Wenn Sie die verwaltete EWS-API zum Erstellen, abrufen, aktualisieren, löschen und Senden von Nachrichten in Batches verwenden, verwenden Sie [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Objektmethoden, während Sie bei der Arbeit mit einzelnen e-Mail-Nachrichten [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objektmethoden verwenden. Wenn Sie EWS verwenden, verwenden Sie dieselben Vorgänge, um sowohl mit einzelnen als auch mit Batches von e-Mail-Nachrichten zu arbeiten.

**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge zum Arbeiten mit Batches von e-Mail-Nachrichten**

|**Gewünschte Aktion**|**Verwenden Sie diese verwaltete EWS-API-Methode**|**Zu verwendender EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen von e-Mail-Nachrichten in Batches  <br/> |[Datei "ExchangeService. CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Abrufen von e-Mail-Nachrichten in Batches  <br/> |[Datei "ExchangeService. BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Aktualisieren von e-Mail-Nachrichten in Batches  <br/> |[Datei "ExchangeService. Update Items](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](https://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen von e-Mail-Nachrichten in Batches  <br/> |[Datei "ExchangeService. DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](../web-service-reference/deleteitem-operation.md) <br/> |

In diesem Artikel erfahren Sie, wie Sie grundlegende Aufgaben für Batches von e-Mail-Nachrichten mithilfe der verwaltete EWS-API oder EWS ausführen.

## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a>Erstellen von e-Mail-Nachrichten in Batches mithilfe der verwaltete EWS-API
<a name="bk_createewsma"> </a>

Sie können Nachrichten in Batches mithilfe der verwaltete EWS-API **CreateItems** -Methode erstellen, wie im folgenden Beispiel gezeigt. In diesem Beispiel werden drei [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekte lokal erstellt, jede Nachricht wird einer Auflistung hinzugefügt, und anschließend wird die **CreateItems** -Methode für die Auflistung von Nachrichten aufgerufen.

In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.

```cs
public static Collection<ItemId> CreateDraftEmailInBatch(ExchangeService service)
{
    // These are unsaved local instances of an EmailMessage object.
    // Despite the required parameter of an ExchangeService object (service), no call
    // to an Exchange server is made when the objects are instantiated.
    // A call to the Exchange server is made when the service.CreateItems() method is called.
    EmailMessage message1 = new EmailMessage(service);
    EmailMessage message2 = new EmailMessage(service);
    EmailMessage message3 = new EmailMessage(service);
    // Set the properties on the first message.
    message1.Subject = "Project priorities";
    message1.Body = "(1) Buy pizza, (2) Eat pizza";
    message1.ToRecipients.Add("sadie@contoso.com");
    // Set the properties on the second message.
    message2.Subject = "Company Soccer Team";
    message2.Body = "Are you interested in joining?";
    message2.ToRecipients.Add("magdalena@contoso.com");
    // Set the properties on the third message.
    message3.Subject = "Code Blast";
    message3.Body = "Are you interested in getting together to finish the methods for the ContosoLive project?";
    message3.ToRecipients.Add("mack@contoso.com");
    // Add the EmailMessage objects to a collection.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>() { message1, message2, message3 };
    // Create the batch of email messages on the server.
    // This method call results in an CreateItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.Drafts, MessageDisposition.SaveOnly, null);
    // Instantiate a collection of item IDs to populate from the values that are returned by the Exchange server.
    Collection<ItemId> itemIds = new Collection<ItemId>();
    // Collect the item IDs from the created email messages.
    foreach (EmailMessage message in messageItems)
    {
        try
        {
            itemIds.Add(message.Id);
            Console.WriteLine("Email message '{0}' created successfully.", message.Subject);
        }
        catch (Exception ex)
        {
            // Print out the exception and the last eight characters of the item ID.
            Console.WriteLine("Exception while creating message {0}: {1}", message.Id.ToString().Substring(144), ex.Message);
        }
    }
    // Check for success of the CreateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
            Console.WriteLine("All locally created messages were successfully saved to the Drafts folder.");
            Console.WriteLine("\r\n");
    }

    // If the method did not return success, print the result message for each email.
    else
    {
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            // Print out the result and the last eight characters of the item ID.
            Console.WriteLine("Result (message {0}), id {1}: {2}", counter, itemIds[counter - 1].ToString().Substring(144), resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            Console.WriteLine("\r\n");
            counter++;
        }
    }
    return itemIds;
}
```

Beachten Sie, dass im Beispiel die Nachrichten nur im Ordner "Entwürfe" gespeichert werden. die Nachrichten werden nicht gesendet. Weitere Informationen zum Senden von Nachrichten finden Sie unter [Senden von e-Mail-Nachrichten in Batches mithilfe der verwaltete EWS-API](#bk_sendewsma).

## <a name="create-email-messages-in-batches-by-using-ews"></a>Erstellen von e-Mail-Nachrichten in Batches mithilfe von EWS
<a name="bk_createews"> </a>

Sie können e-Mail-Nachrichten in Batches mithilfe des [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -EWS-Vorgangs erstellen, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [e-Mail-Nachrichten in Batches zu erstellen](#bk_createewsma).

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
    <m:CreateItem MessageDisposition="SaveOnly">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Project priorities</t:Subject>
          <t:Body BodyType="HTML">(1) Buy pizza, (2) Eat pizza</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>magdalena@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
        <t:Message>
          <t:Subject>Code Blast</t:Subject>
          <t:Body BodyType="HTML">Are you interested in getting together to finish the methods for the ContosoLive project?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>mack@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die einen [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert von **noError** für jede der neuen Nachrichten enthält, was darauf hinweist, dass jede e-Mail erstellt und erfolgreich gespeichert wurde.

Beachten Sie, dass im Beispiel die Nachrichten nur im Ordner "Entwürfe" gespeichert werden. die Nachrichten werden nicht gesendet. Weitere Informationen zum Senden von Nachrichten finden Sie unter [Senden von e-Mail-Nachrichten in Batches mithilfe von EWS](#bk_sendews).

## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a>Senden von e-Mail-Nachrichten in Batches mithilfe der verwaltete EWS-API
<a name="bk_sendewsma"> </a>

Sie verwenden denselben Code zum Senden von e-Mail-Nachrichten in Batches, die Sie zum Erstellen von e-Mail-Nachrichten in Batches verwenden, mit dem Unterschied, dass sich einige der Parameter der [CreateItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) -Methode ändern. Verwenden Sie also zum Senden von e-Mail-Nachrichten mithilfe des verwaltete EWS-API den Code, den Sie zum [Erstellen von e-Mail-Nachrichten in Batches](#bk_createewsma)verwenden, und ersetzen Sie den Aufruf der **CreateItems** -Methode durch den Aufruf im folgenden Beispiel. In diesem Beispiel werden die Nachrichten im Ordner "Gesendete Elemente" erstellt, und die Nachrichten Disposition wird in [MessageDisposition. SendAndSaveCopy](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx)geändert, sodass die Nachricht gesendet und nicht nur lokal gespeichert wird.

```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a>Senden von e-Mail-Nachrichten in Batches mithilfe von EWS
<a name="bk_sendews"> </a>

Sie verwenden denselben Code zum Senden von e-Mail-Nachrichten in Batches, die Sie zum Erstellen von e-Mail-Nachrichten in Batches verwenden, mit dem Unterschied, dass sich einige der Attributwerte für den **CreateItem** -Vorgang ändern. Um also e-Mail-Nachrichten mithilfe von EWS zu senden, verwenden Sie den Code, mit dem Sie [e-Mail-Nachrichten in Batches erstellen](#bk_createews), und ändern Sie den **MessageDisposition** -Wert in "SendAndSaveCopy", und ändern Sie die [DistinguishedFolderId](https://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) in "Gesendete Elemente", wie im folgenden Codebeispiel dargestellt.

```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die einen [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert von **noError** für jede der neuen Nachrichten enthält, was darauf hinweist, dass jede e-Mail erstellt und erfolgreich gesendet wurde.

## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a>Abrufen von e-Mail-Nachrichten in Batches mithilfe der verwaltete EWS-API
<a name="bk_getewsma"> </a>

Sie können e-Mail-Nachrichten in Batches abrufen, indem Sie die verwaltete EWS-API [BindToItems](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt.

In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.

```cs
public static Collection<EmailMessage> BatchGetEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Create a property set that limits the properties returned by the Bind method to only those that are required.
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
    // Get the items from the server.
    // This method call results in a GetItem call to EWS.
    ServiceResponseCollection<GetItemResponse> response = service.BindToItems(itemIds, propSet);

    // Instantiate a collection of EmailMessage objects to populate from the values that are returned by the Exchange server.
    Collection<EmailMessage> messageItems = new Collection<EmailMessage>();
    foreach (GetItemResponse getItemResponse in response)
    {
        try
        {
            Item item = getItemResponse.Item;
            EmailMessage message = (EmailMessage)item;
            messageItems.Add(message);
            // Print out confirmation and the last eight characters of the item ID.
            Console.WriteLine("Found item {0}.", message.Id.ToString().Substring(144));
        }
        catch (Exception ex)
        {
           Console.WriteLine("Exception while getting a message: {0}", ex.Message);
        }
    }
    // Check for success of the BindToItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages retrieved successfully.");
        Console.WriteLine("\r\n");
    }
        return messageItems;
}
```

## <a name="get-email-messages-in-batches-by-using-ews"></a>Abrufen von e-Mail-Nachrichten in Batches mithilfe von EWS
<a name="bk_getews"> </a>

Sie können e-Mail-Nachrichten in Batches mit dem [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang und dem Code im folgenden Beispiel abrufen. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [e-Mail-Nachrichten in Batches abzurufen](#bk_getewsma).

[!HINWEIS] Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt.

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
    <m:GetItem>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="message:ToRecipients" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:ItemIds>
        <t:ItemId Id="m4NxAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB0" />
        <t:ItemId Id="m4NyAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB1" />
        <t:ItemId Id="m4NzAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKB2" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **GetItem** -Anforderung mit einer [GetItemResponse](https://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die die [ersten Klassen Eigenschaften](email-properties-and-elements-in-ews-in-exchange.md) für jede der angeforderten Nachrichten enthält.

## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a>Aktualisieren von e-Mail-Nachrichten in Batches mithilfe der verwaltete EWS-API
<a name="bk_updateewsma"> </a>

Sie können e-Mail-Nachrichten in Batches abrufen, indem Sie die verwaltete EWS-API [Update Items](https://msdn.microsoft.com/library/dd634705%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt.

Eine Liste der schreibbaren Eigenschaften von e-Mail-Nachrichten finden Sie unter [e-Mail-Eigenschaften und-Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).

Ausführliche Informationen zum Senden einer Entwurfsnachricht nach der Aktualisierung finden Sie unter [Senden von e-Mail-Nachrichten mithilfe der verwaltete EWS-API](#bk_sendewsma).

In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.

```cs
public static Collection<EmailMessage> BatchUpdateEmailItems(ExchangeService service, Collection<EmailMessage> messageItems)
{
    // Update the subject of each message locally.
    foreach (EmailMessage message in messageItems)
    {
        // Update the Subject of the email.
        message.Subject = "Updated subject at " + DateTime.Now;
        // Print out confirmation with the last eight characters of the item ID and the email subject.
        Console.WriteLine("Updated local email message {0} with the subject '{1}'.", message.Id.ToString().Substring(144), message.Subject);
    }
    // Send the item updates to the server.
    // This method call results in an UpdateItem call to EWS.
    ServiceResponseCollection<UpdateItemResponse> response = service.UpdateItems(messageItems, WellKnownFolderName.Drafts, ConflictResolutionMode.AutoResolve, MessageDisposition.SaveOnly, null);
    // Check for success of the UpdateItems method call.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("All email messages updated successfully.\r\n");
    }
    // If the method did not return success, print the result message for each email.
    else
    {
        Console.WriteLine("All emails were not successfully saved on the server.\r\n");
        int counter = 1;
        foreach (ServiceResponse resp in response)
        {
            Console.WriteLine("Result for (message {0}): {1}", counter, resp.Result);
            Console.WriteLine("Error Code: {0}", resp.ErrorCode);
            Console.WriteLine("ErrorMessage: {0}\r\n", resp.ErrorMessage);
            counter++;
        }
    }
    return messageItems;
}
```

## <a name="update-email-messages-in-batches-by-using-ews"></a>Aktualisieren von e-Mail-Nachrichten in Batches mithilfe von EWS
<a name="bk_updateews"> </a>

Sie können e-Mail-Nachrichten in Batches mit dem [GetItem](https://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang aktualisieren, wie im folgenden Codebeispiel gezeigt. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [e-Mail-Nachrichten in Batches zu aktualisieren](#bk_updateewsma).

Eine Liste der beschreibbaren e-Mail-Nachrichtenelemente finden Sie unter [e-Mail-Eigenschaften und-Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).

Ausführliche Informationen zum Senden einer Entwurfsnachricht nach der Aktualisierung finden Sie unter [Senden von e-Mail-Entwurfsnachrichten mithilfe von EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).

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
    <m:UpdateItem MessageDisposition="SaveOnly"
                  ConflictResolution="AutoResolve">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="drafts" />
      </m:SavedItemFolderId>
      <m:ItemChanges>
        <t:ItemChange>
          <t:ItemId Id="m4OVAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCy" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OWAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKCz" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
        <t:ItemChange>
          <t:ItemId Id="m4OXAAA="
                    ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKC0" />
          <t:Updates>
            <t:SetItemField>
              <t:FieldURI FieldURI="item:Subject" />
              <t:Message>
                <t:Subject>Updated subject at 1/17/2014 2:58:09 PM</t:Subject>
              </t:Message>
            </t:SetItemField>
          </t:Updates>
        </t:ItemChange>
      </m:ItemChanges>
    </m:UpdateItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **UpdateItem** -Anforderung mit einer [UpdateItemResponse](https://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert **noError**enthält, der angibt, dass jedes Update erfolgreich auf dem Server gespeichert wurde. Alle Konflikte werden im [ConflictResult](https://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) -Element gemeldet.

## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a>Löschen von e-Mail-Nachrichten in Batches mithilfe der verwaltete EWS-API
<a name="bk_deleteewsma"> </a>

Sie können Nachrichten in Batches löschen, indem Sie die verwaltete EWS-API [DeleteItems](https://msdn.microsoft.com/library/dd635460%28v=exchg.80%29.aspx) -Methode verwenden, wie im folgenden Beispiel gezeigt.

In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.

```cs
public static void BatchDeleteEmailItems(ExchangeService service, Collection<ItemId> itemIds)
{
    // Delete the batch of email message objects.
    // This method call results in an DeleteItem call to EWS.
    ServiceResponseCollection<ServiceResponse> response = service.DeleteItems(itemIds, DeleteMode.SoftDelete, null, AffectedTaskOccurrence.AllOccurrences);

    // Check for success of the DeleteItems method call.
    // DeleteItems returns success even if it does not find all the item IDs.
    if (response.OverallResult == ServiceResult.Success)
    {
        Console.WriteLine("Email messages deleted successfully.\r\n");
    }
    // If the method did not return success, print a message.
    else
    {
        Console.WriteLine("Not all email messages deleted successfully.\r\n");
    }
}
```

## <a name="delete-email-messages-in-batches-by-using-ews"></a>Löschen von e-Mail-Nachrichten in Batches mithilfe von EWS
<a name="bk_deleteews"> </a>

Sie können e-Mail-Nachrichten in Batches löschen, indem Sie den EWS-Vorgang [DeleteItem](../web-service-reference/deleteitem-operation.md) verwenden, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anforderung, die von der verwaltete EWS-API gesendet wird, wenn Sie die verwaltete EWS-API verwenden, um [e-Mail-Nachrichten in Batches zu löschen](#bk_deleteewsma).

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
    <m:DeleteItem DeleteType="SoftDelete"
                  AffectedTaskOccurrences="AllOccurrences">
      <m:ItemIds>
        <t:ItemId Id="m4OkAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDE" />
        <t:ItemId Id="m4OlAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDF" />
        <t:ItemId Id="m4OmAAA="
                  ChangeKey="CQAAABYAAAApjGm7TnMWQ5TzjbhziLL0AAF/yKDG" />
      </m:ItemIds>
    </m:DeleteItem>
  </soap:Body>
</soap:Envelope>
```

Der Server antwortet auf die **DeleteItem** -Anforderung mit einer [DeleteItemResponse](https://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Wert **noError** für jedes entfernte Element enthält. Beachten Sie, dass der Vorgang auch dann Success zurückgegeben wird, wenn die Element-ID nicht gefunden werden konnte.

## <a name="verifying-that-a-batch-process-completed-successfully"></a>Überprüfen, ob ein Batchprozess erfolgreich abgeschlossen wurde
<a name="bk_successful"> </a>

Wenn eine oder mehrere e-Mail-Nachrichten in einer Batchanforderung nicht wie angefordert verarbeitet werden können, wird für jede e-Mail-Nachricht, die fehlgeschlagen ist, ein Fehler zurückgegeben, und die restlichen e-Mails im Batch werden wie erwartet verarbeitet. Fehler in der Batchverarbeitung können auftreten, wenn das Element gelöscht wurde und daher nicht gesendet, abgerufen oder aktualisiert werden kann oder wenn das Element in einen anderen Ordner verschoben wurde und daher über eine neue Element-ID verfügt und nicht mit der gesendeten Element-ID geändert werden kann. Die Informationen in diesem Abschnitt zeigen, wie Fehlerdetails zu Fehlern in der Batchverarbeitung von e-Mail-Nachrichten abgerufen werden.

Um den Erfolg eines Batchprozesses mithilfe der verwaltete EWS-API zu überprüfen, können Sie überprüfen, ob die [OverallResult](https://msdn.microsoft.com/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft des [ServiceResponseCollection](https://msdn.microsoft.com/library/dd633715%28v=exchg.80%29.aspx) gleich [ServiceResult. Success](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)ist. Wenn dies der Fall ist, wurden alle e-Mails erfolgreich verarbeitet. Wenn **OverallResult** nicht gleich **ServiceResult. Success**ist, wurden eine oder mehrere der e-Mails nicht erfolgreich verarbeitet. Jedes der Objekte, die in der **ServiceResponseCollection** zurückgegeben werden, enthält die folgenden Eigenschaften:

- [ErrorCode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)

- [ErrorDetails](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)

- [ErrorMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)

- [ErrorProperties](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)

- [Ergebnis](https://msdn.microsoft.com/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)

Diese Eigenschaften enthalten Informationen dazu, warum die e-Mail-Nachrichten nicht wie angefordert verarbeitet werden konnten. In den Beispielen in diesem Artikel werden das **Ergebnis**, **errorCode**und **ErrorMessage** für jede fehlgeschlagene Nachricht gedruckt. Sie können diese Ergebnisse verwenden, um das Problem zu untersuchen.

Überprüfen Sie für EWS das [ResponseClass](https://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) -Attribut für jedes verarbeitete Element, um den Erfolg eines Batchprozesses zu überprüfen. Im folgenden finden Sie die grundlegende Struktur des **ResponseMessageType**, den Basistyp, von dem alle Antwortnachrichten abgeleitet werden.

```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

Das **ResponseClass** -Attribut wird auf " **Success** " festgelegt, wenn die e-Mail erfolgreich verarbeitet wurde, oder **Fehler** , wenn die e-Mail nicht erfolgreich verarbeitet wurde. Bei e-Mail-Nachrichten wird während der Batchverarbeitung keine **Warnung angezeigt** . Wenn der **ResponseClass** **erfolgreich**ist, wird das [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element, das folgt, auch immer auf **noError**festgelegt. Wenn das **ResponseClass** -Element **fehlerhaft**ist, müssen Sie die Werte der [MessageText](https://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx)-, **Response Code**-und [messagexml verwendet](https://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) -Elemente überprüfen, um zu ermitteln, was das Problem verursacht hat. [DescriptiveLinkKey](https://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) wird derzeit nicht verwendet.

## <a name="see-also"></a>Siehe auch


- [E-Mail- und EWS in Exchange](email-and-ews-in-exchange.md)

- [Senden von E-Mail-Nachrichten mit EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)

- [Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)

- [Verschieben und Kopieren von E-Mail-Nachrichten mithilfe von EWS in Exchange](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)

- [Einschränkungs Auswirkungen auf EWS-Batchanforderungen](ews-throttling-in-exchange.md#throttling-implications-for-ews-batch-requests)
