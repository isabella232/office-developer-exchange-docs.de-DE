---
title: Trennen Sie (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: Der Trennvorgang beendet den Anruf, der durch die angegebene CallId (UM-Webdienst) bezeichnet wird.
ms.openlocfilehash: 1e04e65fa1951a6aa46e2c8b6dd5fe524c84a8fc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758018"
---
# <a name="disconnect-operation-um-web-service"></a>Trennen Sie (UM-Webdienst)

Der Trennvorgang beendet den Anruf, der durch die angegebene [CallId (UM-Webdienst)](callid-um-web-service.md)bezeichnet wird.
  
## <a name="disconnect-request-example"></a>Trennen Sie anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel für eine Anforderung zum Trennen der veranschaulicht das Formular einer Anforderung an eine Verbindung zu trennen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a>Erfolgreiche Verbindung trennen antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort trennen zeigt eine Antwort auf die Anforderung zum Trennen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Trennen Sie (UM-Webdienst)](disconnect-um-web-service.md) 
- [DisconnectResponse (UM-Webdienst)](disconnectresponse-um-web-service.md) 
- [CallId (UM-Webdienst)](callid-um-web-service.md)

