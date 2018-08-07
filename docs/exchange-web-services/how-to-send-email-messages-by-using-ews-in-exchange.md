---
title: Senden von E-Mail-Nachrichten mit EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 5290fafe-8b51-4275-a27e-baf497fc969c
description: Erfahren Sie, wie neue E-Mail-Nachrichten oder Entwürfe oder eine verzögerte E-Mail-Nachricht mithilfe der verwalteten EWS-API oder mithilfe von EWS in Exchange gesendet werden.
ms.openlocfilehash: f09babfcc420d4cbc563ed6605ba555fd9f8c7e9
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: HT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756992"
---
# <a name="send-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="3ca47-103">Senden von E-Mail-Nachrichten mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ca47-103">How to: Send email messages by using EWS in Exchange</span></span>

<span data-ttu-id="3ca47-104">Erfahren Sie, wie neue E-Mail-Nachrichten oder Entwürfe oder eine verzögerte E-Mail-Nachricht mithilfe der verwalteten EWS-API oder mithilfe von EWS in Exchange gesendet werden.</span><span class="sxs-lookup"><span data-stu-id="3ca47-104">Learn how to send new or draft email messages, or to send a delayed email message by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="3ca47-105">Unabhängig davon, ob Sie die verwaltete EWS-API oder EWS verwenden, können Sie E-Mail-Nachrichten auf zweierlei Weise senden.</span><span class="sxs-lookup"><span data-stu-id="3ca47-105">Whether you are using the EWS Managed API or EWS, you can send email messages in two ways.</span></span> <span data-ttu-id="3ca47-106">Sie können entweder eine vorhandene Nachricht, z. B. eine im Ordner „Entwürfe“ gespeicherte Nachricht, senden, oder Sie können eine E-Mail in einem Schritt erstellen und senden.</span><span class="sxs-lookup"><span data-stu-id="3ca47-106">You can either send an existing message, such as a message stored in your Drafts folder, or you can create and send an email in one step.</span></span> <span data-ttu-id="3ca47-107">Die Methoden und Vorgänge, die Sie zum Senden der Nachricht verwenden, sind die gleichen, unabhängig davon, ob Sie die Nachricht sofort oder später senden.</span><span class="sxs-lookup"><span data-stu-id="3ca47-107">The methods and operations that you use to send the message are the same whether you're sending a message immediately, or sending a delayed message.</span></span>
  
<span data-ttu-id="3ca47-108">**Tabelle 1. Methoden der verwalteten EWS-API-Methoden und EWS-Vorgänge zum Senden von E-Mail-Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="3ca47-108">**Table 1. EWS Managed API methods and EWS operations for moving and copying email messages**</span></span>

|<span data-ttu-id="3ca47-109">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="3ca47-109">**Task**</span></span>|<span data-ttu-id="3ca47-110">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="3ca47-110">**EWS Managed API method**</span></span>|<span data-ttu-id="3ca47-111">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="3ca47-111">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="3ca47-112">Senden einer neuen E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3ca47-112">Send a new email message</span></span>  <br/> |[<span data-ttu-id="3ca47-113">EmailMessage.SendAndSaveCopy</span><span class="sxs-lookup"><span data-stu-id="3ca47-113">EmailMessage.SendAndSaveCopy</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="3ca47-114">CreateItem</span><span class="sxs-lookup"><span data-stu-id="3ca47-114">CreateItem</span></span>](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="3ca47-115">Senden einer vorhandenen E-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="3ca47-115">Send an email message</span></span>  <br/> |[<span data-ttu-id="3ca47-116">EmailMessage.Send</span><span class="sxs-lookup"><span data-stu-id="3ca47-116">EmailMessage.Send</span></span>](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="3ca47-117">SendItem</span><span class="sxs-lookup"><span data-stu-id="3ca47-117">SendItem</span></span>](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) <br/> |
   
