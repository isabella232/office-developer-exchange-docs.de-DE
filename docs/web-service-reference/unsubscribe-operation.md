---
title: Melden Sie sich ab Vorgang
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Unsubscribe
api_type:
- schema
ms.assetid: 994a9d2b-1501-4804-90f0-12bd914496ec
description: Der Vorgang zum Abmelden wird verwendet, um ein Pullabonnement Benachrichtigung zu beenden. Verwenden dieser Vorgang, anstatt einen Abonnement Timeout Navigate. Dieser Vorgang ist nur gültig für Pull-Benachrichtigungen.
ms.openlocfilehash: 64514a718d473f0fd7d0320bd1ccecddb1940ac8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839333"
---
# <a name="unsubscribe-operation"></a>Melden Sie sich ab Vorgang

Der Vorgang zum Abmelden wird verwendet, um ein Pullabonnement Benachrichtigung zu beenden. Verwenden dieser Vorgang, anstatt einen Abonnement Timeout Navigate. Dieser Vorgang ist nur gültig für Pull-Benachrichtigungen.
  
## <a name="unsubscribe-request-example"></a>Melden Sie sich ab anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt die XML-SOAP-Nachricht, die gesendet wird, um zu einen Client Benachrichtigungsdienst kündigen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/"
  xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types">
  <soap:Body>
    <Unsubscribe xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <SubscriptionId>e6fbf5c1-7e26-4bc6-a5f2-882063d5e34e</SubscriptionId>  
    </Unsubscribe>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-request-elements"></a>Melden Sie sich ab Anforderung Elemente

In der Anforderung werden folgende Elemente verwendet:
  
- [Melden Sie sich ab](unsubscribe.md)
    
- [SubscriptionId (GetEvents)](subscriptionid-getevents.md)
    
## <a name="successful-unsubscribe-response-example"></a>Erfolgreiche zum Abmelden antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung zum Abmelden.
  
### <a name="code"></a>Code

```xml
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" 
               xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" 
               xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Header>
    <t:ServerVersionInfo MajorVersion="8" MinorVersion="0" MajorBuildNumber="628" MinorBuildNumber="0" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" />
  </soap:Header>
  <soap:Body>
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Success">
          <m:ResponseCode>NoError</m:ResponseCode>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-response-elements"></a>Melden Sie sich ab Antwortelemente

In der Antwort werden folgende Elemente verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [Melden Sie sich ab](unsubscribe.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UnsubscribeResponseMessage](unsubscriberesponsemessage.md)
    
- [ResponseCode](responsecode.md)
    
## <a name="unsubscribe-error-response-example"></a>Melden Sie sich ab Fehler antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Fehlerantwort kündigen wird als Reaktion auf ein Versuch, kündigen mithilfe einer Abonnement-ID, die nicht gefunden werden kann im Exchange-Speicher.
  
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
    <UnsubscribeResponse xmlns:m="http://schemas.microsoft.com/exchange/services/2006/messages" 
                         xmlns:t="http://schemas.microsoft.com/exchange/services/2006/types" 
                         xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <m:ResponseMessages>
        <m:UnsubscribeResponseMessage ResponseClass="Error">
          <m:MessageText>The specified subscription was not found.</m:MessageText>
          <m:ResponseCode>ErrorSubscriptionNotFound</m:ResponseCode>
          <m:DescriptiveLinkKey>0</m:DescriptiveLinkKey>
        </m:UnsubscribeResponseMessage>
      </m:ResponseMessages>
    </UnsubscribeResponse>
  </soap:Body>
</soap:Envelope>
```

### <a name="unsubscribe-error-response-elements"></a>Melden Sie sich ab Antwortelemente Fehler

Folgende Elemente werden in der Fehlerantwort verwendet:
  
- [ServerVersionInfo](serverversioninfo.md)
    
- [UnsubscribeResponse](unsubscriberesponse.md)
    
- [ResponseMessages](responsemessages.md)
    
- [UnsubscribeResponseMessage](unsubscriberesponsemessage.md)
    
- [MessageText](messagetext.md)
    
- [ResponseCode](responsecode.md)
    
- [DescriptiveLinkKey](descriptivelinkkey.md)
    
## <a name="see-also"></a>Siehe auch

- [Vorgang abonnieren](subscribe-operation.md)
- [GetEvents-Vorgang](getevents-operation.md)
- [Mithilfe von Pullabonnements](http://msdn.microsoft.com/library/f956bc0e-2b25-4613-966b-54c65456897c%28Office.15%29.aspx)

