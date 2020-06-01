---
title: GetCallInfo-Vorgang (um-Webdienst)
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
description: Der GetCallInfo-Vorgang gibt den Status des ausgehenden Anrufs zurück, der von der "Calling"-Dienst (um-Webdienst) angegeben wird.
ms.openlocfilehash: 6b5664dfe16f9c74cc7175098145141b815a6355
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461240"
---
# <a name="getcallinfo-operation-um-web-service"></a>GetCallInfo-Vorgang (um-Webdienst)

Der GetCallInfo-Vorgang gibt den Status des ausgehenden Anrufs zurück, der von der ["Calling"-Dienst (um-Webdienst)](callid-um-web-service.md)angegeben wird.
  
## <a name="getcallinfo-request-example"></a>GetCallInfo-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer GetCallInfo-Anforderung wird gezeigt, wie eine Anforderung zum Abrufen von Informationen zu einem angegebenen ausgehenden Aufruf bildet.
  
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

## <a name="successful-getcallinfo-response-example"></a>Erfolgreiches GetCallInfo-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer GetCallInfo-Antwort wird eine Antwort auf eine GetCallInfo-Anforderung angezeigt.
  
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



[GetCallInfo (um-Webdienst)](getcallinfo-um-web-service.md)
  
[GetCallInfoResponse (um-Webdienst)](getcallinforesponse-um-web-service.md)
  
[Anrufdienst (um-Webdienst)](callid-um-web-service.md)
  
[CallState (um-Webdienst)](callstate-um-web-service.md)
  
[EventCause (um-Webdienst)](eventcause-um-web-service.md)

