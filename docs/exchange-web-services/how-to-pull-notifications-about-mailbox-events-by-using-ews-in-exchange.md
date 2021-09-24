---
title: Pullbenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.localizationpriority: medium
ms.assetid: eb25cbd1-2244-4c3f-a71a-5ee20f81c41f
description: Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um Pullbenachrichtigungen zu abonnieren und Ereignisse abzurufen.
ms.openlocfilehash: eb694eddd16567e42ccc43b2854f0432c54dc6b1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513101"
---
# <a name="pull-notifications-about-mailbox-events-by-using-ews-in-exchange"></a>Pullbenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange

Erfahren Sie, wie Sie die verwaltete EWS-API oder EWS verwenden, um Pullbenachrichtigungen zu abonnieren und Ereignisse abzurufen.
  
EWS in Exchange verwendet Pullbenachrichtigungen, damit Clients Benachrichtigungen über Änderungen am Postfach vom Server an den Client anfordern (oder abrufen) können.
  
Wenn Sie Pullbenachrichtigungen mithilfe der verwalteten EWS-API abonnieren [und abrufen, abonnieren Sie Pullbenachrichtigungen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullewsma) mithilfe der [SubscribeToPullNotifications-Methode.](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) Anschließend rufen Sie Ereignisse vom Server mithilfe der [GetEvents-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) ab. 
  
Um Pullbenachrichtigungen mithilfe von EWS zu abonnieren, erstellen Sie [ein Abonnement](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_cepullews) mithilfe des [Subscribe-Vorgangs,](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)analysieren die Antwort und rufen dann [die Benachrichtigungen](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_getpull) mithilfe des [GetEvents-Vorgangs](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx)ab.
  
Nachdem der Client Benachrichtigungen über Elemente erhalten hat, die auf dem Server geändert oder erstellt wurden, kann er [die Änderungen synchronisieren.](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps)
  
## <a name="subscribe-to-and-get-pull-notifications-by-using-the-ews-managed-api"></a>Abonnieren und Abrufen von Pullbenachrichtigungen mithilfe der verwalteten EWS-API
<a name="bk_cepullewsma"> </a>

Das folgende Codebeispiel zeigt, wie Sie die [SubscribeToPullNotifications-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) verwenden, um Pullbenachrichtigungen für alle Ereignisse im Ordner "Posteingang" zu abonnieren. Anschließend wird die [GetEvents-Methode](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.pullsubscription.getevents%28v=exchg.80%29.aspx) verwendet, um Ereignisse vom Server abzurufen. In diesem Beispiel wird davon ausgegangen, dass **der Dienst** eine gültige [ExchangeService-Bindung](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice%28v=exchg.80%29.aspx) ist. 
  
```cs
// Subscribe to pull notifications in the Inbox.
PullSubscription subscription = service.SubscribeToPullNotifications( 
    new FolderId[] { WellKnownFolderName.Inbox }, 30, null, 
    EventType.NewMail, EventType.Created, EventType.Deleted,
    EventType.Modified, EventType.Moved, EventType.Copied, EventType.FreeBusyChanged); 
 
// Call GetEvents to retrieve events from the server. 
GetEventsResults events = subscription.GetEvents(); 
```

