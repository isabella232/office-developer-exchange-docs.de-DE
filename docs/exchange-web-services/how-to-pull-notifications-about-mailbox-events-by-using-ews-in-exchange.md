---
title: Pullbenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: Hier erfahren Sie, wie Sie die verwaltete EWS-API oder EWS zum Abonnieren von Pull-Benachrichtigungen und Abrufen von Ereignissen verwenden.
ms.openlocfilehash: 3d77c0d4efb8fc853eea64ff2429af5c3dbead27
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456737"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a><span data-ttu-id="600e8-103">Pullbenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="600e8-103">Pull notifications about mailbox events by using EWS in Exchange</span></span>

<span data-ttu-id="600e8-104">Hier erfahren Sie, wie Sie die verwaltete EWS-API oder EWS zum Abonnieren von Pull-Benachrichtigungen und Abrufen von Ereignissen verwenden.</span><span class="sxs-lookup"><span data-stu-id="600e8-104">Find out how to use the EWS Managed API or EWS to subscribe to pull notifications and get events.</span></span>
  
<span data-ttu-id="600e8-105">EWS in Exchange verwendet Pull-Benachrichtigungen, um Clients das anfordern (oder abrufen) von Benachrichtigungen über Änderungen am Postfach vom Server an den Client zu ermöglichen.</span><span class="sxs-lookup"><span data-stu-id="600e8-105">EWS in Exchange uses pull notifications to enable clients to request (or pull) notifications about changes to the mailbox from the server to the client.</span></span>
  
