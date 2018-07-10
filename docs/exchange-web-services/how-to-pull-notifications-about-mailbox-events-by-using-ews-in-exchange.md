---
title: Ziehen Sie Benachrichtigungen über Ereignisse Postfach mithilfe der EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: Erfahren Sie, wie die EWS Managed API oder EWS Pull Benachrichtigungen abonnieren und Ereignisse verwenden.
ms.openlocfilehash: 6a04aaf0102c149691a30c2bd2f499e03265bce8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19756985"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a><span data-ttu-id="9fa1e-103">Ziehen Sie Benachrichtigungen über Ereignisse Postfach mithilfe der EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fa1e-103">Pull notifications about mailbox events by using EWS in Exchange</span></span>

<span data-ttu-id="9fa1e-104">Erfahren Sie, wie die EWS Managed API oder EWS Pull Benachrichtigungen abonnieren und Ereignisse verwenden.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-104">Find out how to use the EWS Managed API or EWS to subscribe to pull notifications and get events.</span></span>
  
<span data-ttu-id="9fa1e-105">EWS in Exchange verwendet Pull Benachrichtigungen, um Clients das anfordern (oder Pull) Benachrichtigungen zu Änderungen an das Postfach auf dem Server an den Client zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-105">EWS in Exchange uses pull notifications to enable clients to request (or pull) notifications about changes to the mailbox from the server to the client.</span></span>
  
