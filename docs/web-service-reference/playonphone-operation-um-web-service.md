---
title: PlayOnPhone-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: Der PlayOnPhone-Vorgang führt einen ausgehenden Anruf durch und gibt eine angegebene Nachricht über das durch das DialString-Element angegebene Telefon wieder.
ms.openlocfilehash: 4d18727da18c36e6410c3cc6ab3bbf873993be72
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516564"
---
# <a name="playonphone-operation-um-web-service"></a>PlayOnPhone-Vorgang (UM-Webdienst)

Der PlayOnPhone-Vorgang führt einen ausgehenden Anruf durch und gibt eine angegebene Nachricht über das durch das **DialString-Element** angegebene Telefon wieder. 
  
## <a name="playonphone-request-example"></a>PlayOnPhone-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer PlayOnPhone-Anforderung zeigt, wie Sie eine Anforderung zum Tätigen eines ausgehenden Anrufs und zum Wiedergeben einer Nachricht erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <PlayOnPhone xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <entryId>AAAAAGsd2rbQLVtLobUGbrq/9IUHAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAACxVpEl+KVVLl957wp//x6UAGAetcDUAAA==</entryId>
      <DialString>12345</DialString>
    </PlayOnPhone>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-playonphone-response-example"></a>Beispiel für erfolgreiche PlayOnPhone-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer PlayOnPhone-Antwort zeigt eine Antwort auf die PlayOnPhone-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <PlayOnPhoneResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <PlayOnPhoneResponse>NDEzYjEzNmMtZTE2Zi00NTJlLWI3YzctNDhkMTE3MDE3YjlmQGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</PlayOnPhoneResponse> 
    </PlayOnPhoneResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[PlayOnPhone (UM-Webdienst)](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse (UM-Webdienst)](playonphoneresponse-um-web-service.md)
  
[PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)

