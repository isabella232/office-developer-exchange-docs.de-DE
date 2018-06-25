---
title: Verarbeiten von e-Mail-Nachrichten in Batches mithilfe von EWS in Exchange
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 96390f92-cab1-4de6-9ec2-a55678fc20af
description: Informationen Sie zum Erstellen, abrufen, aktualisieren und Löschen von e-Mail-Nachrichten in einem einzigen Aufruf im Batchmodus durch Verwenden der EWS Managed API oder EWS in Exchange.
ms.openlocfilehash: 30ebbdf4c92111df629c7662987e301d167336e2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757005"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a>Verarbeiten von e-Mail-Nachrichten in Batches mithilfe von EWS in Exchange

Informationen Sie zum Erstellen, abrufen, aktualisieren und Löschen von e-Mail-Nachrichten in einem einzigen Aufruf im Batchmodus durch Verwenden der EWS Managed API oder EWS in Exchange.
  
Sie können die EWS Managed API verwenden oder EWS Batches von e-Mail-Nachrichten, um die Anzahl von Anrufen zu verringern Clientidentität entwickelt werden an einen Exchange-Server. Wenn Sie der EWS Managed API mithilfe erstellen, abrufen, aktualisieren, löschen und Senden von Nachrichten in Batches, verwenden Sie [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) Methoden-Objekts während beim Arbeiten mit einzelnen e-Mail-Nachrichten, Methoden des Objekts ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) verwenden. Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die gleichen Vorgänge zum Arbeiten mit einzelnen und Batches von e-Mail-Nachrichten. 
  
**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Arbeit mit von e-Mail-Nachrichten im Batchmodus**

