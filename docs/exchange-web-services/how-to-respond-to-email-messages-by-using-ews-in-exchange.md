---
title: Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 9d584991-4d67-4d36-ae2f-99970af8488f
description: In diesem Artikel erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.
ms.openlocfilehash: 81599051f603654cdf8a50b789b37d7e76664a53
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455709"
---
# <a name="respond-to-email-messages-by-using-ews-in-exchange"></a><span data-ttu-id="56dde-103">Antworten auf E-Mail-Nachrichten mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56dde-103">Respond to email messages by using EWS in Exchange</span></span>

<span data-ttu-id="56dde-104">In diesem Artikel erfahren Sie, wie Sie mithilfe der verwaltete EWS-API oder EWS in Exchange auf e-Mail-Nachrichten reagieren.</span><span class="sxs-lookup"><span data-stu-id="56dde-104">Learn how to respond to email messages by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="56dde-105">Sie können die verwaltete EWS-API oder EWS verwenden, um auf Nachrichten zu antworten, indem Sie Ihnen Antworten oder Sie an Empfänger weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="56dde-105">You can use the EWS Managed API or EWS to respond to messages by replying to them or forwarding them to recipients.</span></span>
  
<span data-ttu-id="56dde-106">**Tabelle 1. Verwaltete EWS-API Methoden und EWS-Vorgänge für die Reaktion auf e-Mail-Nachrichten**</span><span class="sxs-lookup"><span data-stu-id="56dde-106">**Table 1. EWS Managed API methods and EWS operations for responding to email messages**</span></span>

