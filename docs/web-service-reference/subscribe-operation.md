---
title: Vorgang abonnieren
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Subscribe
api_type:
- schema
ms.assetid: f17c3d08-c79e-41f1-ba31-6e41e7aafd87
description: Subscribe-Vorgang wird verwendet, um die Clientanwendungen auf Push oder Pull-Benachrichtigungen zu abonnieren. Es ist wichtig, beachten Sie, dass die Struktur der Anforderungsnachrichten und Antworten je nach den Typ des ereignisbenachrichtigung unterscheidet.
ms.openlocfilehash: f6cacab80c8ca2e505ab63a162a161fcf5de8585
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831619"
---
# <a name="subscribe-operation"></a>Vorgang abonnieren

Subscribe-Vorgang wird verwendet, um die Clientanwendungen auf Push oder Pull-Benachrichtigungen zu abonnieren. Es ist wichtig, beachten Sie, dass die Struktur der Anforderungsnachrichten und Antworten je nach den Typ des ereignisbenachrichtigung unterscheidet. 
  
## <a name="pull-subscription-subscribe-request-example"></a>Pull-Abonnement abonnieren anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Codebeispiel wird veranschaulicht, wie ein Ereignis-Benachrichtigung Pullabonnement abonnieren. Das Abonnement informiert die Clientanwendung, wenn neue e-Mail-Nachrichten in den Posteingang hinzugefügt wird und wenn ein Element aus dem Posteingang gelöscht wird. Das Abonnement wird Timeout auf, wenn der Client keine Informationen zu Ereignissen innerhalb von zehn Minuten anfordert. Wenn das Abonnement abläuft, muss ein neues Abonnement weiterhin Benachrichtigungen anfordern hergestellt werden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-subscribe-request-elements"></a>Pullabonnement abonnieren Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [Abonnieren](subscribe.md)
    
- [PullSubscriptionRequest](pullsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [Timeout](timeout.md)
    
Um weitere Optionen für die Anforderung an die Subscribe-Operation zu suchen, verwenden Sie die Schemahierarchie. Starten Sie das [PullSubscriptionRequest](pullsubscriptionrequest.md) -Element. 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a>Erfolgreiche Pull-Abonnement abonniert antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Pull-Abonnement-Antwort. Die Antwort enthält die Abonnement-ID und Wasserzeichen, die verwendet wird, um das Array der Ereignisse abzurufen, die ein Abonnement zugeordnet sind. Die Abonnement-ID wird auch verwendet, einen Client von einem Abonnement zu kündigen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-subscribe-response-elements"></a>Pull-Abonnement abonniert Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Wasserzeichen](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a>Pull-Abonnement abonnieren Fehler antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine Fehlerantwort an die Subscribe-Anforderung. Der Fehler wird durch den Versuch, Abonnieren von Benachrichtigungen mithilfe von Zugriffsrechten für Stellvertretung verursacht.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="685" MinorBuildNumber="8" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="pull-subscription-error-response-elements"></a>Ziehen Sie Antwortelemente Abonnementfehler

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a>Push-Abonnement-anforderungsbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Codebeispiel wird veranschaulicht, wie ein Push-Ereignis Benachrichtigungsabonnement abonnieren. Die Anforderung identifiziert den Ordner überwacht werden, die Typen der zu überwachenden Ereignisse, die Häufigkeit der statusbenachrichtigungen und die URL des Clients Webdienst, der die Pushbenachrichtigungen überwacht.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
               xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Subscribe xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
      <PushSubscriptionRequest xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <FolderIds xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <DistinguishedFolderId Id="inbox" />
        </FolderIds>
        <EventTypes xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
          <EventType>NewMailEvent</EventType>
          <EventType>CopiedEvent</EventType>
          <EventType>CreatedEvent</EventType>
          <EventType>DeletedEvent</EventType>
          <EventType>ModifiedEvent</EventType>
          <EventType>MovedEvent</EventType>
        </EventTypes>
        <StatusFrequency xmlns="http://schemas.microsoft.com/exchange/services/2006/types">1</StatusFrequency>
        <URL xmlns="http://schemas.microsoft.com/exchange/services/2006/types">http://clientWebService/Service.asmx</URL>
      </PushSubscriptionRequest>
    </Subscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="comments"></a>Kommentare

Der Client Web Service eingerichtet werden muss, bevor das Push Notification abonnieren Anforderung wird gesendet. Andernfalls wird die erste Benachrichtigung an einen gültigen Endpunkt nicht gesendet, und das Push Notification schlägt fehl. Weitere Informationen finden Sie unter [Push Notification Beispielanwendung](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).
  
Eine neue [SubscriptionId (GetEvents)](subscriptionid-getevents.md) wird erstellt, sobald Sie erneut abonnieren. Verwenden Sie das Wasserzeichen des vorherigen-Abonnements, um an der Stelle erneut abonnieren, in dem das vorherige Abonnement beendet. 
  
### <a name="push-subscription-request-elements"></a>Push-Abonnement Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [Abonnieren](subscribe.md)
    
- [PushSubscriptionRequest](pushsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [StatusFrequency](statusfrequency.md)
    
- [URL](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a>Erfolgreiche Pushabonnement antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Push-Abonnement-Antwort. 
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <SubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                       xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                       xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
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

### <a name="push-subscription-response-elements"></a>Schieben Antwortelemente Abonnement

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
- [Wasserzeichen](watermark.md)
    
## <a name="see-also"></a>Siehe auch



[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)


[Mithilfe von Pullabonnements](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[Beispielanwendung für Pushbenachrichtigungen](http://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