|**Gewünschte Aktion**|**Verwenden Sie diese Methode EWS Managed API**|**Zu verwendender EWS-Vorgang**|
|:-----|:-----|:-----|
|Erstellen von e-Mail-Nachrichten in batches  <br/> |[ExchangeService.CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|Abrufen von e-Mail-Nachrichten in batches  <br/> |[ExchangeService.BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|Aktualisieren von e-Mail-Nachrichten in batches  <br/> |[ExchangeService.UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) <br/> |[UpdateItem](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|Löschen von e-Mail-Nachrichten in batches  <br/> |[ExchangeService.DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) <br/> |[DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
In diesem Artikel erfahren Sie, wie Sie grundlegende Aufgaben für Batches von e-Mail-Nachrichten mithilfe der EWS Managed API oder EWS abschließen.
  
## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a>Erstellen von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API
<a name="bk_createewsma"> </a>

Sie können Nachrichten in Batches erstellen, mit der EWS Managed API **CreateItems** -Methode, wie im folgenden Beispiel dargestellt. In diesem Beispiel werden drei lokal ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekte erstellt, eine Auflistung aller Nachrichten hinzugefügt und dann Ruft die **CreateItems** -Methode für die Auflistung von Nachrichten. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

Beachten Sie, dass im Beispiel wird nur die Nachrichten im Ordner Entwürfe gespeichert. Es werden keine Nachrichten gesendet werden. Weitere Informationen zum Senden von Nachrichten finden Sie unter [Senden von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API](#bk_sendewsma).
  
## <a name="create-email-messages-in-batches-by-using-ews"></a>Erstellen von e-Mail-Nachrichten in Batches mithilfe von Exchange-Webdienste
<a name="bk_createews"> </a>

Sie können e-Mail-Nachrichten in Batches erstellen, mithilfe des [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -EWS-Vorgangs, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Erstellen von e-Mail-Nachrichten in Batches](#bk_createewsma)verwenden. 
  
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

Der Server antwortet an die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** für jede der neuen Nachrichten, die angibt, dass jede e-Mail erstellt und erfolgreich gespeichert wurde . 
  
Beachten Sie, dass im Beispiel wird nur die Nachrichten im Ordner Entwürfe gespeichert. Es werden keine Nachrichten gesendet werden. Weitere Informationen zum Senden von Nachrichten finden Sie unter [Senden von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste](#bk_sendews).
  
## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a>Senden von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API
<a name="bk_sendewsma"> </a>

Sie verwenden den gleichen Code zum Senden von e-Mail-Nachrichten in Batches, mit denen Sie zum Erstellen von e-Mail-Nachrichten in Batches, außer dass wenige Methodenparameter [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) ändern. Daher zum Senden von e-Mail-Nachrichten mithilfe der EWS Managed API, verwenden Sie den Code, den Sie zum [Erstellen von e-Mail-Nachrichten in Batches](#bk_createewsma)verwenden, und Ersetzen Sie den Anruf an die **CreateItems** -Methode mit dem Aufruf im folgenden Beispiel. In diesem Beispiel werden die Nachrichten im Ordner "Gesendete Elemente" erstellt, und die Disposition Nachricht zu [MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), so geändert, dass die Nachricht gesendet wird, und nicht nur lokal gespeichert.
  
```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a>Senden von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste
<a name="bk_sendews"> </a>

Verwenden Sie denselben Code zum Senden von e-Mail-Nachrichten in Batches für die Verwendung zum Erstellen von e-Mail-Nachrichten in Batches, mit der Ausnahme, dass nur einige der Attributwerte für den Vorgang **CreateItem** ändern. Zum Senden von e-Mail-Nachrichten mithilfe der Exchange-Webdienste, also, verwenden Sie den Code, die Sie verwenden, um [e-Mail-Nachricht in Batches erstellen](#bk_createews)und ändern Sie den Wert **"MessageDisposition"** in "SendAndSaveCopy", und ändern Sie die [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) in "Gesendete Elemente", siehe die folgende Codebeispiel. 
  
```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** für jede der neuen Nachrichten, gibt an, dass jede e-Mail erstellt und erfolgreich gesendet wurde. 
  
## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a>Abrufen von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API
<a name="bk_getewsma"> </a>

Sie können e-Mail-Nachrichten in Batches abrufen, indem Sie mithilfe der EWS Managed API [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) -Methode, wie im folgenden Beispiel dargestellt. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="get-email-messages-in-batches-by-using-ews"></a>Abrufen von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste
<a name="bk_getews"> </a>

Sie können e-Mail-Nachrichten in Batches mithilfe von [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang und den Code im folgenden Beispiel abrufen. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Abrufen von e-Mail-Nachrichten in Batches](#bk_getewsma)verwenden. 
  
[!HINWEIS] Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt. 
  
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

Der Server antwortet auf die Anforderung **GetItem** mit einer [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die die [First-Class Eigenschaften](email-properties-and-elements-in-ews-in-exchange.md) für jede der angeforderten Nachrichten enthält. 
  
## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a>Aktualisieren von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API
<a name="bk_updateewsma"> </a>

Sie können e-Mail-Nachrichten in Batches abrufen, indem Sie mithilfe der EWS Managed API [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) -Methode, wie im folgenden Beispiel dargestellt. 
  
Eine Liste der Eigenschaften der schreibbare e-Mail-Nachricht finden Sie unter [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).
  
Ausführliche Informationen über den Entwurf einer Nachricht senden, nach der Aktualisierung wurde finden Sie unter [Senden von e-Mail-Nachrichten mithilfe der EWS Managed API](#bk_sendewsma).
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="update-email-messages-in-batches-by-using-ews"></a>Aktualisieren von e-Mail-Nachrichten in Batches mithilfe von Exchange-Webdienste
<a name="bk_updateews"> </a>

Sie können e-Mail-Nachrichten in Batches aktualisieren, mithilfe von [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgangs, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Aktualisieren von e-Mail-Nachrichten in Batches](#bk_updateewsma)verwenden.
  
Eine Liste der schreibbare e-Mail-Nachrichtenelemente finden Sie unter [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).
  
Ausführliche Informationen über den Entwurf einer Nachricht senden, nach der Aktualisierung wurde finden Sie unter [den Entwurf einer e-Mail-Nachricht mithilfe der Exchange-Webdienste senden](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).
  
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

Der Server antwortet auf die Anforderung **UpdateItem** mit einer [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, die angibt, dass es sich bei allen Updates auf dem Server erfolgreich gespeichert wurde. Im [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) -Element werden alle Konflikte gemeldet. 
  
## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a>Löschen von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API
<a name="bk_deleteewsma"> </a>

Sie können Nachrichten in Batches löschen, mithilfe der EWS Managed API [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) -Methode, wie im folgenden Beispiel dargestellt. 
  
In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde. 
  
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

## <a name="delete-email-messages-in-batches-by-using-ews"></a>Löschen von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste
<a name="bk_deleteews"> </a>

Sie können e-Mail-Nachrichten in Batches mit löschen [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) EWS-Vorgangs, wie im folgenden Codebeispiel dargestellt. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Löschen von e-Mail-Nachrichten in Batches](#bk_deleteewsma)verwenden.
  
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

Der Server antwortet auf die Anforderung **DeleteItem** mit einer [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) -Nachricht, [die responseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Wert **NoError** für jedes Element enthält, das entfernt wurde. Beachten Sie, dass der Vorgang erfolgreich auch zurückgegeben, wenn die Element-ID wurde nicht gefunden. 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a>Sicherstellen, dass die Batch-Verarbeitung erfolgreich abgeschlossen
<a name="bk_successful"> </a>

Wenn eine oder mehrere e-Mail-Nachrichten in einer Anforderung im Batch nicht verarbeitet werden können, wie angefordert, für jede e-Mail-Nachricht, die fehlgeschlagen ist ein Fehler zurückgegeben, und die restlichen die e-Mails im Batch erwartungsgemäß verarbeitet werden. Fehler im Batch-Verarbeitung können auftreten, wenn das Element wurde gelöscht, und daher nicht gesendet, abgerufen, oder aktualisiert werden, oder wenn das Element in einen anderen Ordner verschoben und daher eine neues Element-ID hat und nicht werden, mit der Element-ID gesendet geändert kann. Die Informationen in diesem Abschnitt veranschaulicht die Fehlerdetails zu Fehlern in Batchverarbeitung von e-Mail-Nachricht erhalten möchten.
  
Um den Erfolg der Batch-Verarbeitung mithilfe der EWS Managed API zu überprüfen, können Sie überprüfen, dass die [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft der [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)gleich ist. In diesem Fall wurden alle e-Mails erfolgreich verarbeitet. Ist die **OverallResult** nicht gleich **ServiceResult.Success**, eine oder mehrere der e-Mails wurden nicht verarbeitet werden. Jeder der Objekte zurückgegeben, die in der **ServiceResponseCollection** enthält die folgenden Eigenschaften: 
  
- [ErrorCode](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [ErrorDetails](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [ErrorMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [ErrorProperties](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [Ergebnis](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
Diese Eigenschaften enthalten Informationen, warum die e-Mail-Nachrichten nicht verarbeitet werden kann, wie angefordert. Die Beispiele in diesem Artikel drucken Sie das **Ergebnis**, **ErrorCode**und **ErrorMessage** für jede fehlgeschlagene Nachricht. Sie können diese Ergebnisse verwenden, um das Problem zu untersuchen. 
  
Überprüfen Sie für EWS um die erfolgreiche eines Prozesses im Batchmodus zu überprüfen, das [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) -Attribut für jedes Element verarbeitet werden. Im folgenden finden die Grundstruktur der **ResponseMessageType**, den Basistyp der Antwort, die alle Nachrichten abgeleitet sind. 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

Das **ResponseClass** -Attribut wird zum **Erfolg** , wenn die e-Mail-Nachricht wurde erfolgreich verarbeitet oder **Fehler** festgelegt, wenn die e-Mail-Nachricht nicht erfolgreich verarbeitet wurde. Für e-Mail-Nachrichten wird eine **Warnung** nicht bei der Batchverarbeitung auftreten. Wenn die **ResponseClass** **erfolgreich**ist, wird das [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element, das folgt auch immer auf **NoError**festgelegt. Wenn die **ResponseClass** **Fehler**ist, müssen Sie überprüfen Sie die Werte der [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**und [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) Elemente, die Ursache des Problems zu bestimmen. [DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) wird derzeit nicht verwendet. 
  
## <a name="see-also"></a>Siehe auch


- [E-Mail- und EWS in Exchange](email-and-ews-in-exchange.md)
    
- [Senden von e-Mail-Nachrichten mithilfe der EWS in Exchange](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [Reagieren Sie auf e-Mail-Nachrichten mithilfe der EWS in Exchange](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [Verschieben und Kopieren von e-Mail-Nachrichten mithilfe der EWS in Exchange](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [Konsequenzen für Batchanforderungen EWS-Einschränkung](ews-throttling-in-exchange.md#bk_ThrottlingBatch)
    

