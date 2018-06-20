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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757005"
---
# <a name="process-email-messages-in-batches-by-using-ews-in-exchange"></a><span data-ttu-id="32d2e-103">Verarbeiten von e-Mail-Nachrichten in Batches mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="32d2e-103">Process email messages in batches by using EWS in Exchange</span></span>

<span data-ttu-id="32d2e-104">Informationen Sie zum Erstellen, abrufen, aktualisieren und Löschen von e-Mail-Nachrichten in einem einzigen Aufruf im Batchmodus durch Verwenden der EWS Managed API oder EWS in Exchange.</span><span class="sxs-lookup"><span data-stu-id="32d2e-104">Learn how to create, get, update, and delete batches of email messages in a single call by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="32d2e-105">Sie können die EWS Managed API verwenden oder EWS Batches von e-Mail-Nachrichten, um die Anzahl von Anrufen zu verringern Clientidentität entwickelt werden an einen Exchange-Server.</span><span class="sxs-lookup"><span data-stu-id="32d2e-105">You can use the EWS Managed API or EWS to work with batches of email messages to reduce the number of calls a client makes to an Exchange server.</span></span> <span data-ttu-id="32d2e-106">Wenn Sie der EWS Managed API mithilfe erstellen, abrufen, aktualisieren, löschen und Senden von Nachrichten in Batches, verwenden Sie [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) Methoden-Objekts während beim Arbeiten mit einzelnen e-Mail-Nachrichten, Methoden des Objekts ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) verwenden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-106">When you use the EWS Managed API to create, get, update, delete, and send messages in batches, you use [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object methods, whereas when you work with single email messages, you use [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object methods.</span></span> <span data-ttu-id="32d2e-107">Wenn Sie Exchange-Webdienste verwenden, verwenden Sie die gleichen Vorgänge zum Arbeiten mit einzelnen und Batches von e-Mail-Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="32d2e-107">If you are using EWS, you use the same operations to work with both single and batches of email messages.</span></span> 
  
<span data-ttu-id="32d2e-108">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Arbeit mit von e-Mail-Nachrichten im Batchmodus**</span><span class="sxs-lookup"><span data-stu-id="32d2e-108">**Table 1. EWS Managed API methods and EWS operations for working with batches of email messages**</span></span>

