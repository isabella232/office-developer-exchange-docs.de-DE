---
title: Arbeiten Sie mit Unterhaltungen im Exchange mithilfe der Exchange-Webdienste
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: 7750528c-acb2-43e5-a1e1-ee201c0e1730
description: In diesem Artikel erfahren Sie, wie Sie mit der verwalteten EWS-API oder EWS in Exchange nach Unterhaltungen suchen, Aktionen auf Unterhaltungen anwenden und Elemente in Unterhaltungen abrufen.
ms.openlocfilehash: 71ef7674086607e1544111071928f3dd74073a77
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757027"
---
# <a name="work-with-conversations-by-using-ews-in-exchange"></a><span data-ttu-id="91466-103">Arbeiten Sie mit Unterhaltungen im Exchange mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="91466-103">Work with conversations by using EWS in Exchange</span></span>

<span data-ttu-id="91466-104">In diesem Artikel erfahren Sie, wie Sie mit der verwalteten EWS-API oder EWS in Exchange nach Unterhaltungen suchen, Aktionen auf Unterhaltungen anwenden und Elemente in Unterhaltungen abrufen.</span><span class="sxs-lookup"><span data-stu-id="91466-104">Learn about how to find conversations, apply actions to conversations, and get items in conversations by using the EWS Managed API or EWS in Exchange.</span></span>
  
<span data-ttu-id="91466-p101">Im Kontext von Exchange stellen Unterhaltungen eine Möglichkeit dar, einen zusammengehörigen Satz E-Mail-Nachrichten zu gruppieren und zu verwalten. Sie können auch die Anzeige von zusammengehörigen Nachrichten ermöglichen. In Exchange werden Unterhaltungen auf Grundlage des **Message-ID**-Werts der ersten E-Mail-Nachricht in einem Thread definiert. Alle Antworten und zugehörigen Nachrichten verweisen in ihren jeweiligen **References**- und **In-Reply-To**-Kopfzeilen auf die **Message-ID**-Kopfzeile der ursprünglichen Nachricht.</span><span class="sxs-lookup"><span data-stu-id="91466-p101">In the context of Exchange, conversations are a way to group and manage a related set of email messages. They can also provide a way to view related messages. Exchange defines conversations based on the **Message-ID** value of the first email message in a thread. All replies and related messages reference the original message's **Message-ID** header in their **References** and **In-Reply-To** headers.</span></span> 
  
<span data-ttu-id="91466-109">Darüber hinaus legt Exchange innerhalb des SOAP-Umschlags für jede in einem Postfach empfangene Nachricht bestimmte Eigenschaften und Elemente fest.</span><span class="sxs-lookup"><span data-stu-id="91466-109">Additionally, inside the SOAP envelope, for each message received in a mailbox, Exchange sets specific properties and elements.</span></span>
  
<span data-ttu-id="91466-110">**Tabelle 1. Für alle E-Mail-Nachrichten festgelegte Unterhaltungseigenschaften und -elemente**</span><span class="sxs-lookup"><span data-stu-id="91466-110">**Table 1. Conversation properties and elements set on all email messages**</span></span>

