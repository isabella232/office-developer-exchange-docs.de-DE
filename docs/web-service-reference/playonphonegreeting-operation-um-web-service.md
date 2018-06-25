---
title: PlayOnPhoneGreeting-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: Der Vorgang PlayOnPhoneGreeting macht einen ausgehenden Anruf und eine der zwei Begrüßung angezeigt am Telefon abgespielt.
ms.openlocfilehash: 85ba76c7638911678c1ef1aef88f47fdab2c6a4e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830828"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>PlayOnPhoneGreeting-Vorgang (UM-Webdienst)

Der Vorgang PlayOnPhoneGreeting macht einen ausgehenden Anruf und eine der zwei Begrüßung angezeigt am Telefon abgespielt.
  
## <a name="playonphonegreeting-request-example"></a>Anforderungsbeispiel PlayOnPhoneGreeting

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung PlayOnPhoneGreeting bilden eine Anforderung zum Tätigen eines ausgehenden Anrufs und Wiedergabe der Nachricht normal Ansage über ein Telefon veranschaulicht.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a>Erfolgreiche PlayOnPhoneGreeting antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort PlayOnPhoneGreeting zeigt eine Antwort auf die Anforderung PlayOnPhoneGreeting.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[PlayOnPhoneGreeting (UM-Webdienst)](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse (UM-Webdienst)](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType (UM-Webdienst)](greetingtype-um-web-service.md)
  
[DialString (UM-Webdienst)](dialstring-um-web-service.md)