<span data-ttu-id="600e8-106">Wenn Sie Pull-Benachrichtigungen mit dem verwaltete EWS-API abonnieren, können Sie mithilfe der [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode [Pull-Benachrichtigungen abonnieren und Abrufen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) .</span><span class="sxs-lookup"><span data-stu-id="600e8-106">If you're subscribing to pull notifications by using the EWS Managed API, you [subscribe to and get pull notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) by using the [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> <span data-ttu-id="600e8-107">Anschließend werden Ereignisse vom Server mithilfe der [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) -Methode abgerufen.</span><span class="sxs-lookup"><span data-stu-id="600e8-107">You then get events from the server by using the [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method.</span></span> 
  
<span data-ttu-id="600e8-108">Zum Abonnieren von Pull-Benachrichtigungen mithilfe von EWS [Erstellen Sie ein Abonnement](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) mit dem [Subscribe-Vorgang](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), analysieren die Antwort und rufen dann [die Benachrichtigungen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mithilfe des [GetEvents-Vorgangs](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)ab.</span><span class="sxs-lookup"><span data-stu-id="600e8-108">To subscribe to pull notifications by using EWS, you [create a subscription](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) by using the [Subscribe operation](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), parse the response, and then [get the notifications](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) by using the [GetEvents operation](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).</span></span>
  
<span data-ttu-id="600e8-109">Nachdem der Clientbenachrichtigungen über Elemente erhält, die auf dem Server geändert oder erstellt wurden, kann er [die Änderungen dann synchronisieren](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="600e8-109">After the client receives notifications of items that are changed or created on the server, it can then [synchronize the changes](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span>
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a><span data-ttu-id="600e8-110">Abonnieren und Abrufen von Pull-Benachrichtigungen mithilfe der verwaltete EWS-API</span><span class="sxs-lookup"><span data-stu-id="600e8-110">Subscribe to and get pull notifications by using the EWS Managed API</span></span>
<span data-ttu-id="600e8-111"><a name="bk_cepullewsma"> </a></span><span class="sxs-lookup"><span data-stu-id="600e8-111"><a name="bk_cepullewsma"> </a></span></span>

<span data-ttu-id="600e8-112">Im folgenden Codebeispiel wird gezeigt, wie Sie mit der [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode Pull-Benachrichtigungen für alle Ereignisse im Ordner Posteingang abonnieren.</span><span class="sxs-lookup"><span data-stu-id="600e8-112">The following code example shows how to use the [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method to subscribe to pull notifications for all events in the Inbox folder.</span></span> <span data-ttu-id="600e8-113">Im Beispiel wird dann die [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) -Methode verwendet, um Ereignisse vom Server abzurufen.</span><span class="sxs-lookup"><span data-stu-id="600e8-113">The example then uses the [GetEvents](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) method to retrieve events from the server.</span></span> <span data-ttu-id="600e8-114">In diesem Beispiel wird davon ausgegangen, dass der **Dienst** eine gültige [Datei "ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) -Bindung ist.</span><span class="sxs-lookup"><span data-stu-id="600e8-114">In this example, we assume that **service** is a valid [ExchangeService](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) binding.</span></span> 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

<span data-ttu-id="600e8-115">Nachdem Sie ein Ereignis vom Server empfangen haben, können Sie [diese Änderungen mit dem Server synchronisieren](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span><span class="sxs-lookup"><span data-stu-id="600e8-115">After you receive an event from the server, you can [synchronize those changes with the server](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).</span></span> <span data-ttu-id="600e8-116">Verwenden Sie eine der Unsubscribe-Methoden, die unter [How do I dissubscribe to Notifications](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) angegeben wird? zum Beenden des Abonnements mit dem Server, wenn das Abonnement nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="600e8-116">Use one of the unsubscribe methods specified in [How do I unsubscribe to notifications?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a><span data-ttu-id="600e8-117">Abonnieren von Pull-Benachrichtigungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="600e8-117">Subscribe to pull notifications by using EWS</span></span>
<span data-ttu-id="600e8-118"><a name="bk_cepullews"> </a></span><span class="sxs-lookup"><span data-stu-id="600e8-118"><a name="bk_cepullews"> </a></span></span>

<span data-ttu-id="600e8-119">Im folgenden Beispiel wird die XML-Anforderung zum Senden an den Server zum Abonnieren aller [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) im Posteingangsordner mithilfe des [subscribe-Vorgangs](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)gezeigt.</span><span class="sxs-lookup"><span data-stu-id="600e8-119">The following example shows the XML request to send to the server to subscribe to all [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) in the Inbox folder by using the [Subscribe operation](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx).</span></span> <span data-ttu-id="600e8-120">Dies ist auch die XML-Anforderung, die der verwaltete EWS-API beim Abonnieren von Pull-Benachrichtigungen mithilfe der [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode sendet.</span><span class="sxs-lookup"><span data-stu-id="600e8-120">This is also the XML request that the EWS Managed API sends when subscribing to pull notifications by using the [SubscribeToPullNotifications](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) method.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
           xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <PullSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
      <DistinguishedFolderId Id="inbox" />
    </FolderIds>
    <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
            <EventType>NewMailEvent</EventType>
            <EventType>CreatedEvent</EventType>
            <EventType>DeletedEvent</EventType>
            <EventType>ModifiedEvent</EventType>
            <EventType>MovedEvent</EventType>
            <EventType>CopiedEvent</EventType>
            <EventType>FreeBusyChangedEvent</EventType>
    </EventTypes>
    <Timeout xmlns="https://schemas.microsoft.com/exchange/services/2006/types">30</Timeout>
  </PullSubscriptionRequest>
</Subscribe>
```

<span data-ttu-id="600e8-121">Das folgende XML-Beispiel zeigt die [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) -Nachricht, die als Antwort auf die Anforderung des **subscribe** -Vorgangs vom Server an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="600e8-121">The following XML example shows the [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message that is sent from the server to the client in response to the **Subscribe** operation request.</span></span> <span data-ttu-id="600e8-122">Die Einbeziehung des noError-Werts für das [Response Code](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) -Element bedeutet, dass das Abonnement erfolgreich erstellt wurde.</span><span class="sxs-lookup"><span data-stu-id="600e8-122">The inclusion of the NoError value for the [ResponseCode](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) element means that the subscription was created successfully.</span></span> <span data-ttu-id="600e8-123">Das [Abonnement](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) Kennungs Element identifiziert das Pullabonnement auf dem Server eindeutig.</span><span class="sxs-lookup"><span data-stu-id="600e8-123">The [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) element uniquely identifies the pull notification subscription on the server.</span></span> <span data-ttu-id="600e8-124">Das [Wasserzeichen](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) -Element stellt eine Textmarke in der Post Fach Ereigniswarteschlange dar.</span><span class="sxs-lookup"><span data-stu-id="600e8-124">The [Watermark](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) element represents a bookmark in the mailbox event queue.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<SubscribeResponse xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                   xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <SubscribeResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <SubscriptionId>d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
      <Watermark>AAAAAGUhAAAAAAAAAQ==</Watermark>
    </SubscribeResponseMessage>
  </ResponseMessages>
</SubscribeResponse>
```

<span data-ttu-id="600e8-125">Nachdem Sie das Abonnement erstellt haben, können Sie jetzt Ereignisse abrufen, indem Sie die in der **SubscribeResponse** -Nachricht zurückgegebene **Abonnement** -e-Mail verwenden.</span><span class="sxs-lookup"><span data-stu-id="600e8-125">After creating the subscription, you can now get events by using the **SubscriptionId** that is returned in the **SubscribeResponse** message.</span></span> 
  
## <a name="get-pull-notifications-by-using-ews"></a><span data-ttu-id="600e8-126">Abrufen von Pull-Benachrichtigungen mithilfe von EWS</span><span class="sxs-lookup"><span data-stu-id="600e8-126">Get pull notifications by using EWS</span></span>
<span data-ttu-id="600e8-127"><a name="bk_getpull"> </a></span><span class="sxs-lookup"><span data-stu-id="600e8-127"><a name="bk_getpull"> </a></span></span>

<span data-ttu-id="600e8-128">Das folgende XML-Beispiel zeigt die [GetEvents-Vorgangs](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) Anforderungsnachricht, die vom Client an den Server gesendet wird, um Benachrichtigungen für die in der [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) -Nachricht zurückgegebene [Abonnement](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) -e-Mail zu erhalten.</span><span class="sxs-lookup"><span data-stu-id="600e8-128">The following XML example shows the [GetEvents operation](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) request message that is sent from the client to the server to get notifications for the [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) that is returned in the [SubscribeResponse](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) message.</span></span> <span data-ttu-id="600e8-129">Verwenden Sie für die erste **GetEvents** -Anforderung das [Wasserzeichen](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) , das in der **subscribe** -Antwort zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="600e8-129">For the first **GetEvents** request, use the [Watermark](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) returned in the **Subscribe** response.</span></span> <span data-ttu-id="600e8-130">Verwenden Sie für nachfolgende **GetEvents** -Anforderungen das letzte **Wasserzeichen** , das in der vorherigen **GetEvents** -Anforderung zurückgegeben wurde.</span><span class="sxs-lookup"><span data-stu-id="600e8-130">For subsequent **GetEvents** requests, use the last **Watermark** that was returned in the previous **GetEvents** request.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

<span data-ttu-id="600e8-131">Das folgende XML-Beispiel zeigt die **GetEvents** -Antwortnachricht, die vom Server an den Client gesendet wird.</span><span class="sxs-lookup"><span data-stu-id="600e8-131">The following XML example shows the **GetEvents** response message that is sent from the server to the client.</span></span> <span data-ttu-id="600e8-132">Jede **GetEvents** -Antwort enthält Informationen zu einem oder mehreren Ereignissen.</span><span class="sxs-lookup"><span data-stu-id="600e8-132">Each **GetEvents** response includes information about one or more events.</span></span> <span data-ttu-id="600e8-133">Für jedes Ereignis wird ein **Wasserzeichen** zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="600e8-133">A **Watermark** is returned for each event.</span></span> <span data-ttu-id="600e8-134">Das letzte **Wasserzeichen** muss gespeichert und in der nächsten **GetEvents** -Anforderung verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="600e8-134">The last **Watermark** must be saved and used in the next **GetEvents** request.</span></span> <span data-ttu-id="600e8-135">Wenn seit der letzten **GetEvents** -Anforderung keine Speicherereignisse aufgetreten sind, wird ein Status-Ereignis zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="600e8-135">If no store events have occurred since the last **GetEvents** request, a status event is returned.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEventsResponseType xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
                       xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <ResponseMessages xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <GetEventsResponseMessage ResponseClass="Success">
      <ResponseCode>NoError</ResponseCode>
      <Notification>
        <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/types">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
        <PreviousWatermark xmlns="https://schemas.microsoft.com/exchange/services/2006/types">AAAAAGUhAAAAAAAAAQ==</PreviousWatermark>
        <MoreEvents xmlns="https://schemas.microsoft.com/exchange/services/2006/types">false</MoreEvents>
        <NewMailEvent xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

Nachdem Sie ein Ereignis vom Server empfangen haben, [Synchronisieren Sie die Änderungen am Client](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). <span data-ttu-id="600e8-137">Verwenden Sie den [unsubscribe-Vorgang](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) , um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="600e8-137">Use the [Unsubscribe operation](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) to end the subscription with the server when the subscription is no longer needed.</span></span> 
  
## <a name="next-steps"></a><span data-ttu-id="600e8-138">Nächste Schritte</span><span class="sxs-lookup"><span data-stu-id="600e8-138">Next steps</span></span>
<span data-ttu-id="600e8-139"><a name="bk_nextsteps"> </a></span><span class="sxs-lookup"><span data-stu-id="600e8-139"><a name="bk_nextsteps"> </a></span></span>

<span data-ttu-id="600e8-140">Nachdem Sie Benachrichtigungen erhalten haben, können Sie [die Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md) oder [den Inhalt des geänderten Ordners synchronisieren](how-to-synchronize-items-by-using-ews-in-exchange.md).</span><span class="sxs-lookup"><span data-stu-id="600e8-140">After you're received notifications, you can [sync the folder hierarchy](how-to-synchronize-folders-by-using-ews-in-exchange.md) or [sync the contents of the folder that changed](how-to-synchronize-items-by-using-ews-in-exchange.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="600e8-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="600e8-141">See also</span></span>


- [<span data-ttu-id="600e8-142">Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="600e8-142">Notification subscriptions, mailbox events, and EWS in Exchange</span></span>](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [<span data-ttu-id="600e8-143">Streambenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="600e8-143">Stream notifications about mailbox events by using EWS in Exchange</span></span>](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [<span data-ttu-id="600e8-144">Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange</span><span class="sxs-lookup"><span data-stu-id="600e8-144">Maintain affinity between a group of subscriptions and the Mailbox server in Exchange</span></span>](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [<span data-ttu-id="600e8-145">Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="600e8-145">Handling notification-related errors in EWS in Exchange</span></span>](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [<span data-ttu-id="600e8-146">Postfachsynchronisierung und EWS in Exchange</span><span class="sxs-lookup"><span data-stu-id="600e8-146">Mailbox synchronization and EWS in Exchange</span></span>](mailbox-synchronization-and-ews-in-exchange.md)
    