|<span data-ttu-id="56dde-107">**Aufgabe**</span><span class="sxs-lookup"><span data-stu-id="56dde-107">**Task**</span></span>|<span data-ttu-id="56dde-108">**EWS Managed API-Methode**</span><span class="sxs-lookup"><span data-stu-id="56dde-108">**EWS Managed API method**</span></span>|<span data-ttu-id="56dde-109">**EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="56dde-109">**EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56dde-110">Antworten auf eine e-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="56dde-110">Reply to an email message</span></span>  <br/> |[<span data-ttu-id="56dde-111">Email Message. Reply</span><span class="sxs-lookup"><span data-stu-id="56dde-111">EmailMessage.Reply</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="56dde-112">Email Message. createreply</span><span class="sxs-lookup"><span data-stu-id="56dde-112">EmailMessage.CreateReply</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56dde-113">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei das [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element von entweder [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) oder [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="56dde-113">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of either [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) or [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx).</span></span>  <br/> |
|<span data-ttu-id="56dde-114">Weiterleiten einer e-Mail-Nachricht</span><span class="sxs-lookup"><span data-stu-id="56dde-114">Forward an email message</span></span>  <br/> |[<span data-ttu-id="56dde-115">Email Message. Forward</span><span class="sxs-lookup"><span data-stu-id="56dde-115">EmailMessage.Forward</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="56dde-116">Email Message. createforward</span><span class="sxs-lookup"><span data-stu-id="56dde-116">EmailMessage.CreateForward</span></span>](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) <br/> |<span data-ttu-id="56dde-117">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), wobei das [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Element ein untergeordnetes Element von [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx)hat.</span><span class="sxs-lookup"><span data-stu-id="56dde-117">[CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx), where the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element has a child element of [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx).</span></span>  <br/> |
   
## <a name="reply-to-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="56dde-118">Antworten auf eine e-Mail-Nachricht mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="56dde-118">Reply to an email message by using the EWS Managed API</span></span>
<span data-ttu-id="56dde-119"><a name="bk_replyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="56dde-119"><a name="bk_replyewsma"> </a></span></span>

<span data-ttu-id="56dde-120">Das verwaltete EWS-API bietet zwei Methoden, mit denen Sie auf Nachrichten reagieren können: [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) und [createreply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="56dde-120">The EWS Managed API provides two methods that you can use to respond to messages: [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) and [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="56dde-121">Die **Reply** -Methode akzeptiert nur zwei Parameter: die Antwortnachricht, die dem vorhandenen Text vorangestellt werden soll, und einen **booleschen** Wert, der angibt, ob die Antwort an alle Empfänger (true) oder nur an den Absender (false) gesendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56dde-121">The **Reply** method only takes two parameters: the response message to prepend to the existing body, and a **Boolean** value that indicates whether the response should go to all recipients (true) or just the sender (false).</span></span> <span data-ttu-id="56dde-122">Wenn Sie einer Nachricht zusätzliche Empfänger hinzufügen müssen, zusätzliche Eigenschaften für eine Antwort festlegen oder eine Anlage hinzufügen möchten, verwenden Sie die **createreply** -Methode, mit der Sie alle [Eigenschaften der First-Klasse](email-properties-and-elements-in-ews-in-exchange.md) festlegen können, die für ein [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="56dde-122">If you need to add additional recipients to a message, set additional properties on a response, or add an attachment, use the **CreateReply** method, which enables you to set all the [first-class properties](email-properties-and-elements-in-ews-in-exchange.md) that are available on an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="56dde-123">Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **Reply** -Methode auf eine e-Mail-Nachricht reagieren.</span><span class="sxs-lookup"><span data-stu-id="56dde-123">The following code example shows how to use the **Reply** method to respond to an email message.</span></span> 
  
<span data-ttu-id="56dde-124">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-124">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="56dde-125">Die lokale Variable *ItemID* ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, auf das reagiert werden soll.</span><span class="sxs-lookup"><span data-stu-id="56dde-125">The local variable  *ItemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to respond to.</span></span> <span data-ttu-id="56dde-126">Im Beispiel wird die [FindRecentlySent-Methode](#bk_findlast) aufgerufen, um zu überprüfen, ob die Nachricht als beantwortet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-126">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as replied to.</span></span> 
  
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

<span data-ttu-id="56dde-127">Im folgenden Codebeispiel wird veranschaulicht, wie die **createreply** -Methode verwendet wird, um auf eine e-Mail-Nachricht zu antworten.</span><span class="sxs-lookup"><span data-stu-id="56dde-127">The following code example shows how to use the **CreateReply** method to respond to an email message.</span></span> 
  
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

<span data-ttu-id="56dde-128">Wenn Sie eine Anlage zur Antwortnachricht hinzufügen müssen, ersetzen Sie den Aufruf der **SendAndSaveCopy** -Methode durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="56dde-128">If you need to add an attachment to the response message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage reply = responseMessage.Save();
reply.Attachments.AddFileAttachment("attachmentname.txt");
reply.Update(ConflictResolutionMode.AutoResolve);
reply.SendAndSaveCopy();
```

## <a name="reply-to-an-email-message-by-using-ews"></a><span data-ttu-id="56dde-129">Antworten auf eine e-Mail-Nachricht mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="56dde-129">Reply to an email message by using EWS</span></span>
<span data-ttu-id="56dde-130"><a name="bk_replyews"> </a></span><span class="sxs-lookup"><span data-stu-id="56dde-130"><a name="bk_replyews"> </a></span></span>

<span data-ttu-id="56dde-131">Im folgenden Codebeispiel wird gezeigt, wie eine Nachricht mithilfe von EWS beantwortet wird.</span><span class="sxs-lookup"><span data-stu-id="56dde-131">The following code example shows how to reply to a message by using EWS.</span></span> <span data-ttu-id="56dde-132">Verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgang, wobei das **MessageDisposition** -Attribut auf **SendAndSaveCopy** festgelegt ist, um die Nachricht zu senden und die Antwort im Ordner "Gesendete Elemente" zu speichern.</span><span class="sxs-lookup"><span data-stu-id="56dde-132">Use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="56dde-133">Fügen Sie das [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) -Element als untergeordnetes Element des [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) -Elements ein, das jeder Person im Nachrichtenthread antworten soll, oder fügen Sie das [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) -Element hinzu, um nur dem Absender zu antworten.</span><span class="sxs-lookup"><span data-stu-id="56dde-133">Include either the [ReplyAllToItem](https://msdn.microsoft.com/library/8ca970ca-ca73-40db-9233-7b271cc5f44f%28Office.15%29.aspx) element as a child of the [Items](https://msdn.microsoft.com/library/d61ef1cc-ddfc-480a-9625-7b436cb33ae0%28Office.15%29.aspx) element to reply to everyone on the message thread, or include the [ReplyToItem](https://msdn.microsoft.com/library/35ee751a-41c0-4216-ad8b-78f7ada43a2f%28Office.15%29.aspx) element to reply only to the sender.</span></span> 
  
<span data-ttu-id="56dde-134">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn die [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) -oder die [createreply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56dde-134">This is also the XML request that the EWS Managed API sends when calling either the [Reply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.reply%28v=exchg.80%29.aspx) or the [CreateReply](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createreply%28v=exchg.80%29.aspx) method.</span></span> 
  
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

<span data-ttu-id="56dde-135">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die Antwort erstellt und erfolgreich gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-135">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the reply was created and sent successfully.</span></span>
  
<span data-ttu-id="56dde-136">Wenn Sie eine Anlage zur Antwortnachricht hinzufügen müssen, rufen Sie den **CreateItem** -Vorgang wie oben angegeben auf, ändern Sie jedoch die **MessageDisposition** in **SaveOnly**.</span><span class="sxs-lookup"><span data-stu-id="56dde-136">If you need to add an attachment to your response message, call the **CreateItem** operation as specified above, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="56dde-137">Rufen Sie dann den [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von der [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Operation auf.</span><span class="sxs-lookup"><span data-stu-id="56dde-137">Then call the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="forward-an-email-message-by-using-the-ews-managed-api"></a><span data-ttu-id="56dde-138">Weiterleiten einer e-Mail-Nachricht mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="56dde-138">Forward an email message by using the EWS Managed API</span></span>
<span data-ttu-id="56dde-139"><a name="bk_forwardewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="56dde-139"><a name="bk_forwardewsma"> </a></span></span>

<span data-ttu-id="56dde-140">Das verwaltete EWS-API stellt zwei Methoden bereit, die Sie zum Weiterleiten von Nachrichten verwenden können: [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) und [createforward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="56dde-140">The EWS Managed API provides two methods that you can use to forward messages: [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) and [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx).</span></span> <span data-ttu-id="56dde-141">Die **Forward** -Methode benötigt nur zwei Parameter: die Nachricht, die dem vorhandenen Text vorangestellt werden soll, und ein Array oder eine Auflistung von Empfängern, je nach der zu verwendenden Überladung.</span><span class="sxs-lookup"><span data-stu-id="56dde-141">The **Forward** method only takes two parameters: the message to prepend to the existing body, and an array or collection of recipients, depending on the overload you choose to use.</span></span> <span data-ttu-id="56dde-142">Wenn Sie der weiterzuleitenden Nachricht eine Anlage hinzufügen oder zusätzliche Eigenschaften für die neue Nachricht festlegen möchten, verwenden Sie die **createforward** -Methode, mit der Sie alle Eigenschaften festlegen können, die für ein [Email Message](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) -Objekt verfügbar sind.</span><span class="sxs-lookup"><span data-stu-id="56dde-142">If you need to add an attachment to the message you're forwarding, or set additional properties on the new message, use the **CreateForward** method, which enables you to set all the properties that are available on an [EmailMessage](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage%28v=exchg.80%29.aspx) object.</span></span> 
  
<span data-ttu-id="56dde-143">Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **Forward** -Methode eine e-Mail-Nachricht an einen Empfänger weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="56dde-143">The following code example shows how to use the **Forward** method to forward an email message to one recipient.</span></span> 
  
<span data-ttu-id="56dde-144">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-144">This example assumes that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> <span data-ttu-id="56dde-145">Die lokale Variable *ItemID* ist die [ID](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) des Elements, das weitergeleitet werden soll.</span><span class="sxs-lookup"><span data-stu-id="56dde-145">The local variable  *ItemId*  is the [Id](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.item.id%28v=exchg.80%29.aspx) of the item to forward.</span></span> <span data-ttu-id="56dde-146">Im Beispiel wird die [FindRecentlySent-Methode](#bk_findlast) aufgerufen, um zu überprüfen, ob die Nachricht als weitergeleitet markiert wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-146">The example calls the [FindRecentlySent method](#bk_findlast) to verify that the message was marked as forwarded.</span></span> 
  
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

<span data-ttu-id="56dde-147">Im folgenden Codebeispiel wird gezeigt, wie Sie mit der **createforward** -Methode eine e-Mail-Nachricht an einen Empfänger weiterleiten.</span><span class="sxs-lookup"><span data-stu-id="56dde-147">The following code example shows how to use the **CreateForward** method to forward an email message to one recipient.</span></span> 
  
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

<span data-ttu-id="56dde-148">Wenn Sie eine Anlage zur weitergeleiteten Nachricht hinzufügen müssen, ersetzen Sie den Aufruf der **SendAndSaveCopy** -Methode durch den folgenden Code.</span><span class="sxs-lookup"><span data-stu-id="56dde-148">If you need to add an attachment to the forwarded message, replace the call to the **SendAndSaveCopy** method with the following code.</span></span> 
  
```cs
EmailMessage forward = forwardMessage.Save();
forward.Attachments.AddFileAttachment("attachmentname.txt");
forward.Update(ConflictResolutionMode.AutoResolve);
forward.SendAndSaveCopy();
```

## <a name="forward-an-email-message-by-using-ews"></a><span data-ttu-id="56dde-149">Weiterleiten einer e-Mail-Nachricht mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="56dde-149">Forward an email message by using EWS</span></span>
<span data-ttu-id="56dde-150"><a name="bk_forwardews"> </a></span><span class="sxs-lookup"><span data-stu-id="56dde-150"><a name="bk_forwardews"> </a></span></span>

<span data-ttu-id="56dde-151">Im folgenden Codebeispiel wird gezeigt, wie eine Nachricht mithilfe von EWS weitergeleitet wird.</span><span class="sxs-lookup"><span data-stu-id="56dde-151">The following code example shows how to forward a message by using EWS.</span></span> <span data-ttu-id="56dde-152">Verwenden Sie den [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) -Vorgang, wobei das **MessageDisposition** -Attribut auf **SendAndSaveCopy** festgelegt ist, um die Nachricht zu senden und die Antwort im Ordner "Gesendete Elemente" zu speichern.</span><span class="sxs-lookup"><span data-stu-id="56dde-152">Use the [CreateItem](https://msdn.microsoft.com/library/fe6bb7fc-8918-4e6e-b0a1-b7e0ef44c3d1%28Office.15%29.aspx) operation with the **MessageDisposition** attribute set to **SendAndSaveCopy** to send the message and save the response in the Sent Items folder.</span></span> <span data-ttu-id="56dde-153">Das [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) -Element gibt an, dass das Element eine weitergeleitete Nachricht ist.</span><span class="sxs-lookup"><span data-stu-id="56dde-153">The [ForwardItem](https://msdn.microsoft.com/library/97786086-8b91-4471-8af8-d21e8d66de87%28Office.15%29.aspx) element indicates that the item is a forwarded message.</span></span> 
  
<span data-ttu-id="56dde-154">Dies ist auch die XML-Anforderung, die vom verwaltete EWS-API gesendet wird, wenn die [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) -oder die [createforward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) -Methode aufgerufen wird.</span><span class="sxs-lookup"><span data-stu-id="56dde-154">This is also the XML request that the EWS Managed API sends when calling either the [Forward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.forward%28v=exchg.80%29.aspx) or the [CreateForward](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.emailmessage.createforward%28v=exchg.80%29.aspx) method.</span></span> 
  
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

<span data-ttu-id="56dde-155">Der Server antwortet auf die **CreateItem** -Anforderung mit einer [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) -Nachricht, die den [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Elementwert **noError**enthält, der angibt, dass die weitergeleitete Nachricht erfolgreich erstellt und gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-155">The server responds to the **CreateItem** request with a [CreateItemResponse](https://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element value of **NoError**, which indicates that the forwarded message was created and sent successfully.</span></span>
  
<span data-ttu-id="56dde-156">Wenn Sie eine Anlage zur Antwortnachricht hinzufügen müssen, rufen Sie den **CreateItem** -Vorgang auf, ändern Sie jedoch die **MessageDisposition** in **SaveOnly**.</span><span class="sxs-lookup"><span data-stu-id="56dde-156">If you need to add an attachment to your response message, call the **CreateItem** operation, but change the **MessageDisposition** to **SaveOnly**.</span></span> <span data-ttu-id="56dde-157">Rufen Sie dann den [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) -Vorgang, gefolgt von der [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) -Operation auf.</span><span class="sxs-lookup"><span data-stu-id="56dde-157">Then call the [CreateAttachment](https://msdn.microsoft.com/library/e066db95-6963-4507-a8d0-8efad287f550%28Office.15%29.aspx) operation, followed by the [SendItem](https://msdn.microsoft.com/library/337b89ef-e1b7-45ed-92f3-8abe4200e4c7%28Office.15%29.aspx) operation.</span></span> 
  
## <a name="find-the-message-last-replied-to-or-forwarded-by-using-the-ews-managed-api"></a><span data-ttu-id="56dde-158">Suchen Sie die Nachricht, die zuletzt mit dem verwaltete EWS-API beantwortet oder weitergeleitet wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-158">Find the message last replied to or forwarded by using the EWS Managed API</span></span>
<span data-ttu-id="56dde-159"><a name="bk_findlast"> </a></span><span class="sxs-lookup"><span data-stu-id="56dde-159"><a name="bk_findlast"> </a></span></span>

<span data-ttu-id="56dde-160">Im folgenden Codebeispiel wird gezeigt, wie das zuletzt ausgeführte Verb und die Uhrzeit, zu der das letzte Verb für das angegebene Element ausgeführt wurde, gefunden werden.</span><span class="sxs-lookup"><span data-stu-id="56dde-160">The following code example shows how to find the last verb executed and the time the last verb was executed on the item specified.</span></span> <span data-ttu-id="56dde-161">Diese Methode wird aus anderen verwaltete EWS-API Codebeispielen in diesem Thema aufgerufen, um sicherzustellen, dass die geantworteten oder weitergeleiteten Elemente als beantwortet oder weitergeleitet in Ihrem Posteingang markiert wurden.</span><span class="sxs-lookup"><span data-stu-id="56dde-161">This method is called from other EWS Managed API code examples in this topic to verify that the items you replied to or forwarded were marked as replied to or forwarded in your Inbox.</span></span> 
  
<span data-ttu-id="56dde-162">Im Beispiel wird die erweiterte Eigenschaft [pidtaglastverbexecuted (](https://msdn.microsoft.com/library/cc841968.aspx) (0x10820003) verwendet, um zu bestimmen, ob die Nachricht eine Antwort, eine Antwort all oder eine Forward-und die [pidtaglastverbexecutiontime (](https://msdn.microsoft.com/library/cc839918.aspx) (0x10820040)-erweiterte Eigenschaft war, um zu bestimmen, wann die Antwort oder der Forward gesendet wurde.</span><span class="sxs-lookup"><span data-stu-id="56dde-162">The example uses the [PidTagLastVerbExecuted](https://msdn.microsoft.com/library/cc841968.aspx) (0x10820003) extended property to determine whether the message was a reply, a reply all, or a forward, and the [PidTagLastVerbExecutionTime](https://msdn.microsoft.com/library/cc839918.aspx) (0x10820040) extended property to determine when the reply or forward was sent.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="56dde-163">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="56dde-163">See also</span></span>


- [<span data-ttu-id="56dde-164">E-Mail- und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56dde-164">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
    
- [<span data-ttu-id="56dde-165">Senden von E-Mail-Nachrichten mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="56dde-165">Send email messages by using EWS in Exchange</span></span>](how-to-send-email-messages-by-using-ews-in-exchange.md)
    