## <a name="send-a-new-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="3ca47-118">Senden einer neuen E-Mail-Nachricht mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="3ca47-118">Copy an email message by using the EWS Managed API</span></span>
<span data-ttu-id="3ca47-119"><a name="bk_sendnewewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="3ca47-119"></span></span>

<span data-ttu-id="3ca47-120">Im folgenden Codebeispiel wird gezeigt, wie Sie das [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekt zum Erstellen einer E-Mail-Nachricht und die [SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode zum Senden der Nachricht an den Empfänger und zum Speichern der Nachricht im Ordner „Gesendete Objekte“ verwenden.</span><span class="sxs-lookup"><span data-stu-id="3ca47-120">The following code example shows how to use the [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message and the [SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send the message to the recipient and save the message in the Sent Items folder.</span></span> 
  
<span data-ttu-id="3ca47-121">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ca47-121">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create an email message and provide it with connection 
// configuration information by using an ExchangeService object named service.
EmailMessage message = new EmailMessage(service);
// Set properties on the email message.
message.Subject = "Company Soccer Team";
message.Body = "Are you interested in joining?";
message.ToRecipients.Add("sadie@contoso.com");
// Send the email message and save a copy.
// This method call results in a CreateItem call to EWS.
message.SendAndSaveCopy();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "' and saved in the SendItems folder.");
```

## <a name="send-a-new-email-message-by-using-ews"></a><span data-ttu-id="3ca47-122">Senden einer neuen E-Mail-Nachricht mit EWS</span><span class="sxs-lookup"><span data-stu-id="3ca47-122">Send a new email message by using EWS</span></span>
<span data-ttu-id="3ca47-123"><a name="bk_sendnewews"> </a></span><span class="sxs-lookup"><span data-stu-id="3ca47-123"></span></span>

<span data-ttu-id="3ca47-124">Im folgenden Codebeispiel wird gezeigt, wie der [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)-Vorgang mit dem**MessageDisposition**-Wert **SendAndSaveCopy** verwendet wird, um eine E-Mail-Nachricht zu erstellen, die Nachricht an den Empfänger zu senden und die Nachricht im Ordner „Gesendete Objekte“ zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3ca47-124">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with a **MessageDisposition** value of **SendAndSaveCopy** to create an email message, send the message to the recipient, and save the message in the Sent Items folder.</span></span> <span data-ttu-id="3ca47-125">Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie [eine neue E-Mail senden](#bk_sendnewewsma).</span><span class="sxs-lookup"><span data-stu-id="3ca47-125">This is also the XML request that the EWS Managed API sends when you [create an email message](#bk_sendnewewsma).</span></span>
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Company Soccer Team</t:Subject>
          <t:Body BodyType="HTML">Are you interested in joining?</t:Body>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com </t:EmailAddress>
              </t:Mailbox>
          </t:ToRecipients>
        </t:Message>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3ca47-126">Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich erstellt wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="3ca47-126">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/de-DE/library/aa580757%28v=exchg.150%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="send-a-draft-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="3ca47-127">Senden einer Entwurfs-E-Mail-Nachricht mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="3ca47-127">To send a draft message after you've updated it, see Send a draft email message by using the EWS Managed API.</span></span>
<span data-ttu-id="3ca47-128"><a name="bk_senddraftewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="3ca47-128"></span></span>

<span data-ttu-id="3ca47-129">Im folgenden Codebeispiel wird gezeigt, wie eine Nachricht gesendet wird, die im Entwurfsordner gespeichert wurde, wie unter [Erstellen einer E-Mail-Nachricht mithilfe der verwalteten EWS-API](email-and-ews-in-exchange.md#bk_createewsma) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3ca47-129">The following code example shows how to send a message that was stored in the Drafts folder, as shown in [Create an email message by using the EWS Managed API](email-and-ews-in-exchange.md#bk_createewsma).</span></span> <span data-ttu-id="3ca47-130">Verwenden Sie zunächst die [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)-Methode, um die Nachricht abzurufen, und verwenden Sie dann die [Send](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx)-Methode, um die E-Mail-Nachricht zu senden, wie im folgenden Beispiel gezeigt.</span><span class="sxs-lookup"><span data-stu-id="3ca47-130">First, use the [Bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method to retrieve the message, and then use the [Send](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.send%28v=exchg.80%29.aspx) method to send the email message, as shown in the following code example.</span></span> <span data-ttu-id="3ca47-131">Beachten Sie, dass bei dieser Methode die gesendete Nachricht nicht im Ordner „Gesendete Objekte“ gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="3ca47-131">Note that this method does not save the sent message in the Sent Items folder.</span></span> 
  
<span data-ttu-id="3ca47-132">In diesem Fall werden die Eigenschaften [EmailMessageSchema.Subject](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) und [EmailMessageSchema.ToRecipients](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) dem [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) hinzugefügt, damit die Werte in die Konsolenausgabe eingeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="3ca47-132">In this case, the [EmailMessageSchema.Subject](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.itemschema.subject%28v=exchg.80%29.aspx) and [EmailMessageSchema.ToRecipients](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessageschema.torecipients%28v=exchg.80%29.aspx) properties are added to the [PropertySet](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.propertyset%28v=exchg.80%29.aspx) so that the values can be included in the console output.</span></span> 
  
<span data-ttu-id="3ca47-133">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ca47-133">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// As a best practice, create a property set that limits the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, EmailMessageSchema.ToRecipients);
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
// Send the email message.
// This method call results in a SendItem call to EWS.
message.Send();
Console.WriteLine("An email with the subject '" + message.Subject + "' has been sent to '" + message.ToRecipients[0] + "'.");
```

## <a name="send-a-draft-email-message-by-using-ews"></a><span data-ttu-id="3ca47-134">Senden einer Entwurfs-E-Mail-Nachricht mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="3ca47-134">To send a draft message after you've updated it, see Send a draft email message by using EWS.</span></span>
<span data-ttu-id="3ca47-135"><a name="bk_senddraftews"> </a></span><span class="sxs-lookup"><span data-stu-id="3ca47-135"></span></span>

<span data-ttu-id="3ca47-136">Die folgenden Codebeispiele zeigen, wie eine Nachricht gesendet wird, die zuvor im Ordner „Entwürfe“ gespeichert wurde, wie in [Erstellen eine E-Mail-Nachricht mithilfe von EWS](email-and-ews-in-exchange.md#bk_createews) dargestellt.</span><span class="sxs-lookup"><span data-stu-id="3ca47-136">The following code examples show how to send a message that was previously stored in the Drafts folder, as shown in [Create an email message by using EWS](email-and-ews-in-exchange.md#bk_createews).</span></span> <span data-ttu-id="3ca47-137">Verwenden Sie zuerst den [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx)-Vorgang, um die zu sendende E-Mail abzurufen.</span><span class="sxs-lookup"><span data-stu-id="3ca47-137">First use the [GetItem](http://msdn.microsoft.com/library/e8492e3b-1c8d-4b14-8070-9530f8306edd%28Office.15%29.aspx) operation to retrieve the email message to send.</span></span> <span data-ttu-id="3ca47-138">Verwenden Sie dann den [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx)-Vorgang, um die E-Mail an Empfänger zu senden und sie im Ordner „Entwürfe“ zu speichern.</span><span class="sxs-lookup"><span data-stu-id="3ca47-138">Then use the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation to send the email message to recipients and save it in the Sent Items folder.</span></span> 
  
<span data-ttu-id="3ca47-139">Die erste Nachricht, die **GetItem**-Anforderungsnachricht, gibt die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) des Entwurfs für die Bindung an, und die Elemente im [ItemShape](http://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx)-Element beschränken die Ergebnisse so, dass sie in die **GetItem**-Antwort eingeschlossen werden können.</span><span class="sxs-lookup"><span data-stu-id="3ca47-139">The first message, the **GetItem** request message, specifies the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the draft email message to bind to, and elements in the [ItemShape](http://msdn.microsoft.com/library/c5604161-bbc0-40bc-ad75-ff7e837d745f%28Office.15%29.aspx) element limit the results to include in the **GetItem** response.</span></span> <span data-ttu-id="3ca47-140">Das **ItemShape**-Element weist die [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) **IdOnly** auf, und das [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx)-Element umfasst die [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx)-Werte für die **Subject**-Eigenschaft aus dem Item-Schema und die **ToRecipients**-Eigenschaft aus dem Message-Schema, was bedeutet, dass nur die Elemente **ItemId**, [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx) und [ToRecipients](http://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) in der Antwort an den Client zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="3ca47-140">The **ItemShape** element has a [BaseShape](http://msdn.microsoft.com/library/42c04f3b-abaa-4197-a3d6-d21677ffb1c0%28Office.15%29.aspx) of **IdOnly**, and the [AdditionalProperties](http://msdn.microsoft.com/library/7a269aed-dcfd-4c3e-9e14-094e53828101%28Office.15%29.aspx) element includes the [FieldURI](http://msdn.microsoft.com/library/24af8e3b-3074-4c8c-8d0a-52446508d044%28Office.15%29.aspx) values for the **Subject** property from the Item schema and the **ToRecipients** property from the Message schema, which means that only the **ItemId**, [Subject](http://msdn.microsoft.com/library/c140d6c2-deb1-4f67-a908-9397197c4ae7%28Office.15%29.aspx), and [ToRecipients](http://msdn.microsoft.com/library/72dc3be8-30bb-4ae1-acf4-fb94ff490631%28Office.15%29.aspx) elements will be returned to the client in the response.</span></span> <span data-ttu-id="3ca47-141">Weitere Informationen zur Einschränkung der in Aufrufen zurückgegebenen Werte und zur Bedeutung des **BaseShape**-Elements finden Sie unter [Eigenschaftensätze und Antwortshapes in EWS in Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="3ca47-141">For more information about limiting the values returned in calls and the meaning of the **BaseShape** element, see [Property sets and response shapes in EWS in Exchange](property-sets-and-response-shapes-in-ews-in-exchange.md).</span></span>
  
<span data-ttu-id="3ca47-142">Dies ist auch die XML-Anforderung, die von der verwalteten EWS-API gesendet wird, wenn die [bind](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx)-Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="3ca47-142">This is also the XML request that is sent by the EWS Managed API when calling the [Copy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.bind%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="3ca47-143">Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="3ca47-143">The values of some attributes and elements have been shortened for readability.</span></span> 
  
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
        <t:ItemId Id="AAMkADE4=" />
      </m:ItemIds>
    </m:GetItem>
  </soap:Body>
</soap:Envelope>
```

Das folgende Beispiel zeigt die XML-Antwort, die der Server zurückgibt, nachdem der **GetItem**-Vorgang verarbeitet wurde. Die Antwort weist darauf hin, dass die E-Mail-Nachricht erfolgreich abgerufen wurde, und enthält, wie angefordert, die Elemente **Subject** und **ToRecipient**. <span data-ttu-id="3ca47-146">Die Werte einiger Attribute und Elemente wurden zur besseren Lesbarkeit gekürzt.</span><span class="sxs-lookup"><span data-stu-id="3ca47-146">The values of some attributes and elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="842"
                         MinorBuildNumber="10"
                         Version="V2_8"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetItemResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetItemResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Items>
            <t:Message>
              <t:ItemId Id="AAMkADE4="
                        ChangeKey="CQAAABYA" />
              <t:Subject>Project priorities</t:Subject>
              <t:ToRecipients>
                <t:Mailbox>
                  <t:Name>sadie@contoso.com</t:Name>
                  <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
                  <t:RoutingType>SMTP</t:RoutingType>
                  <t:MailboxType>OneOff</t:MailboxType>
                </t:Mailbox>
              </t:ToRecipients>
            </t:Message>
          </m:Items>
        </m:GetItemResponseMessage>
      </m:ResponseMessages>
    </m:GetItemResponse>
  </s:Body>
</s:Envelope>
```

<span data-ttu-id="3ca47-147">Die zweite Nachricht, die **SendItem**-Anforderungsnachricht, gibt die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der zu sendenden E-Mail sowie die [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) an, die den Ordner angibt, in dem das gesendete Objekt gespeichert werden soll.</span><span class="sxs-lookup"><span data-stu-id="3ca47-147">The second message, the **SendItem** request message, specifies the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the email message to send, as well as the [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx), which specifies the folder in which to save the sent item.</span></span>
  
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
    <m:SendItem SaveItemToFolder="true">
      <m:ItemIds>
        <t:ItemId Id="AAMkADE4="
                  ChangeKey="CQAAABYA" />
      </m:ItemIds>
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
    </m:SendItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="3ca47-148">Der Server antwortet auf die **SendItem**-Anforderung mit einer [SendItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** enthält, was darauf hinweist, dass die E-Mail erfolgreich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="3ca47-148">The server responds to the **CopyItem** request with a [CopyItemResponse](http://msdn.microsoft.com/library/26ac41c7-57d9-473e-ab7a-bae93e1d2aba%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email message was copied successfully.</span></span>
  
## <a name="send-a-delayed-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="3ca47-149">Senden einer verzögerten E-Mail-Nachricht mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="3ca47-149">Move an email message by using the EWS Managed API</span></span>
<span data-ttu-id="3ca47-150"><a name="bk_senddelayedewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="3ca47-150"></span></span>

<span data-ttu-id="3ca47-151">Im folgenden Codebeispiel wird gezeigt, wie das [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)-Objekt zum Erstellen einer E-Mail-Nachricht, die [ExtendedPropertyDefinition](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx)-Klasse zum Erstellen einer Eigenschaftsdefinition für die [PidTagDeferredSendTime](http://msdn.microsoft.com/de-DE/library/cc840017.aspx)-Eigenschaft (0x3FEF0040) und die [SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx)-Methode zum Senden einer verzögerten Nachricht und zum Speichern der Nachricht im Ordner „Entwürfe“ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ca47-151">The following code example shows how to use the [EmailMessage](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object to create an email message, the [ExtendedPropertyDefinition](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.extendedpropertydefinition%28v=exchg.80%29.aspx) class to create a property definition for the [PidTagDeferredSendTime](http://msdn.microsoft.com/de-DE/library/cc840017.aspx) (0x3FEF0040) property, and the [SendAndSaveCopy](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.emailmessage.sendandsavecopy%28v=exchg.80%29.aspx) method to send a delayed message and save the message in the Sent Items folder.</span></span> 
  
<span data-ttu-id="3ca47-152">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und dass der Benutzer mit einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="3ca47-152">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-DE/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
// Create a new email message. 
EmailMessage message = new EmailMessage(service);
// Specify the email recipient and subject. 
message.ToRecipients.Add("sadie@contoso.com");
message.Subject = "Delayed email";
// Identify the extended property that can be used to specify when to send the email. 
ExtendedPropertyDefinition PidTagDeferredSendTime = new ExtendedPropertyDefinition(16367, MapiPropertyType.SystemTime);
// Set the time that will be used to specify when the email is sent. 
// In this example, the email will be sent one minute after the next line executes, 
// provided that the message.SendAndSaveCopy request is processed by the server within one minute. 
string sendTime = DateTime.Now.AddMinutes(1).ToUniversalTime().ToString();
// Specify when to send the email by setting the value of the extended property. 
message.SetExtendedProperty(PidTagDeferredSendTime, sendTime);
// Specify the email body. 
StringBuilder str = new StringBuilder();
str.AppendLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
str.AppendLine("The email message will be sent at: " + sendTime + ".");
message.Body = str.ToString();
Console.WriteLine("");
Console.WriteLine("The client submitted the SendAndSaveCopy request at: " + DateTime.Now.ToUniversalTime().ToString() + ".");
Console.WriteLine("The email message will be sent at: " + sendTime + ".");
// Submit the request to send the email message. 
message.SendAndSaveCopy();
```

## <a name="send-a-delayed-email-message-by-using-ews"></a><span data-ttu-id="3ca47-153">Senden einer verzögerten E-Mail-Nachricht mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="3ca47-153">Send a delayed email message by using EWS</span></span>
<span data-ttu-id="3ca47-154"><a name="bk_senddelayedews"> </a></span><span class="sxs-lookup"><span data-stu-id="3ca47-154"></span></span>

<span data-ttu-id="3ca47-155">Im folgenden Codebeispiel wird gezeigt, wie der [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx)-Vorgang mit dem **MessageDisposition**-Wert **SendAndSaveCopy** zum Erstellen einer E-Mail-Nachricht, das [ ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx)-Element zum Erstellen einer Eigenschaftsdefinition für die [PidTagDeferredSendTime](http://msdn.microsoft.com/de-DE/library/cc840017.aspx)-Eigenschaft (0x3FEF0040) zum Festlegen einer Uhrzeit für das Senden der Nachricht und das [ SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx)-Element zum Speichern der gesendeten Nachricht im Ordner „Gesendete Objekte“ verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="3ca47-155">The following code example shows how to use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with a **MessageDisposition** value of **SendAndSaveCopy** to create an email message, the [ExtendedProperty](http://msdn.microsoft.com/library/f9701409-b620-4afe-b9ee-4c1e95507af7%28Office.15%29.aspx) element to create a property definition for the [PidTagDeferredSendTime](http://msdn.microsoft.com/de-DE/library/cc840017.aspx) (0x3FEF0040) property to set a time to send the message, and the [SavedItemFolderId](http://msdn.microsoft.com/library/4b8b475c-9ca5-48c9-acb0-8848b53be1ce%28Office.15%29.aspx) element to save the sent message in the Sent Items folder.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange207_SP1" />
  </soap:Header>
  <soap:Body>
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:SavedItemFolderId>
        <t:DistinguishedFolderId Id="sentitems" />
      </m:SavedItemFolderId>
      <m:Items>
        <t:Message>
          <t:Subject>Delayed email</t:Subject>
          <t:Body BodyType="HTML">
            The client submitted the SendAndSaveCopy request at: 1/2/2014 9:08:52 PM.
            The email message will be sent at: 1/2/2014 9:09:52 PM.
          </t:Body>
          <t:ExtendedProperty>
            <t:ExtendedFieldURI PropertyTag="16367"
                                PropertyType="SystemTime" />
            <t:Value>2014-01-02T21:09:52.000</t:Value>
          </t:ExtendedProperty>
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

<span data-ttu-id="3ca47-156">Der Server antwortet auf die **CreateItem**-Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die einen [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** umfasst, der angibt, dass die E-Mail erfolgreich erstellt wurde, und die [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) der neu erstellten Nachricht enthält.</span><span class="sxs-lookup"><span data-stu-id="3ca47-156">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError**, which indicates that the email was created successfully, and the [ItemId](http://msdn.microsoft.com/library/3350b597-57a0-4961-8f44-8624946719b4%28Office.15%29.aspx) of the newly created message.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="3ca47-157">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3ca47-157">See also</span></span>


- [<span data-ttu-id="3ca47-158">E-Mails und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ca47-158">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="3ca47-159">Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="3ca47-159">How to: Respond to email messages by using EWS in Exchange</span></span>](how-to-respond-to-email-messages-by-using-ews-in-exchange.md)
    

