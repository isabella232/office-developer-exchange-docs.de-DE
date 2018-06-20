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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19756985"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>Ziehen Sie Benachrichtigungen über Ereignisse Postfach mithilfe der EWS in Exchange

Erfahren Sie, wie die EWS Managed API oder EWS Pull Benachrichtigungen abonnieren und Ereignisse verwenden.
  
EWS in Exchange verwendet Pull Benachrichtigungen, um Clients das anfordern (oder Pull) Benachrichtigungen zu Änderungen an das Postfach auf dem Server an den Client zu ermöglichen.
  
Wenn Sie auf Pull-Benachrichtigungen abonniert mithilfe der EWS Managed API, Sie [abonnieren und Pull Benachrichtigungen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) mithilfe der [SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode soll werden. Sie erhalten dann Ereignisse vom Server mithilfe der [GetEvents](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) -Methode. 
  
Zum Abonnieren Pull Benachrichtigungen mithilfe von EWS analysieren Sie [ein Abonnement erstellen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) , mit der [Subscribe-Vorgang](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx), der Antwort, und klicken Sie dann [die Benachrichtigungen erhalten möchten](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mit der [GetEvents Vorgang](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx).
  
Nachdem der Client Benachrichtigungen von Elementen empfängt, die geändert oder auf dem Server erstellt werden, kann es klicken Sie dann [die Änderungen zu synchronisieren](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps).
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>Abonnieren Sie und rufen Sie Pull Benachrichtigungen ab, indem Sie die EWS Managed API
<a name="bk_cepullewsma"> </a>

Im folgenden Codebeispiel wird veranschaulicht, wie mit der [SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode, um Pull-Benachrichtigungen für alle Ereignisse im Ordner Posteingang zu abonnieren. Im Beispiel wird die [GetEvents](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) -Methode zum Abrufen von Ereignissen aus dem Server. In diesem Beispiel wird davon ausgegangen, dass die **Service** gültige [ExchangeService](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) Bindung ist. 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

Nachdem Sie ein Ereignis vom Server erhalten haben, können Sie [diese Änderungen mit dem Server synchronisieren](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). Verwenden Sie eine der Methoden zum Abmelden in [wie ich kündigen auf Benachrichtigungen?](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird. 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>Abonnieren von Benachrichtigungen Pull mithilfe der Exchange-Webdienste
<a name="bk_cepullews"> </a>

Das folgende Beispiel zeigt die XML-Anfrage an den Server gesendet, um alle [EventTypes](http://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) im Ordner Posteingang mit der [Subscribe-Vorgang](http://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)zu abonnieren. Dies ist auch die XML-Anfrage, die die EWS Managed API sendet, wenn Sie mithilfe der [SubscribeToPullNotifications](http://msdn.microsoft.com/en-us/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) -Methode auf Pull-Benachrichtigungen zu abonnieren. 
  
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

Das folgende XML-Beispiel zeigt die [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) -Nachricht, die vom Server an den Client als Antwort auf die **Subscribe** -Vorgang Anforderung gesendet wird. Die Aufnahme des Werts für das Element [ResponseCode](http://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) NoError bedeutet, dass das Abonnement erfolgreich erstellt wurde. Das [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) -Element wird das Benachrichtigung Pullabonnement auf dem Server eindeutig identifiziert. Das [Wasserzeichen](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) -Element stellt eine Textmarke in der Ereigniswarteschlange Postfach. 
  
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

Nachdem das Abonnement erstellt haben, können Sie jetzt Ereignisse abrufen, mithilfe der **SubscriptionId** , die in der Nachricht **SubscribeResponse** zurückgegeben wird. 
  
## <a name="get-pull-notifications-by-using-ews"></a>Abrufen von Pull Benachrichtigungen mithilfe der Exchange-Webdienste
<a name="bk_getpull"> </a>

Das folgende XML-Beispiel zeigt die [GetEvents Vorgang](http://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) Request-Nachricht, die gesendet wird vom Client zum Server Benachrichtigungen für die [SubscriptionId](http://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) abgerufen, die in der Nachricht [SubscribeResponse](http://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) zurückgegeben wird. Verwenden Sie für die erste Anforderung **GetEvents** das [Wasserzeichen](http://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) in der **Subscribe** -Antwort zurückgegeben. Verwenden Sie für nachfolgende **GetEvents** Anforderungen des letzten **Wasserzeichen** , die in der vorherigen **GetEvents** Anforderung zurückgegeben wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

Das folgende XML-Beispiel zeigt die **GetEvents** Response-Nachricht, die vom Server an den Client gesendet wird. Jeder **GetEvents** Antwort enthält Informationen über einen oder mehrere Ereignisse. Ein **Wasserzeichen** wird für jedes Ereignis zurückgegeben. Das letzte **Wasserzeichen** muss gespeichert und in der nächsten **GetEvents** Anforderung verwendet werden. Wenn keine Ereignisse Store seit der letzten **GetEvents** Anforderung aufgetreten sind, wird ein Statusereignis zurückgegeben. 
  
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

Nach Erhalt eines Ereignisses auf dem Server, [synchronisieren Sie die Änderungen an den Client](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps). Verwenden Sie die [Abonnement-Vorgang](http://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) , um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird. 
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_nextsteps"> </a>

Nachdem Sie erhalten haben, sind Benachrichtigungen, können Sie die [Synchronisierung der Ordnerhierarchie](how-to-synchronize-folders-by-using-ews-in-exchange.md) oder [synchronisieren Sie den Inhalt des Ordners, der geändert](how-to-synchronize-items-by-using-ews-in-exchange.md).
  
## <a name="see-also"></a>Siehe auch


- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Stream-Benachrichtigungen bezüglich Postfach Ereignisse mithilfe von EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [Fehlerbehandlung Benachrichtigung-bezogene in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