|<span data-ttu-id="32d2e-109">**Gewünschte Aktion**</span><span class="sxs-lookup"><span data-stu-id="32d2e-109">**In order to…**</span></span>|<span data-ttu-id="32d2e-110">**Verwenden Sie diese Methode EWS Managed API**</span><span class="sxs-lookup"><span data-stu-id="32d2e-110">**Use this EWS Managed API method**</span></span>|<span data-ttu-id="32d2e-111">**Zu verwendender EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="32d2e-111">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="32d2e-112">Erstellen von e-Mail-Nachrichten in batches</span><span class="sxs-lookup"><span data-stu-id="32d2e-112">Create email messages in batches</span></span>  <br/> |[<span data-ttu-id="32d2e-113">ExchangeService.CreateItems</span><span class="sxs-lookup"><span data-stu-id="32d2e-113">ExchangeService.CreateItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="32d2e-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="32d2e-114">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="32d2e-115">Abrufen von e-Mail-Nachrichten in batches</span><span class="sxs-lookup"><span data-stu-id="32d2e-115">Get email messages in batches</span></span>  <br/> |[<span data-ttu-id="32d2e-116">ExchangeService.BindToItems</span><span class="sxs-lookup"><span data-stu-id="32d2e-116">ExchangeService.BindToItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="32d2e-117">GetItem</span><span class="sxs-lookup"><span data-stu-id="32d2e-117">GetItem</span></span>](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="32d2e-118">Aktualisieren von e-Mail-Nachrichten in batches</span><span class="sxs-lookup"><span data-stu-id="32d2e-118">Update email messages in batches</span></span>  <br/> |[<span data-ttu-id="32d2e-119">ExchangeService.UpdateItems</span><span class="sxs-lookup"><span data-stu-id="32d2e-119">ExchangeService.UpdateItems</span></span>](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="32d2e-120">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="32d2e-120">UpdateItem</span></span>](http://msdn.microsoft.com/library/5d027523-e0bc-4da2-b60b-0cb9fc1fdfe4%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="32d2e-121">Löschen von e-Mail-Nachrichten in batches</span><span class="sxs-lookup"><span data-stu-id="32d2e-121">Delete email messages in batches</span></span>  <br/> |[<span data-ttu-id="32d2e-122">ExchangeService.DeleteItems</span><span class="sxs-lookup"><span data-stu-id="32d2e-122">ExchangeService.DeleteItems</span></span>](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="32d2e-123">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="32d2e-123">DeleteItem</span></span>](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="32d2e-124">In diesem Artikel erfahren Sie, wie Sie grundlegende Aufgaben für Batches von e-Mail-Nachrichten mithilfe der EWS Managed API oder EWS abschließen.</span><span class="sxs-lookup"><span data-stu-id="32d2e-124">In this article, you'll learn how to complete basic tasks for batches of email messages by using the EWS Managed API or EWS.</span></span>
  
## <a name="create-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="32d2e-125">Erstellen von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="32d2e-125">Create email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="32d2e-126"><a name="bk_createewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-126"></span></span>

<span data-ttu-id="32d2e-127">Sie können Nachrichten in Batches erstellen, mit der EWS Managed API **CreateItems** -Methode, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-127">You can create messages in batches by using the EWS Managed API **CreateItems** method, as shown in the following example.</span></span> <span data-ttu-id="32d2e-128">In diesem Beispiel werden drei lokal ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekte erstellt, eine Auflistung aller Nachrichten hinzugefügt und dann Ruft die **CreateItems** -Methode für die Auflistung von Nachrichten.</span><span class="sxs-lookup"><span data-stu-id="32d2e-128">This example creates three [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) objects locally, adds each message to a collection, then calls the **CreateItems** method on the collection of messages.</span></span> 
  
<span data-ttu-id="32d2e-129">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-129">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

<span data-ttu-id="32d2e-130">Beachten Sie, dass im Beispiel wird nur die Nachrichten im Ordner Entwürfe gespeichert. Es werden keine Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-130">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="32d2e-131">Weitere Informationen zum Senden von Nachrichten finden Sie unter [Senden von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API](#bk_sendewsma).</span><span class="sxs-lookup"><span data-stu-id="32d2e-131">For more about how to send the messages, see [Send email messages in batches by using the EWS Managed API](#bk_sendewsma).</span></span>
  
## <a name="create-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="32d2e-132">Erstellen von e-Mail-Nachrichten in Batches mithilfe von Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="32d2e-132">Create email messages in batches by using EWS</span></span>
<span data-ttu-id="32d2e-133"><a name="bk_createews"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-133"></span></span>

<span data-ttu-id="32d2e-134">Sie können e-Mail-Nachrichten in Batches erstellen, mithilfe des [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -EWS-Vorgangs, wie im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-134">You can create email messages in batches by using the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="32d2e-135">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Erstellen von e-Mail-Nachrichten in Batches](#bk_createewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-135">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [create email messages in batches](#bk_createewsma).</span></span> 
  
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

<span data-ttu-id="32d2e-136">Der Server antwortet an die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** für jede der neuen Nachrichten, die angibt, dass jede e-Mail erstellt und erfolgreich gespeichert wurde .</span><span class="sxs-lookup"><span data-stu-id="32d2e-136">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and saved successfully.</span></span> 
  
<span data-ttu-id="32d2e-137">Beachten Sie, dass im Beispiel wird nur die Nachrichten im Ordner Entwürfe gespeichert. Es werden keine Nachrichten gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-137">Note that the example only saves the messages in the Drafts folder; it does not send the messages.</span></span> <span data-ttu-id="32d2e-138">Weitere Informationen zum Senden von Nachrichten finden Sie unter [Senden von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste](#bk_sendews).</span><span class="sxs-lookup"><span data-stu-id="32d2e-138">For more about how to send the messages, see [Send email messages in batches by using EWS](#bk_sendews).</span></span>
  
## <a name="send-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="32d2e-139">Senden von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="32d2e-139">Send email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="32d2e-140"><a name="bk_sendewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-140"></span></span>

<span data-ttu-id="32d2e-141">Sie verwenden den gleichen Code zum Senden von e-Mail-Nachrichten in Batches, mit denen Sie zum Erstellen von e-Mail-Nachrichten in Batches, außer dass wenige Methodenparameter [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) ändern.</span><span class="sxs-lookup"><span data-stu-id="32d2e-141">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the [CreateItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.createitems%28v=exchg.80%29.aspx) method parameters change.</span></span> <span data-ttu-id="32d2e-142">Daher zum Senden von e-Mail-Nachrichten mithilfe der EWS Managed API, verwenden Sie den Code, den Sie zum [Erstellen von e-Mail-Nachrichten in Batches](#bk_createewsma)verwenden, und Ersetzen Sie den Anruf an die **CreateItems** -Methode mit dem Aufruf im folgenden Beispiel.</span><span class="sxs-lookup"><span data-stu-id="32d2e-142">So, to send email messages by using the EWS Managed API, use the code you use to [create email messages in batches](#bk_createewsma), and replace the call to the **CreateItems** method with the call in the following example.</span></span> <span data-ttu-id="32d2e-143">In diesem Beispiel werden die Nachrichten im Ordner "Gesendete Elemente" erstellt, und die Disposition Nachricht zu [MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), so geändert, dass die Nachricht gesendet wird, und nicht nur lokal gespeichert.</span><span class="sxs-lookup"><span data-stu-id="32d2e-143">In this example, the messages are created in the Sent Items folder, and the message disposition is changed to [MessageDisposition.SendAndSaveCopy](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.messagedisposition%28v=exchg.80%29.aspx), so that the message is sent, and not just saved locally.</span></span>
  
```cs
// Create and send the batch of email messages on the server.
// This method call results in an CreateItem call to EWS.
ServiceResponseCollection<ServiceResponse> response = service.CreateItems(messageItems, WellKnownFolderName.SentItems, MessageDisposition.SendAndSaveCopy, null);
```

## <a name="send-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="32d2e-144">Senden von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="32d2e-144">Send email messages in batches by using EWS</span></span>
<span data-ttu-id="32d2e-145"><a name="bk_sendews"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-145"></span></span>

<span data-ttu-id="32d2e-146">Verwenden Sie denselben Code zum Senden von e-Mail-Nachrichten in Batches für die Verwendung zum Erstellen von e-Mail-Nachrichten in Batches, mit der Ausnahme, dass nur einige der Attributwerte für den Vorgang **CreateItem** ändern.</span><span class="sxs-lookup"><span data-stu-id="32d2e-146">You use the same code to send email messages in batches that you use to create email messages in batches, except that a few of the attribute values change for the **CreateItem** operation.</span></span> <span data-ttu-id="32d2e-147">Zum Senden von e-Mail-Nachrichten mithilfe der Exchange-Webdienste, also, verwenden Sie den Code, die Sie verwenden, um [e-Mail-Nachricht in Batches erstellen](#bk_createews)und ändern Sie den Wert **"MessageDisposition"** in "SendAndSaveCopy", und ändern Sie die [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) in "Gesendete Elemente", siehe die folgende Codebeispiel.</span><span class="sxs-lookup"><span data-stu-id="32d2e-147">So, to send email messages by using EWS, use the code you use to [create email message in batches](#bk_createews), and change the **MessageDisposition** value to "SendAndSaveCopy", and change the [DistinguishedFolderId](http://msdn.microsoft.com/library/50018162-2941-4227-8a5b-d6b4686bb32f%28Office.15%29.aspx) to "sentitems", as shown in the following code example.</span></span> 
  
```XML
<m:CreateItem MessageDisposition="SendAndSaveCopy">
  <m:SavedItemFolderId>
    <t:DistinguishedFolderId Id="sentitems" />
  </m:SavedItemFolderId>
```

<span data-ttu-id="32d2e-148">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **NoError** für jede der neuen Nachrichten, gibt an, dass jede e-Mail erstellt und erfolgreich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-148">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each of the new messages, which indicates that each email was created and sent successfully.</span></span> 
  
## <a name="get-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="32d2e-149">Abrufen von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="32d2e-149">Get email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="32d2e-150"><a name="bk_getewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-150"></span></span>

<span data-ttu-id="32d2e-151">Sie können e-Mail-Nachrichten in Batches abrufen, indem Sie mithilfe der EWS Managed API [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) -Methode, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-151">You can get email messages in batches by using the EWS Managed API [BindToItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.bindtoitems%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="32d2e-152">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-152">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="get-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="32d2e-153">Abrufen von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="32d2e-153">Get email messages in batches by using EWS</span></span>
<span data-ttu-id="32d2e-154"><a name="bk_getews"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-154"></span></span>

<span data-ttu-id="32d2e-155">Sie können e-Mail-Nachrichten in Batches mithilfe von [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgang und den Code im folgenden Beispiel abrufen.</span><span class="sxs-lookup"><span data-stu-id="32d2e-155">You can get email messages in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation and the code in the following example.</span></span> <span data-ttu-id="32d2e-156">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Abrufen von e-Mail-Nachrichten in Batches](#bk_getewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-156">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [get email messages in batches](#bk_getewsma).</span></span> 
  
<span data-ttu-id="32d2e-157">[!HINWEIS] Die Attribute **ItemId** und **ChangeKey** wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-157">The **ItemId** and **ChangeKey** attributes have been shortened for readability.</span></span> 
  
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

<span data-ttu-id="32d2e-158">Der Server antwortet auf die Anforderung **GetItem** mit einer [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) -Nachricht, die die [First-Class Eigenschaften](email-properties-and-elements-in-ews-in-exchange.md) für jede der angeforderten Nachrichten enthält.</span><span class="sxs-lookup"><span data-stu-id="32d2e-158">The server responds to the **GetItem** request with a [GetItemResponse](http://msdn.microsoft.com/library/8b66de1b-26a6-476c-9585-a96059125716%28Office.15%29.aspx) message that includes the [first class properties](email-properties-and-elements-in-ews-in-exchange.md) for each of the requested messages.</span></span> 
  
## <a name="update-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="32d2e-159">Aktualisieren von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="32d2e-159">Update email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="32d2e-160"><a name="bk_updateewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-160"></span></span>

<span data-ttu-id="32d2e-161">Sie können e-Mail-Nachrichten in Batches abrufen, indem Sie mithilfe der EWS Managed API [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) -Methode, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-161">You can get email messages in batches by using the EWS Managed API [UpdateItems](http://msdn.microsoft.com/en-us/library/dd634705%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="32d2e-162">Eine Liste der Eigenschaften der schreibbare e-Mail-Nachricht finden Sie unter [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="32d2e-162">For a list of writable email message properties, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="32d2e-163">Ausführliche Informationen über den Entwurf einer Nachricht senden, nach der Aktualisierung wurde finden Sie unter [Senden von e-Mail-Nachrichten mithilfe der EWS Managed API](#bk_sendewsma).</span><span class="sxs-lookup"><span data-stu-id="32d2e-163">For details about how to send a draft message after it's been updated, see [Sending email messages by using the EWS Managed API](#bk_sendewsma).</span></span>
  
<span data-ttu-id="32d2e-164">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-164">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="update-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="32d2e-165">Aktualisieren von e-Mail-Nachrichten in Batches mithilfe von Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="32d2e-165">Update email messages in batches by using EWS</span></span>
<span data-ttu-id="32d2e-166"><a name="bk_updateews"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-166"></span></span>

<span data-ttu-id="32d2e-167">Sie können e-Mail-Nachrichten in Batches aktualisieren, mithilfe von [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) -EWS-Vorgangs, wie im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-167">You can update email messages in batches by using the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) EWS operation, as shown in following code example.</span></span> <span data-ttu-id="32d2e-168">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Aktualisieren von e-Mail-Nachrichten in Batches](#bk_updateewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-168">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [update email messages in batches](#bk_updateewsma).</span></span>
  
<span data-ttu-id="32d2e-169">Eine Liste der schreibbare e-Mail-Nachrichtenelemente finden Sie unter [E-Mail-Eigenschaften und Elemente in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="32d2e-169">For a list of writable email message elements, see [Email properties and elements in EWS in Exchange](email-properties-and-elements-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="32d2e-170">Ausführliche Informationen über den Entwurf einer Nachricht senden, nach der Aktualisierung wurde finden Sie unter [den Entwurf einer e-Mail-Nachricht mithilfe der Exchange-Webdienste senden](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span><span class="sxs-lookup"><span data-stu-id="32d2e-170">For details about how to send a draft message after it's been updated, see [Send a draft email message by using EWS](how-to-send-email-messages-by-using-ews-in-exchange.md#bk_senddraftews).</span></span>
  
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

<span data-ttu-id="32d2e-171">Der Server antwortet auf die Anforderung **UpdateItem** mit einer [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) -Nachricht, die enthält den Wert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, die angibt, dass es sich bei allen Updates auf dem Server erfolgreich gespeichert wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-171">The server responds to the **UpdateItem** request with an [UpdateItemResponse](http://msdn.microsoft.com/library/023b79b4-c675-4669-9112-d85499ec4fc4%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that each of the updates was saved successfully on the server.</span></span> <span data-ttu-id="32d2e-172">Im [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) -Element werden alle Konflikte gemeldet.</span><span class="sxs-lookup"><span data-stu-id="32d2e-172">Any conflicts are reported in the [ConflictResult](http://msdn.microsoft.com/library/08cdd547-4de7-4c7a-b60f-e618dc217d20%28Office.15%29.aspx) element.</span></span> 
  
## <a name="delete-email-messages-in-batches-by-using-the-ews-managed-api"></a><span data-ttu-id="32d2e-173">Löschen von e-Mail-Nachrichten in Batches mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="32d2e-173">Delete email messages in batches by using the EWS Managed API</span></span>
<span data-ttu-id="32d2e-174"><a name="bk_deleteewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-174"></span></span>

<span data-ttu-id="32d2e-175">Sie können Nachrichten in Batches löschen, mithilfe der EWS Managed API [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) -Methode, wie im folgenden Beispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-175">You can delete messages in batches by using the EWS Managed API [DeleteItems](http://msdn.microsoft.com/en-us/library/dd635460%28v=exchg.80%29.aspx) method, as shown in the following example.</span></span> 
  
<span data-ttu-id="32d2e-176">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-176">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
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

## <a name="delete-email-messages-in-batches-by-using-ews"></a><span data-ttu-id="32d2e-177">Löschen von e-Mail-Nachrichten in Batches mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="32d2e-177">Delete email messages in batches by using EWS</span></span>
<span data-ttu-id="32d2e-178"><a name="bk_deleteews"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-178"></span></span>

<span data-ttu-id="32d2e-179">Sie können e-Mail-Nachrichten in Batches mit löschen [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) EWS-Vorgangs, wie im folgenden Codebeispiel dargestellt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-179">You can delete email messages in batches by using the [DeleteItem](http://msdn.microsoft.com/library/3e26c416-fa12-476e-bfd2-5c1f4bb7b348%28Office.15%29.aspx) EWS operation, as shown in the following code example.</span></span> <span data-ttu-id="32d2e-180">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie die EWS Managed API zum [Löschen von e-Mail-Nachrichten in Batches](#bk_deleteewsma)verwenden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-180">This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [delete email messages in batches](#bk_deleteewsma).</span></span>
  
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

<span data-ttu-id="32d2e-181">Der Server antwortet auf die Anforderung **DeleteItem** mit einer [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) -Nachricht, [die responseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) Wert **NoError** für jedes Element enthält, das entfernt wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-181">The server responds to the **DeleteItem** request with a [DeleteItemResponse](http://msdn.microsoft.com/library/86463d66-fe47-4a19-a81b-e24841e816ab%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** for each item that was removed.</span></span> <span data-ttu-id="32d2e-182">Beachten Sie, dass der Vorgang erfolgreich auch zurückgegeben, wenn die Element-ID wurde nicht gefunden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-182">Note that the operation also returns success if the item ID could not be found.</span></span> 
  
## <a name="verifying-that-a-batch-process-completed-successfully"></a><span data-ttu-id="32d2e-183">Sicherstellen, dass die Batch-Verarbeitung erfolgreich abgeschlossen</span><span class="sxs-lookup"><span data-stu-id="32d2e-183">Verifying that a batch process completed successfully</span></span>
<span data-ttu-id="32d2e-184"><a name="bk_successful"> </a></span><span class="sxs-lookup"><span data-stu-id="32d2e-184"></span></span>

<span data-ttu-id="32d2e-185">Wenn eine oder mehrere e-Mail-Nachrichten in einer Anforderung im Batch nicht verarbeitet werden können, wie angefordert, für jede e-Mail-Nachricht, die fehlgeschlagen ist ein Fehler zurückgegeben, und die restlichen die e-Mails im Batch erwartungsgemäß verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-185">When one or more email messages in a batched request can't be processed as requested, an error is returned for each email message that failed, and the rest of the emails in the batch are processed as expected.</span></span> <span data-ttu-id="32d2e-186">Fehler im Batch-Verarbeitung können auftreten, wenn das Element wurde gelöscht, und daher nicht gesendet, abgerufen, oder aktualisiert werden, oder wenn das Element in einen anderen Ordner verschoben und daher eine neues Element-ID hat und nicht werden, mit der Element-ID gesendet geändert kann.</span><span class="sxs-lookup"><span data-stu-id="32d2e-186">Failures in batch processing can occur if the item was deleted, and therefore can't be sent, retrieved, or updated, or if the item moved to a different folder, and therefore has a new item ID, and cannot be modified with the item ID sent.</span></span> <span data-ttu-id="32d2e-187">Die Informationen in diesem Abschnitt veranschaulicht die Fehlerdetails zu Fehlern in Batchverarbeitung von e-Mail-Nachricht erhalten möchten.</span><span class="sxs-lookup"><span data-stu-id="32d2e-187">The information in this section shows how to get error details about failures in batch processing of email message.</span></span>
  
<span data-ttu-id="32d2e-188">Um den Erfolg der Batch-Verarbeitung mithilfe der EWS Managed API zu überprüfen, können Sie überprüfen, dass die [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) -Eigenschaft der [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx)gleich ist.</span><span class="sxs-lookup"><span data-stu-id="32d2e-188">To verify the success of a batch process by using the EWS Managed API, you can check that the [OverallResult](http://msdn.microsoft.com/en-us/library/dd634515%28v=exchg.80%29.aspx) property of the [ServiceResponseCollection](http://msdn.microsoft.com/en-us/library/dd633715%28v=exchg.80%29.aspx) is equal to [ServiceResult.Success](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresult%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="32d2e-189">In diesem Fall wurden alle e-Mails erfolgreich verarbeitet.</span><span class="sxs-lookup"><span data-stu-id="32d2e-189">If so, all the emails were processed successfully.</span></span> <span data-ttu-id="32d2e-190">Ist die **OverallResult** nicht gleich **ServiceResult.Success**, eine oder mehrere der e-Mails wurden nicht verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-190">If the **OverallResult** is not equal to **ServiceResult.Success**, one or more of the emails were not processed successfully.</span></span> <span data-ttu-id="32d2e-191">Jeder der Objekte zurückgegeben, die in der **ServiceResponseCollection** enthält die folgenden Eigenschaften:</span><span class="sxs-lookup"><span data-stu-id="32d2e-191">Each of the objects returned in the **ServiceResponseCollection** contains the following properties:</span></span> 
  
- [<span data-ttu-id="32d2e-192">ErrorCode</span><span class="sxs-lookup"><span data-stu-id="32d2e-192">ErrorCode</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorcode%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="32d2e-193">ErrorDetails</span><span class="sxs-lookup"><span data-stu-id="32d2e-193">ErrorDetails</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errordetails%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="32d2e-194">ErrorMessage</span><span class="sxs-lookup"><span data-stu-id="32d2e-194">ErrorMessage</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errormessage%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="32d2e-195">ErrorProperties</span><span class="sxs-lookup"><span data-stu-id="32d2e-195">ErrorProperties</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.serviceresponse.errorproperties%28v=exchg.80%29.aspx)
    
- [<span data-ttu-id="32d2e-196">Ergebnis</span><span class="sxs-lookup"><span data-stu-id="32d2e-196">Result</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.serviceresponse.result%28v=exchg.80%29.aspx)
    
<span data-ttu-id="32d2e-197">Diese Eigenschaften enthalten Informationen, warum die e-Mail-Nachrichten nicht verarbeitet werden kann, wie angefordert.</span><span class="sxs-lookup"><span data-stu-id="32d2e-197">These properties contain information about why the email messages could not be processed as requested.</span></span> <span data-ttu-id="32d2e-198">Die Beispiele in diesem Artikel drucken Sie das **Ergebnis**, **ErrorCode**und **ErrorMessage** für jede fehlgeschlagene Nachricht.</span><span class="sxs-lookup"><span data-stu-id="32d2e-198">The examples in this article print out the **Result**, **ErrorCode**, and **ErrorMessage** for each failed message.</span></span> <span data-ttu-id="32d2e-199">Sie können diese Ergebnisse verwenden, um das Problem zu untersuchen.</span><span class="sxs-lookup"><span data-stu-id="32d2e-199">You can use these results to investigate the issue.</span></span> 
  
<span data-ttu-id="32d2e-200">Überprüfen Sie für EWS um die erfolgreiche eines Prozesses im Batchmodus zu überprüfen, das [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) -Attribut für jedes Element verarbeitet werden.</span><span class="sxs-lookup"><span data-stu-id="32d2e-200">For EWS, to verify the success of a batched process, check the [ResponseClass](http://msdn.microsoft.com/library/bf57265a-d354-4cd7-bbfc-d93e19cbede6%28Office.15%29.aspx) attribute for each item being processed.</span></span> <span data-ttu-id="32d2e-201">Im folgenden finden die Grundstruktur der **ResponseMessageType**, den Basistyp der Antwort, die alle Nachrichten abgeleitet sind.</span><span class="sxs-lookup"><span data-stu-id="32d2e-201">The following is the basic structure of the **ResponseMessageType**, the base type from which all response messages are derived.</span></span> 
  
```XML
<ResponseMessage ResponseClass="Success | Warning | Error">
            <MessageText/>
            <ResponseCode/>
            <DescriptiveLinkKey/>
            <MessageXml/>
</ResponseMessage>
```

<span data-ttu-id="32d2e-202">Das **ResponseClass** -Attribut wird zum **Erfolg** , wenn die e-Mail-Nachricht wurde erfolgreich verarbeitet oder **Fehler** festgelegt, wenn die e-Mail-Nachricht nicht erfolgreich verarbeitet wurde.</span><span class="sxs-lookup"><span data-stu-id="32d2e-202">The **ResponseClass** attribute is set to **Success** if the email was processed successfully, or **Error** if the email was not processed successfully.</span></span> <span data-ttu-id="32d2e-203">Für e-Mail-Nachrichten wird eine **Warnung** nicht bei der Batchverarbeitung auftreten.</span><span class="sxs-lookup"><span data-stu-id="32d2e-203">For email messages, you will not encounter a **Warning** during batch processing.</span></span> <span data-ttu-id="32d2e-204">Wenn die **ResponseClass** **erfolgreich**ist, wird das [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element, das folgt auch immer auf **NoError**festgelegt.</span><span class="sxs-lookup"><span data-stu-id="32d2e-204">If the **ResponseClass** is **Success**, the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element that follows is also always set to **NoError**.</span></span> <span data-ttu-id="32d2e-205">Wenn die **ResponseClass** **Fehler**ist, müssen Sie überprüfen Sie die Werte der [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**und [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) Elemente, die Ursache des Problems zu bestimmen.</span><span class="sxs-lookup"><span data-stu-id="32d2e-205">If the **ResponseClass** is **Error**, you need to check the values of the [MessageText](http://msdn.microsoft.com/library/59a23bdc-0d9a-4942-8b3c-9cdb11db1ab1%28Office.15%29.aspx), **ResponseCode**, and [MessageXml](http://msdn.microsoft.com/library/bcaf9e35-d351-48f3-baad-f90c633cba8a%28Office.15%29.aspx) elements to determine what caused the problem.</span></span> <span data-ttu-id="32d2e-206">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) wird derzeit nicht verwendet.</span><span class="sxs-lookup"><span data-stu-id="32d2e-206">[DescriptiveLinkKey](http://msdn.microsoft.com/library/f7f36749-00f3-4915-b17c-e3caa0af6e67%28Office.15%29.aspx) is currently unused.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="32d2e-207">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="32d2e-207">See also</span></span>


- [<span data-ttu-id="32d2e-208">E-Mail- und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="32d2e-208">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="32d2e-209">Senden von e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="32d2e-209">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32d2e-210">Reagieren Sie auf e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="32d2e-210">Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32d2e-211">Verschieben und Kopieren von e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="32d2e-211">Move and copy email messages by using EWS in Exchange</span></span>](how-to-move-and-copy-email-messages-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="32d2e-212">Konsequenzen für Batchanforderungen EWS-Einschränkung</span><span class="sxs-lookup"><span data-stu-id="32d2e-212">Throttling implications for EWS batch requests</span></span>](ews-throttling-in-exchange.md#bk_ThrottlingBatch)
    

