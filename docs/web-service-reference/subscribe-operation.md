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
description: Der Subscribe-Vorgang wird verwendet, um Clientanwendungen für Push-oder Pull-Benachrichtigungen zu abonnieren. Es ist wichtig zu beachten, dass die Struktur der Anforderungsnachrichten und-Antworten je nach Typ der Ereignisbenachrichtigung unterschiedlich ist.
ms.openlocfilehash: c40e0e434f698c6535ff5d03fd4d45a453959dd6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467046"
---
# <a name="subscribe-operation"></a>Vorgang abonnieren

Der Subscribe-Vorgang wird verwendet, um Clientanwendungen für Push-oder Pull-Benachrichtigungen zu abonnieren. Es ist wichtig zu beachten, dass die Struktur der Anforderungsnachrichten und-Antworten je nach Typ der Ereignisbenachrichtigung unterschiedlich ist. 
  
## <a name="pull-subscription-subscribe-request-example"></a>Subscribe-Abonnement-Anforderungs Beispiel für Pullabonnements

### <a name="description"></a>Beschreibung

Das folgende Codebeispiel zeigt, wie Sie ein Ereignis Benachrichtigungsabonnement für Pullabonnements abonnieren. Das Abonnement informiert die Clientanwendung, wenn dem Posteingang neue e-Mails hinzugefügt werden und wenn ein Element aus dem Posteingang gelöscht wird. Das Abonnement hat einen Timeout, wenn der Client nicht innerhalb von zehn Minuten Informationen zu Ereignissen anfordert. Wenn das Abonnement abläuft, muss ein neues Abonnement eingerichtet werden, um weiterhin Benachrichtigungen anzufordern.
  
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

### <a name="pull-subscription-subscribe-request-elements"></a>Subscribe-Abonnement anforderungselemente abrufen

In der Anforderung werden folgende Elemente verwendet:
  
- [Abonnieren](subscribe.md)
    
- [PullSubscriptionRequest](pullsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [Timeout](timeout.md)
    
Um andere Optionen für die Anforderungsnachricht des Subscribe-Vorgangs zu finden, erkunden Sie die Schemahierarchie. Beginnen Sie mit dem [PullSubscriptionRequest](pullsubscriptionrequest.md) -Element. 
  
## <a name="successful-pull-subscription-subscribe-response-example"></a>Beispiel für eine erfolgreiche Abonnement Antwort für Pullabonnements

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine erfolgreiche Antwort auf das Pullabonnement dargestellt. Die Antwort enthält die Abonnement-ID und das Wasserzeichen, das verwendet wird, um das Array von Ereignissen abzurufen, die einem Abonnement zugeordnet sind. Die Abonnement-ID wird auch verwendet, um das Abonnement eines Clients von einem Abonnement abzumelden.
  
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

### <a name="pull-subscription-subscribe-response-elements"></a>Subscribe-Abonnement-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Abonnement-Nr (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="pull-subscription-subscribe-error-response-example"></a>Beispiel für subscribe-Fehlerantwort für Pullabonnement

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Fehlerantwort auf eine subscribe-Anforderung angezeigt. Der Fehler wird durch den Versuch verursacht, Benachrichtigungen mithilfe des Stellvertretungs Zugriffs zu abonnieren.
  
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

### <a name="pull-subscription-error-response-elements"></a>Elemente des Pull-Abonnement-Fehlerantwort Elements

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="push-subscription-request-example"></a>Push-Abonnementanforderung (Beispiel)

### <a name="description"></a>Beschreibung

Im folgenden Codebeispiel wird gezeigt, wie Sie ein Push-Ereignis Benachrichtigungsabonnement abonnieren. Die Anforderung identifiziert die zu überwachenden Ordner, die zu überwachenden Ereignistypen, die Häufigkeit der Statusbenachrichtigungen und die URL des Client-Webdiensts, der die Push-Benachrichtigungen überwacht.
  
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

Der Client-Webdienst muss eingerichtet sein, bevor die Push Notification subscribe-Anforderung gesendet wird. Andernfalls wird die erste Benachrichtigung nicht an einen gültigen Endpunkt gesendet, und die Push-Benachrichtigung wird nicht ausgeführt. Weitere Informationen finden Sie unter [Push Notification-Beispielanwendung](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx).
  
Beim erneuten Abonnieren wird eine neue [Abonnement-Startwert (GetEvents)](subscriptionid-getevents.md) erstellt. Verwenden Sie das Wasserzeichen eines vorherigen Abonnements zum erneuten Abonnieren an der Stelle, an der das vorherige Abonnement endete. 
  
### <a name="push-subscription-request-elements"></a>Push-Abonnement anforderungselemente

In der Anforderung werden folgende Elemente verwendet:
  
- [Abonnieren](subscribe.md)
    
- [PushSubscriptionRequest](pushsubscriptionrequest.md)
    
- [FolderIds](folderids.md)
    
- [DistinguishedFolderId](distinguishedfolderid.md)
    
- [EventTypes](eventtypes.md)
    
- [EventType](eventtype.md)
    
- [StatusFrequency](statusfrequency.md)
    
- [URL](url-ex15websvcsotherref.md)
    
## <a name="successful-push-subscription-response-example"></a>Beispiel für eine erfolgreiche Push-Abonnement Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Push-Abonnement Antwort. 
  
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

### <a name="push-subscription-response-elements"></a>Push-Abonnement-Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [SubscribeResponse](subscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [SubscribeResponseMessage](subscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
- [Abonnement-Nr (GetEvents)](subscriptionid-getevents.md)
    
- [Watermark](watermark.md)
    
## <a name="see-also"></a>Siehe auch



[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)


[Verwenden von Pullabonnements](https://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)
  
[Beispielanwendung für Pushbenachrichtigungen](https://msdn.microsoft.com/library/db1f8523-fa44-483f-bdb6-ab5939b52eee%28Office.15%29.aspx)