|<span data-ttu-id="91466-111">**Eigenschaft in der verwalteten EWS-API**</span><span class="sxs-lookup"><span data-stu-id="91466-111">**EWS Managed API property**</span></span>|<span data-ttu-id="91466-112">**EWS-Element**</span><span class="sxs-lookup"><span data-stu-id="91466-112">**EWS element**</span></span>|<span data-ttu-id="91466-113">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91466-113">**Description**</span></span>|
|:-----|:-----|:-----|
|[<span data-ttu-id="91466-114">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="91466-114">ConversationTopic</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.conversationtopic%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="91466-115">ConversationTopic</span><span class="sxs-lookup"><span data-stu-id="91466-115">ConversationTopic</span></span>](http://msdn.microsoft.com/library/46cacf42-4039-4c8a-9b20-c42cdd9f2760%28Office.15%29.aspx) <br/> |<span data-ttu-id="91466-p102">Enthält eine normalisierte Form des Betreffwerts, der für die ursprüngliche Nachricht festgelegt wurde. Diese ist identisch mit dem **Thread-Topic**-Nachrichtenkopf. Dieser Wert ist schreibgeschützt.  </span><span class="sxs-lookup"><span data-stu-id="91466-p102">Contains a normalized form of the subject value that was set on the original message. This is the same as the **Thread-Topic** message header. This value is read-only.  </span></span><br/> |
|[<span data-ttu-id="91466-119">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="91466-119">ConversationIndex</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.emailmessage.conversationindex%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="91466-120">ConversationIndex</span><span class="sxs-lookup"><span data-stu-id="91466-120">ConversationIndex</span></span>](http://msdn.microsoft.com/library/fdf47e22-8d93-4ae4-883b-0c9f07f48724%28Office.15%29.aspx) <br/> |<span data-ttu-id="91466-p103">Stellt die Position des Elements in der Unterhaltung dar. Diese ist identisch mit dem **Thread-Index**-Nachrichtenkopf. Dieser Wert ist schreibgeschützt.  </span><span class="sxs-lookup"><span data-stu-id="91466-p103">Represents the position of the item in the conversation. This is the same as the **Thread-Index** message header. This value is read-only.  </span></span><br/> |
   
<span data-ttu-id="91466-p104">Exchange wendet den gleichen **ConversationTopic** -Wert auf Antworten auf die erste Nachricht an und aktualisiert anschließend den **ConversationIndex** -Wert so, dass er die Position der Nachricht relativ zur ursprünglichen Nachricht darstellt. Wenn sich der Betreff des E-Mail-Threads ändert, wendet Exchange einen neuen **ConversationTopic** -Wert und neue **ConversationIndex** -Werte auf die neue Unterhaltung an.</span><span class="sxs-lookup"><span data-stu-id="91466-p104">Exchange applies the same **ConversationTopic** value to replies to the first message and then updates the **ConversationIndex** value to represent the message's position relative to the original message. If the subject of the email thread changes, Exchange applies a new **ConversationTopic** value and new **ConversationIndex** values to the new conversation.</span></span> 
  
<span data-ttu-id="91466-126">**Tabelle 2. Methoden der verwalteten EWS-API und EWS-Vorgänge für die Arbeit mit Unterhaltungen**</span><span class="sxs-lookup"><span data-stu-id="91466-126">**Table 2. EWS Managed API methods and EWS operations for working with conversations**</span></span>

|<span data-ttu-id="91466-127">**Gewünschte Aktion**</span><span class="sxs-lookup"><span data-stu-id="91466-127">**In order to…**</span></span>|<span data-ttu-id="91466-128">**Zu verwendende Methode(n) der verwalteten EWS-API**</span><span class="sxs-lookup"><span data-stu-id="91466-128">**Use this EWS Managed API method or methods**</span></span>|<span data-ttu-id="91466-129">**Zu verwendender EWS-Vorgang**</span><span class="sxs-lookup"><span data-stu-id="91466-129">**Use this EWS operation**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="91466-130">Unterhaltungen suchen</span><span class="sxs-lookup"><span data-stu-id="91466-130">Find conversations</span></span>  <br/> |[<span data-ttu-id="91466-131">ExchangeService.FindConversation</span><span class="sxs-lookup"><span data-stu-id="91466-131">ExchangeService.FindConversation</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="91466-132">FindConversation</span><span class="sxs-lookup"><span data-stu-id="91466-132">FindConversation</span></span>](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="91466-133">Unterhaltungsaktionen anwenden</span><span class="sxs-lookup"><span data-stu-id="91466-133">Apply conversation actions</span></span>  <br/> |[<span data-ttu-id="91466-134">Conversation.EnableAlwaysCategorizeItems</span><span class="sxs-lookup"><span data-stu-id="91466-134">Conversation.EnableAlwaysCategorizeItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversation.enablealwayscategorizeitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-135">Conversation.EnableAlwaysDeleteItems</span><span class="sxs-lookup"><span data-stu-id="91466-135">Conversation.EnableAlwaysDeleteItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversation.enablealwaysdeleteitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-136">Conversation.EnableAlwaysMoveItems</span><span class="sxs-lookup"><span data-stu-id="91466-136">Conversation.EnableAlwaysMoveItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversation.enablealwaysmoveitems%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-137">ExchangeService.CopyItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-137">ExchangeService.CopyItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.copyitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-138">ExchangeService.DeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-138">ExchangeService.DeleteItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.deleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-139">ExchangeService.DisableAlwaysCategorizeItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-139">ExchangeService.DisableAlwaysCategorizeItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-140">ExchangeService.DisableAlwaysDeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-140">ExchangeService.DisableAlwaysDeleteItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-141">ExchangeService.DisableAlwaysMoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-141">ExchangeService.DisableAlwaysMoveItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.disablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-142">ExchangeService.EnableAlwaysCategorizeItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-142">ExchangeService.EnableAlwaysCategorizeItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.enablealwayscategorizeitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-143">ExchangeService.EnableAlwaysDeleteItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-143">ExchangeService.EnableAlwaysDeleteItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysdeleteitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-144">ExchangeService.EnableAlwaysMoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-144">ExchangeService.EnableAlwaysMoveItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.enablealwaysmoveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-145">ExchangeService.MoveItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-145">ExchangeService.MoveItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.moveitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-146">ExchangeService.SetFlagStatusForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-146">ExchangeService.SetFlagStatusForItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setflagstatusforitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-147">ExchangeService.SetReadStateForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-147">ExchangeService.SetReadStateForItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.setreadstateforitemsinconversations%28v=exchg.80%29.aspx) <br/> [<span data-ttu-id="91466-148">ExchangeService.SetRetentionPolicyForItemsInConversations</span><span class="sxs-lookup"><span data-stu-id="91466-148">ExchangeService.SetRetentionPolicyForItemsInConversations</span></span>](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.setretentionpolicyforitemsinconversations%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="91466-149">ApplyConversationAction</span><span class="sxs-lookup"><span data-stu-id="91466-149">ApplyConversationAction</span></span>](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) <br/> |
|<span data-ttu-id="91466-150">Elemente in einer oder mehreren Unterhaltungen abrufen</span><span class="sxs-lookup"><span data-stu-id="91466-150">Get items in one or more conversations</span></span>  <br/> |[<span data-ttu-id="91466-151">ExchangeService.GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="91466-151">ExchangeService.GetConversationItems</span></span>](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="91466-152">GetConversationItems</span><span class="sxs-lookup"><span data-stu-id="91466-152">GetConversationItems</span></span>](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) <br/> |

<span data-ttu-id="91466-153"><a name="bk_findewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-153"></span></span>

## <a name="find-a-conversation-by-using-the-ews-managed-api"></a><span data-ttu-id="91466-154">Suchen nach Unterhaltungen mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="91466-154">Find a conversation by using the EWS Managed API</span></span>

<span data-ttu-id="91466-p105">Zum Suchen nach Unterhaltungen können Sie die [ExchangeService.FindConversation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx)-Methode der verwalteten EWS-API verwenden, wie im folgenden Beispiel gezeigt. Dieses Beispiel ruft die ersten zehn Unterhaltungen im Posteingangsordner ab, deren Betreff das Wort "news" enthält. Anschließend werden das Thema der Unterhaltung, die Uhrzeit der letzten Zustellung und die globale eindeutige Empfängerliste im Konsolenfenster ausgegeben.</span><span class="sxs-lookup"><span data-stu-id="91466-p105">You can find conversations by using the [ExchangeService.FindConversation](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.findconversation%28v=exchg.80%29.aspx) EWS Managed API method, as shown in the following example. This example gets the first 10 conversations in the Inbox folder that have a subject that contains the word "news". The example then writes the conversation topic, last delivery time, and global unique recipient list to the console window.</span></span> 
  
<span data-ttu-id="91466-158">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="91466-158">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void FindConversation(ExchangeService service)
{
    // Create the view of conversations returned in the response. This view will return at most 10 results.
    ConversationIndexedItemView view = new ConversationIndexedItemView(10);
    // Create the query string to search for.
    String queryString = "subject:news";
    // Search the Inbox for conversations and return a results set with the specified view.
    // This method call results in a FindConversation call to EWS. 
    ICollection<Conversation> conversations = service.FindConversation(view, WellKnownFolderName.Inbox, queryString);
    // Examine properties on each conversation returned in the response.
    foreach (Conversation conversation in conversations)
    {
        Console.WriteLine("Conversation Topic: " + conversation.Topic);
        Console.WriteLine("Last Delivered: " + conversation.LastDeliveryTime.ToString());
        ApplyConversationActions(service, conversation);
        foreach (string GlUniqRec in conversation.GlobalUniqueRecipients)
        {
            Console.WriteLine("Global Unique Recipient: " + GlUniqRec);
        }
        Console.WriteLine("");
    }
}
```

<span data-ttu-id="91466-159"><a name="bk_findews"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-159"></span></span>

## <a name="find-a-conversation-by-using-ews"></a><span data-ttu-id="91466-160">Suchen nach Unterhaltungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="91466-160">Find a conversation by using EWS</span></span>

<span data-ttu-id="91466-p106">Sie können Unterhaltungen mit dem EWS-Vorgang [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) suchen, wie im folgenden Beispiel gezeigt. Dieses Beispiel ruft die ersten zehn Unterhaltungen im Posteingangsordner ab, deren Betreff das Wort "news" enthält. Dies ist außerdem die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie diese API zum [Suchen nach einer Unterhaltung](#bk_findewsma) verwenden.</span><span class="sxs-lookup"><span data-stu-id="91466-p106">You can find conversations by using the [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) EWS operation, as shown in the following example. This example gets the first ten conversations in the Inbox folder that have a subject that contains the word "news". This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [find a conversation](#bk_findewsma).</span></span>
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:FindConversation>
      <m:IndexedPageItemView MaxEntriesReturned="10"
                             Offset="0"
                             BasePoint="Beginning" />
      <m:ParentFolderId>
        <t:DistinguishedFolderId Id="inbox" />
      </m:ParentFolderId>
      <m:QueryString>subject:news</m:QueryString>
    </m:FindConversation>
  </soap:Body>
</soap:Envelope>

```

<span data-ttu-id="91466-p107">Der Server antwortet auf die **FindConversation**-Anforderung mit einer [FindConversationResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** enthält, um anzuzeigen, dass der Vorgang erfolgreich abgeschlossen wurde. Die Antwort umfasst außerdem die einzige Unterhaltung im Postfach, deren Betreff das Wort "news" enthält.</span><span class="sxs-lookup"><span data-stu-id="91466-p107">The server responds to the **FindConversation** request with a [FindConversationResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully. The response also includes the only conversation in the mailbox that has a subject that contains the word "news".</span></span> 
  
<span data-ttu-id="91466-166">Die Elemente **ItemId**, **ChangeKey** und **ConversationId** wurden der besseren Lesbarkeit halber gekürzt.</span><span class="sxs-lookup"><span data-stu-id="91466-166">The **ItemId**, **ChangeKey**, and **ConversationId** elements have been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="883"
                         MinorBuildNumber="10"
                         Version="V2_10"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <FindConversationResponse ResponseClass="Success"
                              xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseCode>NoError</ResponseCode>
      <Conversations>
        <Conversation xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <ConversationId Id="aO2NM+Q=" />
          <ConversationTopic>Today's top news headlines</ConversationTopic>
          <UniqueRecipients>
            <String>Sadie Daniels</String>
          </UniqueRecipients>
          <GlobalUniqueRecipients>
            <String>Sadie Daniels</String>
          </GlobalUniqueRecipients>
          <UniqueUnreadSenders>
            <String>Ronnie Sturgis</String>
          </UniqueUnreadSenders>
          <GlobalUniqueUnreadSenders>
            <String>Ronnie Sturgis</String>
          </GlobalUniqueUnreadSenders>
          <UniqueSenders>
            <String>Ronnie Sturgis</String>
          </UniqueSenders>
          <GlobalUniqueSenders>
            <String>Ronnie Sturgis</String>
          </GlobalUniqueSenders>
          <LastDeliveryTime>2014-02-18T20:42:26Z</LastDeliveryTime>
          <GlobalLastDeliveryTime>2014-02-18T20:42:26Z</GlobalLastDeliveryTime>
          <HasAttachments>false</HasAttachments>
          <GlobalHasAttachments>false</GlobalHasAttachments>
          <MessageCount>1</MessageCount>
          <GlobalMessageCount>1</GlobalMessageCount>
          <UnreadCount>1</UnreadCount>
          <GlobalUnreadCount>1</GlobalUnreadCount>
          <Size>9330</Size>
          <GlobalSize>9330</GlobalSize>
          <ItemClasses>
            <ItemClass>IPM.Note</ItemClass>
          </ItemClasses>
          <GlobalItemClasses>
            <ItemClass>IPM.Note</ItemClass>
          </GlobalItemClasses>
          <Importance>Normal</Importance>
          <GlobalImportance>Normal</GlobalImportance>
          <ItemIds>
            <ItemId Id="sVCyAAA="
                    ChangeKey="CQAAAA==" />
          </ItemIds>
          <GlobalItemIds>
            <ItemId Id="sVCyAAA="
                    ChangeKey="CQAAAA==" />
          </GlobalItemIds>
          <LastModifiedTime>2014-02-18T20:42:26Z</LastModifiedTime>
          <InstanceKey>AQAAAAAAAQABAAAACbFYggAAAAA=</InstanceKey>
          <HasIrm>false</HasIrm>
          <GlobalHasIrm>false</GlobalHasIrm>
        </Conversation>
      </Conversations>
      <TotalConversationsInView>1</TotalConversationsInView>
      <IndexedOffset>1</IndexedOffset>
    </FindConversationResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="91466-167"><a name="bk_applyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-167"></span></span>

## <a name="apply-conversation-actions-by-using-the-ews-managed-api"></a><span data-ttu-id="91466-168">Anwenden von Unterhaltungsaktionen mithilfe der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="91466-168">Apply conversation actions by using the EWS Managed API</span></span>

<span data-ttu-id="91466-p108">Zum Anwenden von Unterhaltungsaktionen auf Unterhaltungen stehen zahlreiche Methoden der verwalteten EWS-API zur Verfügung, wie im folgenden Beispiel gezeigt. In diesem Beispiel werden vorhandenen Unterhaltungselementen Kategorien hinzugefügt, und die gleichen Kategorien werden auf zukünftige Elemente der Unterhaltung angewendet. Außerdem wird veranschaulicht, wie die automatische Verschiebung von Unterhaltungselementen in einen Ordner aktiviert wird. In diesem Beispiel werden Elemente in den Ordner "Drafts" verschoben.</span><span class="sxs-lookup"><span data-stu-id="91466-p108">You can apply conversation actions to a conversation by using a number of EWS Managed API methods, as shown in the following example. This example adds categories to existing items in a conversation and applies the same categories to future items in the conversation. It also shows how to enable the automatic moving of items in the conversation to a folder. In this example, items are moved to the Drafts folder.</span></span>
  
<span data-ttu-id="91466-173">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="91466-173">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
<span data-ttu-id="91466-174">Eine vollständige Liste der Methoden zur Anwendung von Unterhaltungsaktionen finden Sie in Tabelle 2.</span><span class="sxs-lookup"><span data-stu-id="91466-174">For a complete list of methods that apply conversation actions, see Table 2.</span></span>
  
```cs
static void ApplyConversationActions(ExchangeService service, Conversation conversation)
{
   // Create a list of categories to apply to a conversation.
   List<string> categories = new List<string>();
   categories.Add("Customer");
   categories.Add("System Integrator");
   // Apply categorization to all items in the conversation and process the request
   // synchronously after enabling this rule and after all item categorization has been applied. 
   // This method call results in an ApplyConversationAction call to EWS.
   conversation.EnableAlwaysCategorizeItems(categories, true);
   // Apply an always move rule to all items in the conversation and move the items
   // to the Drafts folder. Process the request asynchronously and return the response. 
   // immediately. This method call results in an ApplyConversationAction call to EWS.
   conversation.EnableAlwaysMoveItems(WellKnownFolderName.Drafts, false);
}

```

<span data-ttu-id="91466-175"><a name="bk_applyews"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-175"></span></span>

## <a name="apply-conversation-actions-by-using-ews"></a><span data-ttu-id="91466-176">Anwenden von Unterhaltungsaktionen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="91466-176">Apply conversation actions by using EWS</span></span>

<span data-ttu-id="91466-p109">Sie können Unterhaltungsaktionen wie z. B. Kategorisieren, Löschen und Verschieben mithilfe des [ApplyConversationAction](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx)-Vorgangs anwenden, wie im folgenden Beispiel gezeigt. In diesem Beispiel werden vorhandenen Unterhaltungselementen Kategorien hinzugefügt, und die gleichen Kategorien werden auf zukünftige Elemente der Unterhaltung angewendet. Außerdem wird veranschaulicht, wie die automatische Verschiebung von Unterhaltungselementen in einen Ordner aktiviert wird; in diesem Beispiel werden Elemente in den Ordner "Drafts" verschoben. Dies ist außerdem die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Sie diese API zum [Anwenden von Unterhaltungsktionen](#bk_applyewsma) verwenden.</span><span class="sxs-lookup"><span data-stu-id="91466-p109">You can apply conversation actions, such as categorize, delete, and move, by using the [ApplyConversationAction](http://msdn.microsoft.com/library/73d7943d-d361-4f8b-9948-d85f886efa1a%28Office.15%29.aspx) operation, as shown in the following example. This example adds categories to existing items in a conversation and applies the same categories to future items in the conversation. It also shows how to enable the automatic moving of items in the conversation to a folder; in this example, items are moved to the Drafts folder. This is also the XML request that the EWS Managed API sends when you use the EWS Managed API to [apply conversation actions](#bk_applyewsma).</span></span>
  
<span data-ttu-id="91466-181">Das **ConversationId**-Element wurde der besseren Lesbarkeit halber gekürzt.</span><span class="sxs-lookup"><span data-stu-id="91466-181">The **ConversationId** element has been shortened for readability.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:ApplyConversationAction>
      <m:ConversationActions>
        <t:ConversationAction>
          <t:Action>AlwaysMove</t:Action>
          <t:ConversationId Id="jG6WVpg=" />
          <t:ProcessRightAway>false</t:ProcessRightAway>
          <t:DestinationFolderId>
            <t:DistinguishedFolderId Id="drafts" />
          </t:DestinationFolderId>
        </t:ConversationAction>
      </m:ConversationActions>
    </m:ApplyConversationAction>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="91466-182">Der Server antwortet auf die **ApplyConversationAction**-Anforderung mit einer [ApplyConversationActionResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** enthält, um anzuzeigen, dass der Vorgang erfolgreich abgeschlossen wurde.</span><span class="sxs-lookup"><span data-stu-id="91466-182">The server responds to the **ApplyConversationAction** request with a [ApplyConversationActionResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully.</span></span> 

<span data-ttu-id="91466-183"><a name="bk_getitemssingleewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-183"></span></span>

## <a name="get-items-in-a-single-conversation-by-using-the-conversation-identifier-in-the-ews-managed-api"></a><span data-ttu-id="91466-184">Abrufen von Elementen in einer einzelnen Unterhaltung mithilfe der Unterhaltungs-ID in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="91466-184">Get items in a single conversation by using the conversation identifier in the EWS Managed API</span></span>

<span data-ttu-id="91466-p110">Zum Abrufen von Elementen in einer Unterhaltung können Sie die [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx)-Methode der verwalteten EWS-API verwenden. Dieses Beispiel stellt den Satz Unterhaltungsknoten für die erste Unterhaltung im Posteingang bereit. Die Element-ID, der Betreff und die Empfangszeit jedes Elements werden in der Antwort zurückgegeben, zusammen mit den Eigenschaften für Unterhaltungsindex und Index der übergeordneten Unterhaltung. Mithilfe der Unterhaltungsindexeigenschaften können Sie die Knotenhierarchie rekonstruieren.</span><span class="sxs-lookup"><span data-stu-id="91466-p110">You can get items in a conversation by using the [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method. This example provides the set of conversation nodes for the first conversation in the Inbox. The item identifier, subject, and received time for each item are returned in the response, along with the conversation index and parent conversation index properties. You can use the conversation index properties to reconstruct the node hierarchy.</span></span> 
  
<span data-ttu-id="91466-189">In diesem Beispiel werden alle Unterhaltungselemente in den Standardordnern "Delete Items" und "Drafts" ignoriert.</span><span class="sxs-lookup"><span data-stu-id="91466-189">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="91466-190">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="91466-190">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void GetConversationItemsSingleConversation(ExchangeService service)
{
   try
   {
      // Find the first item in the mailbox.
      // This method call results in an FindItem call to EWS.
      FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Inbox,
                                                         new ItemView(1));
      // Get the conversation identifier of the item. 
      ConversationId convId = results.Items[0].ConversationId;
      // Specify the properties that will be 
      // returned for the items in the conversation.
      PropertySet properties = new PropertySet(BasePropertySet.IdOnly,
                                                ItemSchema.Subject,
                                                ItemSchema.DateTimeReceived);
      // Identify the folders to ignore.
      Collection<FolderId> foldersToIgnore = new Collection<FolderId>() 
          { WellKnownFolderName.DeletedItems, WellKnownFolderName.Drafts };
      // Request the conversation items.
      // This method call results in an GetConversationItems call to EWS.
      ConversationResponse response = service.GetConversationItems(convId,
                                                   properties,
                                                  null,
                                                  foldersToIgnore,
                                                  ConversationSortOrder.TreeOrderDescending);
      // Get the synchronization state of the conversation.
      Console.WriteLine("SyncState: " + response.SyncState);
      Collection<Item> items = new Collection<Item>();
      // Process each node of conversation items.
      foreach (ConversationNode node in response.ConversationNodes)
      {
         Console.WriteLine("Parent conversation index: " + node.ParentConversationIndex);
         Console.WriteLine("Conversation index: " + node.ConversationIndex);
         Console.WriteLine("Conversation node items:");
         // Process each item in the conversation node.
         foreach (Item item in node.Items)
         {
            Console.WriteLine("   Item ID: " + item.Id.UniqueId);
            Console.WriteLine("   Subject: " + item.Subject);
            Console.WriteLine("   Received: " + item.DateTimeReceived);
            items.Add(item);
         }
      }
   }
   // This exception occurs if there is an error with the service.
   catch (ServiceResponseException srException)
   {
      Console.WriteLine(srException);
   }
}

```

<span data-ttu-id="91466-191">Es wird empfohlen, die **SyncState** -Eigenschaft für nachfolgende Anforderungen zum Abrufen von Unterhaltungselementen zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="91466-191">We recommend that you cache the **SyncState** property for subsequent requests to get items in the conversation.</span></span> 

<span data-ttu-id="91466-192"><a name="bk_getitemsmanyewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-192"></span></span>

## <a name="get-items-in-many-conversations-by-using-the-conversationrequest-object-in-the-ews-managed-api"></a><span data-ttu-id="91466-193">Abrufen von Elementen in vielen Unterhaltungen mithilfe des ConversationRequest-Objekts in der verwalteten EWS-API</span><span class="sxs-lookup"><span data-stu-id="91466-193">Get items in many conversations by using the ConversationRequest object in the EWS Managed API</span></span>

<span data-ttu-id="91466-p111">Sie können das [ConversationRequest](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx)-Objekt und die [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx)-Methode der verwalteten EWS-API verwenden, um Elemente aus zwei oder mehr Unterhaltungen abzurufen. Dieses Beispiel stellt einen Satz Unterhaltungsknoten für die ersten zwei Unterhaltungen im Posteingang bereit. Die Element-ID, der Betreff und die Empfangszeit jedes Elements werden in der Antwort zurückgegeben, zusammen mit den Eigenschaften für Unterhaltungsindex und Index der übergeordneten Unterhaltung. Mithilfe der Unterhaltungsindexeigenschaften können Sie die Knotenhierarchie rekonstruieren. In diesem Beispiel wird davon ausgegangen, dass die ersten zwei Elemente im Posteingang aus verschiedenen Unterhaltungen stammen.</span><span class="sxs-lookup"><span data-stu-id="91466-p111">You can use the [ConversationRequest](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.conversationrequest%28v=exchg.80%29.aspx) object and the [ExchangeService.GetConversationItems](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method to get items from two or more conversations. This example provides a set of conversation nodes for the first two conversations in the Inbox. The item identifier, subject, and the received time for each item will be returned in the response, along with the conversation index and parent conversation index properties. You can use the conversation index properties to reconstruct the node hierarchy. This example assumes that the first two items in the Inbox are from different conversations.</span></span> 
  
<span data-ttu-id="91466-199">In diesem Beispiel werden alle Unterhaltungselemente in den Standardordnern "Delete Items" und "Drafts" ignoriert.</span><span class="sxs-lookup"><span data-stu-id="91466-199">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="91466-200">In diesem Beispiel wird davon ausgegangen, dass **service** ein gültiges [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx)-Objekt ist und der Benutzer bei einem Exchange-Server authentifiziert wurde.</span><span class="sxs-lookup"><span data-stu-id="91466-200">This example assumes that **service** is a valid [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) object and that the user has been authenticated to an Exchange server.</span></span> 
  
```cs
static void GetConversationItemsManyConversations(ExchangeService service)
{
   try
   {
      // Find the first two items in the Inbox. This item will be used to call the GetConversationItems operation.
      // This method call results in an FindItem call to EWS.
      FindItemsResults<Item> results = service.FindItems(WellKnownFolderName.Inbox, new ItemView(2));
      // Get the conversation identifier of the first two items in the Inbox. 
      ConversationId convId1 = results.Items[0].ConversationId;
      ConversationId convId2 = results.Items[1].ConversationId;
      
      // Identify two conversation requests. 
      ConversationRequest convR1 = new ConversationRequest();
      convR1.ConversationId = convId1;
      ConversationRequest convR2 = new ConversationRequest();
      convR2.ConversationId = convId2;
      // Create a collection of conversations to fetch. 
      Collection<ConversationRequest> conversations = new Collection<ConversationRequest>();
      conversations.Add(convR1);
      conversations.Add(convR2);
      // Specify the properties that will be returned for the items in the conversation.
      PropertySet properties = new PropertySet(BasePropertySet.IdOnly,
                                                ItemSchema.Subject,
                                                ItemSchema.DateTimeReceived);
      // Identify the folders to ignore.
      Collection<FolderId> foldersToIgnore = new Collection<FolderId>() 
          { WellKnownFolderName.DeletedItems, WellKnownFolderName.Drafts };
      // Request the conversation items.
      // This method call results in an GetConversationItems call to EWS.
      ServiceResponseCollection<GetConversationItemsResponse> responses = 
          service.GetConversationItems(conversations, properties, foldersToIgnore, 
          ConversationSortOrder.TreeOrderDescending);
      // Process each conversation.
      foreach (GetConversationItemsResponse resp in responses)
      {
         // Identify the synchronization state of the conversation.
         Console.WriteLine("Sync State: " + resp.Conversation.SyncState);
         // Process each node in the conversation.
         foreach (ConversationNode node in resp.Conversation.ConversationNodes)
         {
            Console.WriteLine("Parent conversation index: " + node.ParentConversationIndex);
            Console.WriteLine("Conversation index: " + node.ConversationIndex);
            Console.WriteLine("Conversation node items:");
            // Process each item in the conversation node.
            foreach (Item item in node.Items)
            {
               Console.WriteLine("   Item ID: " + item.Id.UniqueId);
               Console.WriteLine("   Subject: " + item.Subject);
               Console.WriteLine("   Received: " + item.DateTimeReceived);
            }
         }
      }
   }
   // This exception occurs if there is an error with the service.
   catch (ServiceResponseException srException)
   { 
      Console.WriteLine(srException);
   }
}

```

<span data-ttu-id="91466-p112">Als bewährte Methode wird empfohlen, nur die Eigenschaften zurückzugeben, die von der Clientanwendung benötigt werden, statt die **FirstClassProperties** -Option für die **BasePropertySet** -Klasse zu verwenden. Es wird empfohlen, die **SyncState** -Eigenschaft für nachfolgende Anforderungen zum Abrufen von Unterhaltungselementen zwischenzuspeichern.</span><span class="sxs-lookup"><span data-stu-id="91466-p112">As a best practice, we recommend that you return only the properties that the client application requires, rather than using the **FirstClassProperties** option for the **BasePropertySet** class. We recommend that you cache the **SyncState** property for subsequent requests to get items in the conversation.</span></span> 

<span data-ttu-id="91466-203"><a name="bk_getitemsews"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-203"></span></span>

## <a name="get-items-in-conversations-by-using-the-conversation-identifier-in-ews"></a><span data-ttu-id="91466-204">Abrufen von Elementen in Unterhaltungen mithilfe der Unterhaltungs-ID in EWS</span><span class="sxs-lookup"><span data-stu-id="91466-204">Get items in conversations by using the conversation identifier in EWS</span></span>

<span data-ttu-id="91466-p113">Sie können Elemente in einer Unterhaltung mit dem EWS-Vorgang [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) abrufen. Dieses Beispiel stellt einen Satz Unterhaltungsknoten für die erste Unterhaltung im Posteingang bereit. Die Element-ID, der Betreff und die Empfangszeit jedes Elements werden in der Antwort zurückgegeben, zusammen mit den Eigenschaften für Unterhaltungsindex und Index der übergeordneten Unterhaltung. Mithilfe der Unterhaltungsindexeigenschaften können Sie die Knotenhierarchie rekonstruieren.</span><span class="sxs-lookup"><span data-stu-id="91466-p113">You can get items in a conversation by using the [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS operation. This example provides a set of conversation nodes for the first conversation in the Inbox. The item identifier, subject, and received time for each item are returned in the response, along with the conversation index and parent conversation index properties. You can use the conversation index properties to reconstruct the node hierarchy.</span></span> 
  
<span data-ttu-id="91466-209">In diesem Beispiel werden alle Unterhaltungselemente in den Standardordnern "Delete Items" und "Drafts" ignoriert.</span><span class="sxs-lookup"><span data-stu-id="91466-209">In this example, all conversation items in the default Deleted Items and Drafts folders are ignored.</span></span>
  
<span data-ttu-id="91466-210">Das **ConversationId**-Element wurde der besseren Lesbarkeit halber gekürzt.</span><span class="sxs-lookup"><span data-stu-id="91466-210">The **ConversationId** element has been shortened for readability.</span></span> 
  
<span data-ttu-id="91466-211">Um Elemente aus mehreren Unterhaltungen abzurufen, schließen Sie zusätzliche **Conversation**-Elemente ein.</span><span class="sxs-lookup"><span data-stu-id="91466-211">To get items from more than one conversation, include additional **Conversation** elements.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
               xmlns:m=http://schemas.microsoft.com/exchange/services/2006/messages
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types"
               xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Header>
    <t:RequestServerVersion Version="Exchange2013" />
  </soap:Header>
  <soap:Body>
    <m:GetConversationItems>
      <m:ItemShape>
        <t:BaseShape>IdOnly</t:BaseShape>
        <t:AdditionalProperties>
          <t:FieldURI FieldURI="item:Subject" />
          <t:FieldURI FieldURI="item:DateTimeReceived" />
        </t:AdditionalProperties>
      </m:ItemShape>
      <m:FoldersToIgnore>
        <t:DistinguishedFolderId Id="deleteditems" />
        <t:DistinguishedFolderId Id="drafts" />
      </m:FoldersToIgnore>
      <m:SortOrder>TreeOrderDescending</m:SortOrder>
      <m:Conversations>
        <t:Conversation>
          <t:ConversationId Id="LUQFH6Q=" />
        </t:Conversation>
      </m:Conversations>
    </m:GetConversationItems>
  </soap:Body>
</soap:Envelope>
```

<span data-ttu-id="91466-p114">Der Server antwortet auf die **GetConversationItems**-Anforderung mit einer [GetConversationItemsResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx)-Nachricht, die den [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx)-Wert **NoError** enthält, um anzuzeigen, dass der Vorgang erfolgreich abgeschlossen wurde. Die Antwort umfasst außerdem die [ConversationNodes](http://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx) in der Unterhaltung.</span><span class="sxs-lookup"><span data-stu-id="91466-p114">The server responds to the **GetConversationItems** request with a [GetConversationItemsResponse](http://msdn.microsoft.com/library/742a46a0-2475-45a0-b44f-90639a3f5a43%28Office.15%29.aspx) message that includes a [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) value of **NoError** to indicate that the operation completed successfully. The response also includes the [ConversationNodes](http://msdn.microsoft.com/library/5c8a35b8-a940-4b3e-8768-9ba95766fd79%28Office.15%29.aspx) in the conversation.</span></span> 
  
<span data-ttu-id="91466-214">Die Elemente **ItemId**, **SyncState** und **ConversationId** wurden der besseren Lesbarkeit halber gekürzt.</span><span class="sxs-lookup"><span data-stu-id="91466-214">The **ItemId**, **SyncState**, and **ConversationId** elements have been shortened for readability.</span></span> 
  
```XML
<s:Envelope xmlns:s="http://schemas.xmlsoap.org/soap/envelope/">
  <s:Header>
    <h:ServerVersionInfo MajorVersion="15"
                         MinorVersion="0"
                         MajorBuildNumber="873"
                         MinorBuildNumber="9"
                         Version="V2_9"
                         xmlns:h="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/types"
                         xmlns:xsd="http://www.w3.org/2001/XMLSchema"
                         xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" />
  </s:Header>
  <s:Body xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance"
          xmlns:xsd="http://www.w3.org/2001/XMLSchema">
    <m:GetConversationItemsResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages"
                                    xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
      <m:ResponseMessages>
        <m:GetConversationItemsResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:Conversation>
            <t:ConversationId Id="LUQFH6Q=" />
            <t:SyncState>AAAAYAm1</t:SyncState>
            <t:ConversationNodes>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;994051d7c1a346efbfce8dec2cbad509
                    @SN2SR01MB006.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="AYB1NAAA="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYCHq" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T13:15:00Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;6a8e7658524b41cda7cdc3f23c1074a5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="lQAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAu8" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T10:02:08Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;bcdb185495834370a874a1e7ebedbb96
                    @SN2SR01MB005.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6
                    @SN2SR01MB006.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="igAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAuj" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T16:20:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;e52a4de6b98d484887e141da094a2ce6
                    @SN2SR01MB006.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;f0db3ead01db4fe087d98022149aa16f
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="iwAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAul" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T15:30:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;f0db3ead01db4fe087d98022149aa16f
                    @SN2SR01MB001.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;88b1884ecaaa4f68b081c009d827e8c6
                    @SN2SR01MB003.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="jQAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAuq" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T14:20:10Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
              <t:ConversationNode>
                <t:InternetMessageId>&amp;lt;88b1884ecaaa4f68b081c009d827e8c6
                    @SN2SR01MB003.com&amp;gt;</t:InternetMessageId>
                <t:ParentInternetMessageId>&amp;lt;faa2b1df30074380abe3527b0cd18ca5
                    @SN2SR01MB001.com&amp;gt;</t:ParentInternetMessageId>
                <t:Items>
                  <t:Message>
                    <t:ItemId Id="kAAAAA=="
                              ChangeKey="CQAAABYAAAD/oydcA+SPQZGbKWNyvNIZAAAAYAux" />
                    <t:Subject>RE: Review Proposal for Tailspin Toys</t:Subject>
                    <t:DateTimeReceived>2014-01-02T12:52:09Z</t:DateTimeReceived>
                  </t:Message>
                </t:Items>
              </t:ConversationNode>
            </t:ConversationNodes>
          </m:Conversation>
        </m:GetConversationItemsResponseMessage>
      </m:ResponseMessages>
    </m:GetConversationItemsResponse>
  </s:Body>
</s:Envelope>

```

<span data-ttu-id="91466-215"><a name="bk_versiondiffs"> </a></span><span class="sxs-lookup"><span data-stu-id="91466-215"></span></span>

## <a name="version-differences"></a><span data-ttu-id="91466-216">Versionsunterschiede</span><span class="sxs-lookup"><span data-stu-id="91466-216">Version differences</span></span>

<span data-ttu-id="91466-217">Bei Verwendung von Exchange Server 2010 Service Pack 1 (SP1) stehen für die [FindConversation](http://msdn.microsoft.com/en-us/library/office/jj220668%28v=exchg.80%29.aspx)-Methode weniger Optionen zur Verfügung, und der [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx)-Vorgang enthält weniger Elemente in der Anforderung.</span><span class="sxs-lookup"><span data-stu-id="91466-217">When you are using Exchange Server 2010 Service Pack 1 (SP1), the [FindConversation](http://msdn.microsoft.com/en-us/library/office/jj220668%28v=exchg.80%29.aspx) method has fewer options available, and the [FindConversation](http://msdn.microsoft.com/library/2384908a-c203-45b6-98aa-efd6a4c23aac%28Office.15%29.aspx) operation has fewer elements in the request.</span></span> 
  
<span data-ttu-id="91466-218">**Tabelle 3. FindConversation-Unterstützung in Exchange 2010 SP1**</span><span class="sxs-lookup"><span data-stu-id="91466-218">**Table 3. Exchange 2010 SP1 version support for FindConversation**</span></span>

|<span data-ttu-id="91466-219">**Methode der verwalteten EWS-API**</span><span class="sxs-lookup"><span data-stu-id="91466-219">**EWS Managed API method**</span></span>|<span data-ttu-id="91466-220">**EWS-Elemente**</span><span class="sxs-lookup"><span data-stu-id="91466-220">**EWS elements**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91466-221">FindConversation (ViewBase, FolderId)</span><span class="sxs-lookup"><span data-stu-id="91466-221">FindConversation (ViewBase, FolderId)</span></span>](http://msdn.microsoft.com/en-us/library/office/jj220668%28v=exchg.80%29.aspx) <br/> |[<span data-ttu-id="91466-222">IndexedPageItemView</span><span class="sxs-lookup"><span data-stu-id="91466-222">IndexedPageItemView</span></span>](http://msdn.microsoft.com/library/6d1b0b04-cc35-4a57-bd7a-824136d14fda%28Office.15%29.aspx) <br/> [<span data-ttu-id="91466-223">SortOrder</span><span class="sxs-lookup"><span data-stu-id="91466-223">SortOrder</span></span>](http://msdn.microsoft.com/library/c2413f0b-8c03-46ae-9990-13338b3c53a6%28Office.15%29.aspx) <br/> [<span data-ttu-id="91466-224">ParentFolderId</span><span class="sxs-lookup"><span data-stu-id="91466-224">ParentFolderId</span></span>](http://msdn.microsoft.com/library/0e3e6e5f-06d0-499b-8ca4-d36036521658%28Office.15%29.aspx) <br/> |
   
<span data-ttu-id="91466-p115">Die [GetConversationItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx)-Methode der verwalteten EWS-API und der EWS-Vorgang [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) wurden in Exchange Server 2013 eingeführt. Anwendungen, die für frühere Exchange-Versionen erstellt werden, können lediglich Unterhaltungsaktionen auf Unterhaltungen anwenden, wie in Tabelle 2 aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="91466-p115">The [GetConversationItems](http://msdn.microsoft.com/en-us/library/office/microsoft.exchange.webservices.data.exchangeservice.getconversationitems%28v=exchg.80%29.aspx) EWS Managed API method and the [GetConversationItems](http://msdn.microsoft.com/library/8ae00a99-b37b-4194-829c-fe300db6ab99%28Office.15%29.aspx) EWS operation were introduced in Exchange Server 2013. Applications that target earlier versions of Exchange can only apply conversation actions to conversations, as listed in Table 2.</span></span> 
  
<span data-ttu-id="91466-227">Die **FindConversation** -Methode der verwalteten EWS-API und die EWS-Methode **FindConversation** sind in der ersten Version von Exchange 2010 und in Exchange 2007 nicht verfügbar.</span><span class="sxs-lookup"><span data-stu-id="91466-227">The **FindConversation** EWS Managed API method and the **FindConversation** EWS method are not available in the initial release version of Exchange 2010 or in Exchange 2007.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="91466-228">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91466-228">See also</span></span>

- [<span data-ttu-id="91466-229">E-Mail- und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="91466-229">Email and EWS in Exchange</span></span>](email-and-ews-in-exchange.md)
- [<span data-ttu-id="91466-230">Verwenden Sie Suchfilter mit EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="91466-230">Use search filters with EWS in Exchange</span></span>](how-to-use-search-filters-with-ews-in-exchange.md)   
- [<span data-ttu-id="91466-231">Exchange 2013: Programmgesteuertes Suchen nach Unterhaltungen in Postfächern</span><span class="sxs-lookup"><span data-stu-id="91466-231">Exchange 2013: Find conversations in mailboxes programmatically</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Find-d4b6b3af)    
- [<span data-ttu-id="91466-232">Exchange 2013: Anwenden von Aktionen zum Verwalten von Unterhaltungen in einem Postfach</span><span class="sxs-lookup"><span data-stu-id="91466-232">Exchange 2013: Apply actions to manage conversations in a mailbox</span></span>](http://code.msdn.microsoft.com/exchange/Exchange-2013-Apply-accde0b5)
    
