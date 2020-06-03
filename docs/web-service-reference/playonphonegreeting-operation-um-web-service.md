---
title: PlayOnPhoneGreeting-Vorgang (um-Webdienst)
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
description: Der PlayOnPhoneGreeting-Vorgang nimmt einen ausgehenden Anruf vor und gibt eine der beiden Grußnachrichten am Telefon wieder.
ms.openlocfilehash: 3af120b9ac8d7a368742fad2850c924228488662
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528895"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>PlayOnPhoneGreeting-Vorgang (um-Webdienst)

Der PlayOnPhoneGreeting-Vorgang nimmt einen ausgehenden Anruf vor und gibt eine der beiden Grußnachrichten am Telefon wieder.
  
## <a name="playonphonegreeting-request-example"></a>PlayOnPhoneGreeting-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer PlayOnPhoneGreeting-Anforderung wird gezeigt, wie Sie eine Anforderung zum Tätigen eines ausgehenden Anrufs und zum Abspielen der normalen Begrüßungsnachricht auf einem Telefon bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhoneGreeting xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <GreetingType>NormalCustom</GreetingType>
      <DialString>12345</DialString>
    </PlayOnPhoneGreeting>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphonegreeting-response-example"></a>Erfolgreiches PlayOnPhoneGreeting-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer PlayOnPhoneGreeting-Antwort wird eine Antwort auf die PlayOnPhoneGreeting-Anforderung angezeigt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneGreetingResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
    <PlayOnPhoneGreetingResponse>MjA4MTQ5MmItMTBmZC00ZGFmLThiMzEtNDllNDJjM2Y3MjIxQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneGreetingResponse> 
    </PlayOnPhoneGreetingResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[PlayOnPhoneGreeting (um-Webdienst)](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse (um-Webdienst)](playonphonegreetingresponse-um-web-service.md)
  
[Greetingtype (um-Webdienst)](greetingtype-um-web-service.md)
  
[Wähl Dienst (um-Webdienst)](dialstring-um-web-service.md)

