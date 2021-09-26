---
title: Subscribe-Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Subscribe
api_type:
- schema
ms.assetid: f17c3d08-c79e-41f1-ba31-6e41e7aafd87
description: Der Subscribe-Vorgang wird verwendet, um Clientanwendungen für Push- oder Pullbenachrichtigungen zu abonnieren. Es ist wichtig zu beachten, dass die Struktur der Anforderungsnachrichten und -antworten je nach Typ der Ereignisbenachrichtigung unterschiedlich ist.
ms.openlocfilehash: 546f7ab252c7d3a201130cd48e2b30ca52d00088
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544535"
---
# <a name="subscribe-operation"></a>Subscribe-Vorgang

Der Subscribe-Vorgang wird verwendet, um Clientanwendungen für Push- oder Pullbenachrichtigungen zu abonnieren. Es ist wichtig zu beachten, dass die Struktur der Anforderungsnachrichten und -antworten je nach Typ der Ereignisbenachrichtigung unterschiedlich ist. 
  
## <a name="pull-subscription-subscribe-request-example"></a>Beispiel für pull Subscription Subscribe-Anforderung

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt, wie Sie ein Pullereignisbenachrichtigungsabonnement abonnieren. Das Abonnement informiert die Clientanwendung, wenn dem Posteingang neue E-Mails hinzugefügt werden und ein Element aus dem Posteingang gelöscht wird. Für das Abonnement tritt ein Timeout auf, wenn der Client innerhalb von zehn Minuten keine Informationen zu Ereignissen anfordert. Wenn das Abonnement abläuft, muss ein neues Abonnement eingerichtet werden, um weiterhin Benachrichtigungen anzufordern.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PullSubscriptionRequest>
        <t:FolderIds>
          <t:DistinguishedFolderId Id="inbox"/>
        </t:FolderIds>
        <t:EventTypes>
          <t:EventType>NewMailEvent</t:EventType>
          <t:EventType>DeletedEvent</t:EventType>
        </t:EventTypes>
        <t:Timeout>10</t:Timeout>
      </PullSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-request-elements"></a>Subscribe-Anforderungselemente für Pullabonnements

In der Anforderung werden folgende Elemente verwendet:
  
- [Abonnieren](subscribe.md)
    
- [PullSubscriptionRequest](pullsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [Timeout](timeout.md)
    
Weitere Optionen für die Anforderungsnachricht des Subscribe-Vorgangs finden Sie in der Schemahierarchie. Beginnen Sie mit dem [PullSubscriptionRequest-Element.](pullsubscriptionrequest.md) 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a>Beispiel für eine erfolgreiche Pullabonnement-Abonnierung

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Pullabonnementantwort. Die Antwort enthält den Abonnementbezeichner und das Wasserzeichen, das verwendet wird, um das Array von Ereignissen abzurufen, die einem Abonnement zugeordnet sind. Der Abonnementbezeichner wird auch verwendet, um einen Client von einem Abonnement abzumelden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
          <m:SubscriptionId>39ea5d0f-f062-455e-a1e9-89c0304390f4</m:SubscriptionId>
          <m:Watermark>AAAAAHgGAAAAAAAAAQ==</m:Watermark>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-subscribe-response-elements"></a>Pull Subscription Subscribe-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a>Beispiel für Pull Subscription Subscribe Error -Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort auf eine Subscribe-Anforderung. Der Fehler wird durch einen Versuch verursacht, Benachrichtigungen mithilfe des Delegatzugriffs zu abonnieren.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:SubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>Subscriptions are not supported for delegate user access.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionDelegateAccessNotSupported</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:SubscribeResponseMessage>
      </m:ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="pull-subscription-error-response-elements"></a>Pull Subscription Error Response-Elemente

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a>Beispiel für Eine Pushabonnement-Anforderung

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt, wie Sie ein Pushereignisbenachrichtigungsabonnement abonnieren. Die Anforderung identifiziert die zu überwachenden Ordner, die Zu überwachenden Ereignistypen, die Häufigkeit von Statusbenachrichtigungen und die URL des Clientwebdiensts, der auf die Pushbenachrichtigungen lauscht.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="https://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="https://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Comments

Der Clientwebdienst muss eingerichtet sein, bevor die Anforderung zum Abonnieren von Pushbenachrichtigungen gesendet wird. andernfalls wird die erste Benachrichtigung nicht an einen gültigen Endpunkt gesendet, und die Pushbenachrichtigung schlägt fehl. Weitere Informationen finden Sie unter ["Beispielanwendung für Pushbenachrichtigungen".](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)
  
Beim erneuten Senden wird eine neue [SubscriptionId (GetEvents)](subscriptionid-getevents.md) erstellt. Verwenden Sie das Wasserzeichen eines vorherigen Abonnements, um es an dem Punkt erneut zu abonnieren, an dem das vorherige Abonnement endete. 
  
### <a name="push-subscription-request-elements"></a>Elemente der Pushabonnementanforderung

In der Anforderung werden folgende Elemente verwendet:
  
- [Abonnieren](subscribe.md)
    
- [PushSubscriptionRequest](pushsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [StatusFrequency](statusfrequency.md)
    
- [Url ](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a>Antwortbeispiel für erfolgreiches Pushabonnement

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Pushabonnementantwort. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="https://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="https://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <ResponseMessages>
        <SubscribeResponseMessage ResponseClass="Success">
          <ResponseCode>NoError</ResponseCode>
          <SubscriptionId>83826921-afdf-48be-b469-628cc02b5f49</SubscriptionId>
          <Watermark>AQAAAOpvG0LURVdOhQkPOWZLPcI8EgAAAAAAAAE=</Watermark>
        </SubscribeResponseMessage>
      </ResponseMessages>
    </SubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="push-subscription-response-elements"></a>Pushabonnement-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="see-also"></a>Siehe auch



[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)


[Verwenden von Pullabonnements](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[Beispielanwendung für Pushbenachrichtigungen](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