Nachdem Sie ein Ereignis vom Server erhalten haben, können Sie [diese Änderungen mit dem Server synchronisieren.](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) Verwenden Sie eine der in "Wie kann ich das [Abonnement von Benachrichtigungen kündigen?" angegebenen](notification-subscriptions-mailbox-events-and-ews-in-exchange.md#bk_notifunsubscribe) Methoden, um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird. 
  
## <a name="subscribe-to-pull-notifications-by-using-ews"></a>Abonnieren von Pullbenachrichtigungen mithilfe von EWS
<a name="bk_cepullews"> </a>

Das folgende Beispiel zeigt die XML-Anforderung, die an den Server gesendet werden soll, um alle [EventTypes](https://msdn.microsoft.com/library/29ded9e5-f191-4aa3-bc3e-500de2fc8818%28Office.15%29.aspx) im Ordner Posteingang mithilfe des [Subscribe-Vorgangs](https://msdn.microsoft.com/library/f17c3d08-c79e-41f1-ba31-6e41e7aafd87%28Office.15%29.aspx)zu abonnieren. Dies ist auch die XML-Anforderung, die die verwaltete EWS-API sendet, wenn Pullbenachrichtigungen mithilfe der [SubscribeToPullNotifications-Methode abonniert](https://msdn.microsoft.com/library/microsoft.exchange.webservices.data.exchangeservice.subscribetopullnotifications%28v=exchg.80%29.aspx) werden. 
  
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

Das folgende XML-Beispiel zeigt die [SubscribeResponse-Nachricht,](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) die als Antwort auf die Anforderung zum **Abonnieren** des Vorgangs vom Server an den Client gesendet wird. Die Aufnahme des NoError-Werts für das [ResponseCode-Element](https://msdn.microsoft.com/library/4b84d670-74c9-4d6d-84e7-f0a9f76f0d93%28Office.15%29.aspx) bedeutet, dass das Abonnement erfolgreich erstellt wurde. Das [SubscriptionId-Element](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) identifiziert das Pullbenachrichtigungsabonnement auf dem Server eindeutig. Das [Watermark-Element](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) stellt eine Textmarke in der Postfachereigniswarteschlange dar. 
  
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

Nachdem Sie das Abonnement erstellt haben, können Sie jetzt Ereignisse mithilfe der **SubscriptionId** abrufen, die in der **SubscribeResponse-Nachricht** zurückgegeben wird. 
  
## <a name="get-pull-notifications-by-using-ews"></a>Abrufen von Pullbenachrichtigungen mithilfe von EWS
<a name="bk_getpull"> </a>

Das folgende XML-Beispiel zeigt die Anforderungsnachricht für den [GetEvents-Vorgang,](https://msdn.microsoft.com/library/f268efe5-9a1a-41a2-b6a6-51fcde7720a1%28Office.15%29.aspx) die vom Client an den Server gesendet wird, um Benachrichtigungen für die [SubscriptionId](https://msdn.microsoft.com/library/77c0abab-69e8-428e-8c20-22258e4ef71b%28Office.15%29.aspx) abzurufen, die in der [SubscribeResponse-Nachricht](https://msdn.microsoft.com/library/fd87e9b7-c231-44fa-9f5b-19ae96cda5cc%28Office.15%29.aspx) zurückgegeben wird. Verwenden Sie für die erste **GetEvents-Anforderung** das in der **Subscribe-Antwort** zurückgegebene [Wasserzeichen.](https://msdn.microsoft.com/library/e1545046-94f9-4ac7-af1c-ea81dfb6822c%28Office.15%29.aspx) Verwenden Sie für nachfolgende **GetEvents-Anforderungen** das letzte **Wasserzeichen,** das in der vorherigen **GetEvents-Anforderung** zurückgegeben wurde. 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<GetEvents xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <SubscriptionId xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">d581ab79-a2ec-4653-9c8e-564d7cfc1d8c</SubscriptionId>
  <Watermark xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">AAAAAGUhAAAAAAAAAQ==</Watermark>
</GetEvents>
```

Das folgende XML-Beispiel zeigt die **GetEvents-Antwortnachricht,** die vom Server an den Client gesendet wird. Jede **GetEvents-Antwort** enthält Informationen zu einem oder mehreren Ereignissen. Für jedes Ereignis wird ein **Wasserzeichen** zurückgegeben. Das letzte **Wasserzeichen** muss gespeichert und in der nächsten **GetEvents-Anforderung** verwendet werden. Wenn seit der letzten **GetEvents-Anforderung** keine Speicherereignisse aufgetreten sind, wird ein Statusereignis zurückgegeben. 
  
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

Nachdem Sie ein Ereignis vom Server erhalten haben, synchronisieren Sie [die Änderungen mit dem Client.](how-to-pull-notifications-about-mailbox-events-by-using-ews-in-exchange.md#bk_nextsteps) Verwenden Sie den [Unsubscribe-Vorgang,](https://msdn.microsoft.com/library/994a9d2b-1501-4804-90f0-12bd914496ec%28Office.15%29.aspx) um das Abonnement mit dem Server zu beenden, wenn das Abonnement nicht mehr benötigt wird. 
  
## <a name="next-steps"></a>Nächste Schritte
<a name="bk_nextsteps"> </a>

Nachdem Sie Benachrichtigungen erhalten haben, können Sie [die Ordnerhierarchie synchronisieren](how-to-synchronize-folders-by-using-ews-in-exchange.md) oder [den Inhalt des Ordners synchronisieren, der sich geändert hat.](how-to-synchronize-items-by-using-ews-in-exchange.md)
  
## <a name="see-also"></a>Siehe auch


- [Benachrichtigungsabonnements, Postfachereignisse und EWS in Exchange](notification-subscriptions-mailbox-events-and-ews-in-exchange.md)
    
- [Streambenachrichtigungen zu Postfachereignissen mithilfe von EWS in Exchange](how-to-stream-notifications-about-mailbox-events-by-using-ews-in-exchange.md)
    
- [Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](how-to-maintain-affinity-between-group-of-subscriptions-and-mailbox-server.md)
    
- [Umgang von Fehlern im Zusammenhang mit Benachrichtigungen in EWS in Exchange](handling-notification-related-errors-in-ews-in-exchange.md)
    
- [Postfachsynchronisierung und EWS in Exchange](mailbox-synchronization-and-ews-in-exchange.md)
    

