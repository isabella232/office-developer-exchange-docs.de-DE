---
title: GetCallInfo-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: Der Vorgang GetCallInfo wird der Status über den ausgehenden Anruf, der vom CallId (UM-Webdienst) angegeben wird zurückgegeben.
ms.openlocfilehash: 36f9cba3690520ebb457a4cb2bfbcde3fea4b8dc
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758591"
---
# <a name="getcallinfo-operation-um-web-service"></a>GetCallInfo-Vorgang (UM-Webdienst)

Der Vorgang GetCallInfo wird der Status über den ausgehenden Anruf, der vom [CallId (UM-Webdienst)](callid-um-web-service.md)angegeben wird zurückgegeben.
  
## <a name="getcallinfo-request-example"></a>Anforderungsbeispiel GetCallInfo

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung GetCallInfo veranschaulicht eine Anforderung zum Abrufen von Informationen zu einem angegebenen ausgehender Anrufe bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a>Erfolgreiche GetCallInfo antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort GetCallInfo zeigt eine Antwort auf eine GetCallInfo an.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetCallInfoResponse>
        <CallState>Connected</CallState> 
        <EventCause>None</EventCause> 
      </GetCallInfoResponse>
    </GetCallInfoResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[GetCallInfo (UM-Webdienst)](getcallinfo-um-web-service.md)
  
[GetCallInfoResponse (UM-Webdienst)](getcallinforesponse-um-web-service.md)
  
[CallId (UM-Webdienst)](callid-um-web-service.md)
  
[CallState (UM-Webdienst)](callstate-um-web-service.md)
  
[EventCause (UM-Webdienst)](eventcause-um-web-service.md)

