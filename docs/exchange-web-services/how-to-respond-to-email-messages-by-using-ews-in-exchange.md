---
title: Reagieren Sie auf e-Mail-Nachrichten mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: Erfahren Sie, wie durch Verwenden der EWS Managed API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.
ms.openlocfilehash: 2f1428251084a7f2bf8d589a788c143f34b64d5c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756994"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="92c50-103">Reagieren Sie auf e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="92c50-103">Respond to email messages by using EWS in Exchange</span></span>

<span data-ttu-id="92c50-104">Erfahren Sie, wie durch Verwenden der EWS Managed API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.</span><span class="sxs-lookup"><span data-stu-id="92c50-104">Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="92c50-105">Der EWS Managed API oder EWS können Sie auf Nachrichten antworten, indem sie beantworten oder Weiterleiten an Empfänger.</span><span class="sxs-lookup"><span data-stu-id="92c50-105">You can use the EWS Managed API or EWS to respond to messages by replying to them or forwarding them to recipients.</span></span>
  
<span data-ttu-id="92c50-106">**In Tabelle 1. EWS Managed API-Methoden und EWS-Vorgänge für die Reaktion auf e-Mail-Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="92c50-106">**Table 1. EWS Managed API methods and EWS operations for responding to email messages**</span></span>

|<span data-ttu-id="92c50-107">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="92c50-107">**Task**</span></span>|<span data-ttu-id="92c50-108">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="92c50-108">**EWS Managed API method**</span></span>|<span data-ttu-id="92c50-109">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="92c50-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="92c50-110">Antworten Sie auf eine e-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="92c50-110">Reply to an email message</span></span>  <br/> |[<span data-ttu-id="92c50-111">EmailMessage.Reply</span><span class="sxs-lookup"><span data-stu-id="92c50-111">EmailMessage.Reply</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="92c50-112">EmailMessage.CreateReply</span><span class="sxs-lookup"><span data-stu-id="92c50-112">EmailMessage.CreateReply</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="92c50-113">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element des [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) oder [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx)hat.</span><span class="sxs-lookup"><span data-stu-id="92c50-113">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of either [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) or [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="92c50-114">Weiterleiten einer e-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="92c50-114">Forward an email message</span></span>  <br/> |[<span data-ttu-id="92c50-115">EmailMessage.Forward</span><span class="sxs-lookup"><span data-stu-id="92c50-115">EmailMessage.Forward</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="92c50-116">EmailMessage.CreateForward</span><span class="sxs-lookup"><span data-stu-id="92c50-116">EmailMessage.CreateForward</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="92c50-117">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element des [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)hat.</span><span class="sxs-lookup"><span data-stu-id="92c50-117">[CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx).</span></span>  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="92c50-118">Antworten Sie auf eine e-Mail-Nachricht mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="92c50-118">Reply to an email message by using the EWS Managed API</span></span>
<span data-ttu-id="92c50-119"><a name="bk_replyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="92c50-119"></span></span>

