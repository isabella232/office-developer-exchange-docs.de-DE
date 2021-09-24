---
title: GetCallInfo-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetCallInfo
api_type:
- schema
ms.assetid: 6bccd418-caf7-4eb9-8a6f-410e56a635c3
description: Der GetCallInfo-Vorgang gibt den Status des ausgehenden Anrufs zurück, der von CallId (UM-Webdienst) angegeben wird.
ms.openlocfilehash: 0563190ab267b3a48d7ccacbdb1e136c6e3da0b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509944"
---
# <a name="getcallinfo-operation-um-web-service"></a>GetCallInfo-Vorgang (UM-Webdienst)

Der GetCallInfo-Vorgang gibt den Status des ausgehenden Anrufs zurück, der durch [CallId (UM-Webdienst)](callid-um-web-service.md)angegeben wird.
  
## <a name="getcallinfo-request-example"></a>GetCallInfo-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer GetCallInfo-Anforderung zeigt, wie Sie eine Anforderung zum Abrufen von Informationen zu einem angegebenen ausgehenden Anruf erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetCallInfo xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </GetCallInfo>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getcallinfo-response-example"></a>Beispiel für erfolgreiche GetCallInfo-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer GetCallInfo-Antwort zeigt eine Antwort auf eine GetCallInfo-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetCallInfoResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