<span data-ttu-id="9fa1e-106">Wenn Sie auf Pull-Benachrichtigungen abonniert mithilfe der EWS Managed API, Sie [abonnieren und Pull Benachrichtigungen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) mithilfe der [SubscribeToPullNotifications](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode soll werden.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-106">If you're subscribing to pull notifications by using the EWS Managed API, you [subscribe to and get pull notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) by using the [SubscribeToPullNotifications](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="9fa1e-107">Sie erhalten dann Ereignisse vom Server mithilfe der [GetEvents](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) -Methode.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-107">You then get events from the server by using the [GetEvents](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="9fa1e-108">Zum Abonnieren Pull Benachrichtigungen mithilfe von EWS analysieren Sie [ein Abonnement erstellen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) , mit der [Subscribe-Vorgang](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), der Antwort, und klicken Sie dann [die Benachrichtigungen erhalten möchten](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mit der [GetEvents Vorgang](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="9fa1e-108">To subscribe to pull notifications by using EWS, you [create a subscription](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) by using the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), parse the response, and then [get the notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) by using the [GetEvents operation](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="9fa1e-109">Nachdem der Client Benachrichtigungen von Elementen empfängt, die geändert oder auf dem Server erstellt werden, kann es klicken Sie dann [die Änderungen zu synchronisieren](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="9fa1e-109">After the client receives notifications of items that are changed or created on the server, it can then [synchronize the changes](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a><span data-ttu-id="9fa1e-110">Abonnieren Sie und rufen Sie Pull Benachrichtigungen ab, indem Sie die EWS Managed API</span><span class="sxs-lookup"><span data-stu-id="9fa1e-110">Subscribe to and get pull notifications by using the EWS Managed API</span></span>
<span data-ttu-id="9fa1e-111"><a name="bk_cepullewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="9fa1e-111"></span></span>

<span data-ttu-id="9fa1e-112">Im folgenden Codebeispiel wird veranschaulicht, wie mit der [SubscribeToPullNotifications](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode, um Pull-Benachrichtigungen für alle Ereignisse im Ordner Posteingang zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-112">The following code example shows how to use the [SubscribeToPullNotifications](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method to subscribe to pull notifications for all events in the Inbox folder.</span></span> <span data-ttu-id="9fa1e-113">Im Beispiel wird die [GetEvents](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) -Methode zum Abrufen von Ereignissen aus dem Server.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-113">The example then uses the [GetEvents](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method to retrieve events from the server.</span></span> <span data-ttu-id="9fa1e-114">In diesem Beispiel wird davon ausgegangen, dass die **Service** gültige [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-114">In this example, we assume that **service** is a valid [ExchangeService](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) binding.</span></span> 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

<span data-ttu-id="9fa1e-115">Nachdem Sie ein Ereignis vom Server erhalten haben, können Sie [diese Änderungen mit dem Server synchronisieren](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="9fa1e-115">After you receive an event from the server, you can [synchronize those changes with the server](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="9fa1e-116">Verwenden Sie eine der Methoden zum Abmelden in [wie ich kündigen auf Benachrichtigungen?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-116">Use one of the unsubscribe methods specified in [How do I unsubscribe to notifications?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a><span data-ttu-id="9fa1e-117">Abonnieren von Benachrichtigungen Pull mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="9fa1e-117">Subscribe to pull notifications by using EWS</span></span>
<span data-ttu-id="9fa1e-118"><a name="bk_cepullews"> </a></span><span class="sxs-lookup"><span data-stu-id="9fa1e-118"></span></span>

<span data-ttu-id="9fa1e-119">Das folgende Beispiel zeigt die XML-Anfrage an den Server gesendet, um alle [EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) im Ordner Posteingang mit der [Subscribe-Vorgang](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-119">The following example shows the XML request to send to the server to subscribe to all [EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) in the Inbox folder by using the [Subscribe operation](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx).</span></span> <span data-ttu-id="9fa1e-120">Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie mithilfe der [SubscribeToPullNotifications](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode auf Pull-Benachrichtigungen zu abonnieren.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-120">This is also the XML request that the EWS Managed API sends when subscribing to pull notifications by using the [SubscribeToPullNotifications](http://msdn.microsoft.com/de-de/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <PullSubscriptionRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <FolderIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
      <DistinguishedFolderId Id="inbox" />
    </FolderIds>
    <EventTypes xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
            <EventType>NewMailEvent</EventType>
            <EventType>CreatedEvent</EventType>
            <EventType>DeletedEvent</EventType>
            <EventType>ModifiedEvent</EventType>
            <EventType>MovedEvent</EventType>
            <EventType>CopiedEvent</EventType>
            <EventType>FreeBusyChangedEvent</EventType>
    </EventTypes>
    <Timeout xmlns="http://schemas.microsoft.com/exchange/services/2006/types">30</Timeout>
  </PullSubscriptionRequest>
</Subscribe>
```

<span data-ttu-id="9fa1e-121">Das folgende XML-Beispiel zeigt die [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) -Nachricht, die vom Server an den Client als Antwort auf die **Subscribe** -Vorgang Anforderung gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-121">The following XML example shows the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message that is sent from the server to the client in response to the **Subscribe** operation request.</span></span> <span data-ttu-id="9fa1e-122">Die Aufnahme des Werts für das Element [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) NoError bedeutet, dass das Abonnement erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-122">The inclusion of the NoError value for the [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element means that the subscription was created successfully.</span></span> <span data-ttu-id="9fa1e-123">Das [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) -Element wird das Benachrichtigung Pullabonnement auf dem Server eindeutig identifiziert.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-123">The [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) element uniquely identifies the pull notification subscription on the server.</span></span> <span data-ttu-id="9fa1e-124">Das [Wasserzeichen](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) -Element stellt eine Textmarke in der Ereigniswarteschlange Postfach.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-124">The [Watermark](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) element represents a bookmark in the mailbox event queue.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<SubscribeResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <SubscribeResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <SubscriptionId>d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
      <Watermark>AAAAAGUhAAAAAAAAAQ==</Watermark>
    </SubscribeResponseMessage>
  </ResponseMessages>
</SubscribeResponse>
```

<span data-ttu-id="9fa1e-125">Nachdem das Abonnement erstellt haben, können Sie jetzt Ereignisse abrufen, mithilfe der **SubscriptionId** , die in der Nachricht **SubscribeResponse** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-125">After creating the subscription, you can now get events by using the **SubscriptionId** that is returned in the **SubscribeResponse** message.</span></span> 
  
## <a name="get-pull-notifications-by-using-ews"></a><span data-ttu-id="9fa1e-126">Abrufen von Pull Benachrichtigungen mithilfe der Exchange-Webdienste</span><span class="sxs-lookup"><span data-stu-id="9fa1e-126">Get pull notifications by using EWS</span></span>
<span data-ttu-id="9fa1e-127"><a name="bk_getpull"> </a></span><span class="sxs-lookup"><span data-stu-id="9fa1e-127"></span></span>

<span data-ttu-id="9fa1e-128">Das folgende XML-Beispiel zeigt die [GetEvents Vorgang](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) Request-Nachricht, die gesendet wird vom Client zum Server Benachrichtigungen für die [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) abgerufen, die in der Nachricht [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-128">The following XML example shows the [GetEvents operation](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) request message that is sent from the client to the server to get notifications for the [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) that is returned in the [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> <span data-ttu-id="9fa1e-129">Verwenden Sie für die erste Anforderung **GetEvents** das [Wasserzeichen](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) in der **Subscribe** -Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-129">For the first **GetEvents** request, use the [Watermark](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) returned in the **Subscribe** response.</span></span> <span data-ttu-id="9fa1e-130">Verwenden Sie für nachfolgende **GetEvents** Anforderungen des letzten **Wasserzeichen** , die in der vorherigen **GetEvents** Anforderung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-130">For subsequent **GetEvents** requests, use the last **Watermark** that was returned in the previous **GetEvents** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

<span data-ttu-id="9fa1e-131">Das folgende XML-Beispiel zeigt die **GetEvents** Response-Nachricht, die vom Server an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-131">The following XML example shows the **GetEvents** response message that is sent from the server to the client.</span></span> <span data-ttu-id="9fa1e-132">Jeder **GetEvents** Antwort enthält Informationen über einen oder mehrere Ereignisse.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-132">Each **GetEvents** response includes information about one or more events.</span></span> <span data-ttu-id="9fa1e-133">Ein **Wasserzeichen** wird für jedes Ereignis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-133">A **Watermark** is returned for each event.</span></span> <span data-ttu-id="9fa1e-134">Das letzte **Wasserzeichen** muss gespeichert und in der nächsten **GetEvents** Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-134">The last **Watermark** must be saved and used in the next **GetEvents** request.</span></span> <span data-ttu-id="9fa1e-135">Wenn keine Ereignisse Store seit der letzten **GetEvents** Anforderung aufgetreten sind, wird ein Statusereignis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-135">If no store events have occurred since the last **GetEvents** request, a status event is returned.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEventsResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <GetEventsResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <Notification>
        <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/types">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
        <PreviousWatermark xmlns="http://schemas.microsoft.com/exchange/services/2006/types">AAAAAGUhAAAAAAAAAQ==</PreviousWatermark>
        <MoreEvents xmlns="http://schemas.microsoft.com/exchange/services/2006/types">false</MoreEvents>
        <NewMailEvent xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <Watermark>AAAAAHMhAAAAAAAAAQ==</Watermark>
          <TimeStamp>2013-09-15T21:37:01Z</TimeStamp>
          <ItemId Id="AAAtA=" ChangeKey="CQAAAA==" />
          <ParentFolderId Id="AQAtAEFkbWA==" ChangeKey="AQAAAA==" />
        </NewMailEvent>
      </Notification>
    </GetEventsResponseMessage>
  </ResponseMessages>
</GetEventsResponse>
```

Nach Erhalt eines Ereignisses auf dem Server, [synchronisieren Sie die Änderungen an den Client](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). <span data-ttu-id="9fa1e-137">Verwenden Sie die [Abonnement-Vorgang](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) , um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="9fa1e-137">Use the [Unsubscribe operation](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="9fa1e-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="9fa1e-138">Next steps</span></span>
<span data-ttu-id="9fa1e-139"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="9fa1e-139"></span></span>

<span data-ttu-id="9fa1e-140">Nachdem Sie erhalten haben, sind Benachrichtigungen, können Sie die [Synchronisierung der Ordnerhierarchie](how-to-synchronize-folders-by-using-ews-in-exchange.md) oder [synchronisieren Sie den Inhalt des Ordners, der geändert](how-to-synchronize-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="9fa1e-140">After you're received notifications, you can [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [sync the contents of the folder that changed](how-to-synchronize-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="9fa1e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9fa1e-141">See also</span></span>


- [<span data-ttu-id="9fa1e-142">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fa1e-142">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="9fa1e-143">Stream-Benachrichtigungen bezüglich Postfach Ereignisse mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fa1e-143">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="9fa1e-144">Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fa1e-144">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [<span data-ttu-id="9fa1e-145">Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fa1e-145">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="9fa1e-146">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="9fa1e-146">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

