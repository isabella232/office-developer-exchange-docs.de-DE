---
title: PlayOnPhone-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- PlayOnPhone
api_type:
- schema
ms.assetid: 7d55be55-f8b6-4e96-a61e-26fa190217fd
description: Der PlayOnPhone-Vorgang tätigt einen ausgehenden Anruf und gibt eine angegebene Nachricht über das Telefon wieder, das durch das dialtype-Element angegeben wird.
ms.openlocfilehash: c5ff82bcd822aa2c659d1782ea4a1349d198bc80
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466234"
---
# <a name="playonphone-operation-um-web-service"></a>PlayOnPhone-Vorgang (um-Webdienst)

Der PlayOnPhone-Vorgang tätigt einen ausgehenden Anruf und gibt eine angegebene Nachricht über das Telefon wieder, das durch das **dialtype** -Element angegeben wird. 
  
## <a name="playonphone-request-example"></a>PlayOnPhone-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer PlayOnPhone-Anforderung wird gezeigt, wie Sie eine Anforderung zum Erstellen eines ausgehenden Anrufs und zum Abspielen einer Nachricht bilden.
  
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

## <a name="successful-playonphone-response-example"></a>Erfolgreiches PlayOnPhone-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer PlayOnPhone-Antwort wird eine Antwort auf die PlayOnPhone-Anforderung angezeigt.
  
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



[PlayOnPhone (um-Webdienst)](playonphone-um-web-service.md)
  
[PlayOnPhoneResponse (um-Webdienst)](playonphoneresponse-um-web-service.md)
  
[PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)

