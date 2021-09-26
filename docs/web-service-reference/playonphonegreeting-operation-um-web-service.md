---
title: PlayOnPhoneGreeting-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhoneGreeting
api_type:
- schema
ms.assetid: 6deafc40-290b-4bce-9914-b6bcc529f38a
description: Der PlayOnPhoneGreeting-Vorgang führt einen ausgehenden Anruf durch und gibt eine der beiden Begrüßungsnachrichten am Telefon wieder.
ms.openlocfilehash: 540cd44d35e70e2588446996aec19aeab17f83e9
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543135"
---
# <a name="playonphonegreeting-operation-um-web-service"></a>PlayOnPhoneGreeting-Vorgang (UM-Webdienst)

Der PlayOnPhoneGreeting-Vorgang führt einen ausgehenden Anruf durch und gibt eine der beiden Begrüßungsnachrichten am Telefon wieder.
  
## <a name="playonphonegreeting-request-example"></a>PlayOnPhoneGreeting-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer PlayOnPhoneGreeting-Anforderung zeigt, wie Sie eine Anforderung zum Tätigen eines ausgehenden Anrufs und zum Wiedergeben der normalen Begrüßungsnachricht an einem Telefon erstellen.
  
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

## <a name="successful-playonphonegreeting-response-example"></a>Beispiel für erfolgreiche PlayOnPhoneGreeting-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer PlayOnPhoneGreeting-Antwort zeigt eine Antwort auf die PlayOnPhoneGreeting-Anforderung.
  
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



[PlayOnPhoneGreeting (UM-Webdienst)](playonphonegreeting-um-web-service.md)
  
[PlayOnPhoneGreetingResponse (UM-Webdienst)](playonphonegreetingresponse-um-web-service.md)
  
[GreetingType (UM-Webdienst)](greetingtype-um-web-service.md)
  
[dialString (UM-Webdienst)](dialstring-um-web-service.md)