<span data-ttu-id="92c50-120">Die EWS Managed API bietet zwei Methoden, mit denen Sie Antworten auf Nachrichten: [Antworten](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) und [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="92c50-120">The EWS Managed API provides two methods that you can use to respond to messages: [Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) and [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="92c50-121">Die **Reply** -Methode hat nur zwei Parameter: die Antwortnachricht vorangestellt vorhandenen Text und ein **boolescher** Wert, der angibt, ob die Antwort an alle Empfänger (True) oder nur an den Absender (False) eingefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="92c50-121">The **Reply** method only takes two parameters: the response message to prepend to the existing body, and a **Boolean** value that indicates whether the response should go to all recipients (true) or just the sender (false).</span></span> <span data-ttu-id="92c50-122">Wenn Sie benötigen weitere Empfänger einer Nachricht hinzufügen zu einer Antwort zusätzliche Eigenschaften festlegen oder einer Anlage hinzufügen, verwenden Sie die **CreateReply** -Methode, wodurch Sie legen Sie alle [Eigenschaften der ersten Klasse](email-properties-and-elements-in-ews-in-exchange.md) , die auf ein ["EmailMessage" verfügbar sind ](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx)Objekt.</span><span class="sxs-lookup"><span data-stu-id="92c50-122">If you need to add additional recipients to a message, set additional properties on a response, or add an attachment, use the **CreateReply** method, which enables you to set all the [first-class properties](email-properties-and-elements-in-ews-in-exchange.md) that are available on an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="92c50-123">Im folgenden Codebeispiel wird veranschaulicht, wie die **Reply** -Methode verwenden, um auf eine e-Mail-Nachricht zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="92c50-123">The following code example shows how to use the **Reply** method to respond to an email message.</span></span> 
  
<span data-ttu-id="92c50-124">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-124">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="92c50-125">Die lokale Variable *ItemId* ist die [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements zu beantworten.</span><span class="sxs-lookup"><span data-stu-id="92c50-125">The local variable  *ItemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to respond to.</span></span> <span data-ttu-id="92c50-126">Das Beispiel ruft die [FindRecentlySent-Methode](#bk_findlast) , um sicherzustellen, dass die Nachricht als geantwortet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-126">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as replied to.</span></span> 
  
```cs
// As a best practice, limit the properties returned by the Bind method to only those that are required.
PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, ItemSchema.LastModifiedTime);
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, propSet);
string myReply = "This is the message body of the email reply.";
bool replyToAll = false;
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Reply(myReply, replyToAll);
// Verify that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="92c50-127">Im folgenden Codebeispiel wird veranschaulicht, wie die **CreateReply** -Methode verwenden, um auf eine e-Mail-Nachricht zu reagieren.</span><span class="sxs-lookup"><span data-stu-id="92c50-127">The following code example shows how to use the **CreateReply** method to respond to an email message.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
bool replyToAll = true;
ResponseMessage responseMessage = message.CreateReply(replyToAll);
// Prepend the reply to the message body. 
string myReply = "This is the message body of the email reply.";
responseMessage.BodyPrefix = myReply;
// Send the response message.
// This method call results in a CreateItem call to EWS.
responseMessage.SendAndSaveCopy();
// Check that the response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="92c50-128">Wenn Sie, um die Response-Nachricht eine Anlage hinzuzufügen müssen, ersetzen Sie den Anruf an die **SendAndSaveCopy** -Methode durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="92c50-128">If you need to add an attachment to the response message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a><span data-ttu-id="92c50-129">Antworten Sie auf eine e-Mail-Nachricht mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="92c50-129">Reply to an email message by using EWS</span></span>
<span data-ttu-id="92c50-130"><a name="bk_replyews"> </a></span><span class="sxs-lookup"><span data-stu-id="92c50-130"></span></span>

<span data-ttu-id="92c50-131">Im folgenden Codebeispiel wird veranschaulicht, wie mithilfe der Exchange-Webdienste auf eine Nachricht zu antworten.</span><span class="sxs-lookup"><span data-stu-id="92c50-131">The following code example shows how to reply to a message by using EWS.</span></span> <span data-ttu-id="92c50-132">Verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) Operation mit dem festgelegten **SendAndSaveCopy** **"MessageDisposition"** -Attribut senden die Nachricht, und speichern die Antwort im Ordner "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="92c50-132">Use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="92c50-133">Das [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) -Element als untergeordnetes Element des Elements [Elemente](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) für alle Benutzer in der Nachricht Thread Antworten enthalten, oder das [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) -Element, um nur dem Absender Antworten enthalten.</span><span class="sxs-lookup"><span data-stu-id="92c50-133">Include either the [ReplyAllToItem](http://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) element as a child of the [Items](http://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element to reply to everyone on the message thread, or include the [ReplyToItem](http://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) element to reply only to the sender.</span></span> 
  
<span data-ttu-id="92c50-134">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn die [Antwort](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) oder die [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="92c50-134">This is also the XML request that the EWS Managed API sends when calling either the [Reply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) or the [CreateReply](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) method.</span></span> 
  
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
    <m:CreateItem MessageDisposition="SendAndSaveCopy">
      <m:Items>
        <t:ReplyAllToItem>
          <t:ReferenceItemId Id="AAMkADE4="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the email reply.</t:NewBodyContent>
        </t:ReplyAllToItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="92c50-135">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die Antwort erstellt und erfolgreich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-135">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the reply was created and sent successfully.</span></span>
  
<span data-ttu-id="92c50-136">Wenn Sie Ihre Antwortnachricht eine Anlage hinzufügen möchten, rufen Sie die **CreateItem** Operation wie oben angegeben, aber ändern Sie die **"MessageDisposition"** in **SaveOnly**.</span><span class="sxs-lookup"><span data-stu-id="92c50-136">If you need to add an attachment to your response message, call the **CreateItem** operation as specified above, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="92c50-137">Rufen Sie dann den [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="92c50-137">Then call the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="92c50-138">Weiterleiten einer e-Mail-Nachricht mithilfe der EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="92c50-138">Forward an email message by using the EWS Managed API</span></span>
<span data-ttu-id="92c50-139"><a name="bk_forwardewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="92c50-139"></span></span>

<span data-ttu-id="92c50-140">Die EWS Managed API bietet zwei Methoden, die Sie zum Weiterleiten von Nachrichten verwenden können: [Vorwärts-](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) und [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="92c50-140">The EWS Managed API provides two methods that you can use to forward messages: [Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) and [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="92c50-141">Die **Forward** -Methode hat nur zwei Parameter: die Nachricht vorangestellt, um die vorhandenen Text und ein Array oder eine Auflistung von Empfängern, je nach der Überladung, die Sie verwenden möchten.</span><span class="sxs-lookup"><span data-stu-id="92c50-141">The **Forward** method only takes two parameters: the message to prepend to the existing body, and an array or collection of recipients, depending on the overload you choose to use.</span></span> <span data-ttu-id="92c50-142">Wenn Sie zum Hinzufügen einer Anlage an die Nachricht, die Sie weiterleiten, oder klicken Sie auf die neue Nachricht zusätzliche Eigenschaften festlegen müssen, verwenden Sie die **CreateForward** -Methode, wodurch Sie alle Eigenschaften festgelegt, die für ein Objekt ["EmailMessage"](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="92c50-142">If you need to add an attachment to the message you're forwarding, or set additional properties on the new message, use the **CreateForward** method, which enables you to set all the properties that are available on an [EmailMessage](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="92c50-143">Im folgenden Codebeispiel wird veranschaulicht, wie die **Forward** -Methode verwendet, an einen Empfänger eine e-Mail-Nachricht weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="92c50-143">The following code example shows how to use the **Forward** method to forward an email message to one recipient.</span></span> 
  
<span data-ttu-id="92c50-144">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-144">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="92c50-145">Die lokale Variable *ItemId* ist die [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, weiterzuleiten.</span><span class="sxs-lookup"><span data-stu-id="92c50-145">The local variable  *ItemId*  is the [Id](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to forward.</span></span> <span data-ttu-id="92c50-146">Das Beispiel ruft die [FindRecentlySent-Methode](#bk_findlast) , um sicherzustellen, dass die Nachricht als weitergeleitet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-146">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as forwarded.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
string myForward = "This is the message body of the forwarded email.";
// Send the response message.
// This method call results in a CreateItem call to EWS.
message.Forward(myForward, "sadie@contoso.com");
// Verify that the forwarded response was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="92c50-147">Im folgenden Codebeispiel wird veranschaulicht, wie mit der **CreateForward** -Methode eine e-Mail-Nachricht an einen Empfänger weitergeleitet.</span><span class="sxs-lookup"><span data-stu-id="92c50-147">The following code example shows how to use the **CreateForward** method to forward an email message to one recipient.</span></span> 
  
```cs
// Bind to the email message to reply to by using the ItemId.
// This method call results in a GetItem call to EWS.
EmailMessage message = EmailMessage.Bind(service, ItemId, BasePropertySet.IdOnly);
// Create the reply response message from the original email message.
// Indicate whether the message is a reply or reply all type of reply.
ResponseMessage forwardMessage = message.CreateForward();
// Set properties on the email message.
forwardMessage.ToRecipients.Add("sadie@contoso.com");
forwardMessage.Body = "Sadie,<br><br>I thought you'd be interested in this thread.<br><br>-Mack";
// Send and save a copy of the replied email message in the default Sent Items folder. 
forwardMessage.SendAndSaveCopy();
// Verify that the forwarded message was sent by calling FindRecentlySent.
FindRecentlySent(message);
```

<span data-ttu-id="92c50-148">Wenn Sie eine Anlage an die weitergeleitete Nachricht hinzufügen müssen, ersetzen Sie den Anruf an die **SendAndSaveCopy** -Methode durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="92c50-148">If you need to add an attachment to the forwarded message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a><span data-ttu-id="92c50-149">Weiterleiten einer e-Mail-Nachricht mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="92c50-149">Forward an email message by using EWS</span></span>
<span data-ttu-id="92c50-150"><a name="bk_forwardews"> </a></span><span class="sxs-lookup"><span data-stu-id="92c50-150"></span></span>

<span data-ttu-id="92c50-151">Im folgenden Codebeispiel wird veranschaulicht, wie eine Nachricht weiterleiten mithilfe der Exchange-Webdienste.</span><span class="sxs-lookup"><span data-stu-id="92c50-151">The following code example shows how to forward a message by using EWS.</span></span> <span data-ttu-id="92c50-152">Verwenden Sie die [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) Operation mit dem festgelegten **SendAndSaveCopy** **"MessageDisposition"** -Attribut senden die Nachricht, und speichern die Antwort im Ordner "Gesendete Elemente".</span><span class="sxs-lookup"><span data-stu-id="92c50-152">Use the [CreateItem](http://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="92c50-153">Das [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) -Element gibt an, dass das Element einer weitergeleiteten Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="92c50-153">The [ForwardItem](http://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) element indicates that the item is a forwarded message.</span></span> 
  
<span data-ttu-id="92c50-154">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn die [Weiterleiten](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) oder die [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) -Methode aufrufen.</span><span class="sxs-lookup"><span data-stu-id="92c50-154">This is also the XML request that the EWS Managed API sends when calling either the [Forward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) or the [CreateForward](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) method.</span></span> 
  
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
      <m:Items>
        <t:ForwardItem>
          <t:ToRecipients>
            <t:Mailbox>
              <t:EmailAddress>sadie@contoso.com</t:EmailAddress>
            </t:Mailbox>
          </t:ToRecipients>
          <t:ReferenceItemId Id="AAAMkADE="
                             ChangeKey="CQAAABYA" />
          <t:NewBodyContent BodyType="HTML">This is the message body of the forwarded email.</t:NewBodyContent>
        </t:ForwardItem>
      </m:Items>
    </m:CreateItem>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="92c50-155">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die enthält den Elementwert [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) **noError zurück**, der angibt, dass die weitergeleitete Nachricht erstellt und gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-155">The server responds to the **CreateItem** request with a [CreateItemResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the forwarded message was created and sent successfully.</span></span>
  
<span data-ttu-id="92c50-156">Wenn Sie Ihre Antwortnachricht eine Anlage hinzufügen möchten, rufen Sie den **CreateItem** -Vorgang, aber ändern Sie die **"MessageDisposition"** in **SaveOnly**.</span><span class="sxs-lookup"><span data-stu-id="92c50-156">If you need to add an attachment to your response message, call the **CreateItem** operation, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="92c50-157">Rufen Sie dann den [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von [den SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Vorgang.</span><span class="sxs-lookup"><span data-stu-id="92c50-157">Then call the [CreateAttachment](http://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](http://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a><span data-ttu-id="92c50-158">Hier finden Sie die Nachricht zuletzt beantwortet oder mithilfe der EWS Managed API weitergeleitet</span><span class="sxs-lookup"><span data-stu-id="92c50-158">Find the message last replied to or forwarded by using the EWS Managed API</span></span>
<span data-ttu-id="92c50-159"><a name="bk_findlast"> </a></span><span class="sxs-lookup"><span data-stu-id="92c50-159"></span></span>

<span data-ttu-id="92c50-160">Im folgenden Codebeispiel wird veranschaulicht, wie das letzte Verb ausgeführt suchen und die Uhrzeit das letzte Verb ausgeführt wurde auf das angegebene Element festgelegt.</span><span class="sxs-lookup"><span data-stu-id="92c50-160">The following code example shows how to find the last verb executed and the time the last verb was executed on the item specified.</span></span> <span data-ttu-id="92c50-161">Diese Methode wird aufgerufen, von anderen EWS Managed API-Codebeispiele in diesem Thema, um sicherzustellen, dass die Elemente an die Sie weitergeleitet oder darauf geantwortet als geantwortet markiert oder in Ihrem Posteingang weitergeleitet wurden.</span><span class="sxs-lookup"><span data-stu-id="92c50-161">This method is called from other EWS Managed API code examples in this topic to verify that the items you replied to or forwarded were marked as replied to or forwarded in your Inbox.</span></span> 
  
<span data-ttu-id="92c50-162">Im Beispiel wird die [PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) extended-Eigenschaft verwendet, um festzustellen, ob die Nachricht eine Antwort, eine allen Antworten oder eine Weiterleitung wurde und [PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) Eigenschaft erweiterten, um zu bestimmen, wann die Antworten oder Weiterleiten gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="92c50-162">The example uses the [PidTagLastVerbExecuted](http://msdn.microsoft.com/en-us/library/cc841968.aspx) (0x10820003) extended property to determine whether the message was a reply, a reply all, or a forward, and the [PidTagLastVerbExecutionTime](http://msdn.microsoft.com/en-us/library/cc839918.aspx) (0x10820040) extended property to determine when the reply or forward was sent.</span></span> 
  
```cs
public static void FindRecentlySent(EmailMessage messageToCheck)
{
    // Create extended property definitions for PidTagLastVerbExecuted and PidTagLastVerbExecutionTime.
    ExtendedPropertyDefinition PidTagLastVerbExecuted = new ExtendedPropertyDefinition(0x1081, MapiPropertyType.Integer);
    ExtendedPropertyDefinition PidTagLastVerbExecutionTime = new ExtendedPropertyDefinition(0x1082, MapiPropertyType.SystemTime);
    PropertySet propSet = new PropertySet(BasePropertySet.IdOnly, EmailMessageSchema.Subject, PidTagLastVerbExecutionTime, PidTagLastVerbExecuted);
    messageToCheck = EmailMessage.Bind(service, messageToCheck.Id, propSet);
    // Determine the last verb executed on the message and display output.
    object responseType;
    if (messageToCheck.TryGetProperty(PidTagLastVerbExecuted, out responseType))
    {
        object ReplyTime = null;
        switch (((Int32)responseType))
        {
            case 102: Console.WriteLine("A reply was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 103: Console.WriteLine("A reply all was sent to the '" + messageToCheck.Subject.ToString() + "' email message at");
                break;
            case 104: Console.WriteLine("The '" + messageToCheck.Subject.ToString() + "' email message was forwarded at");
                break;
        }
        if (messageToCheck.TryGetProperty(PidTagLastVerbExecutionTime, out ReplyTime))
        {
            Console.WriteLine(((DateTime)ReplyTime).ToString() + ".");
        }
    }
    else
    {
        Console.WriteLine("No changes were made to  '" + messageToCheck.Subject.ToString() + "'.");
    }
}
```

## <a name="see-also"></a><span data-ttu-id="92c50-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92c50-163">See also</span></span>


- [<span data-ttu-id="92c50-164">E-Mail- und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="92c50-164">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="92c50-165">Senden von e-Mail-Nachrichten mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="92c50-165">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

