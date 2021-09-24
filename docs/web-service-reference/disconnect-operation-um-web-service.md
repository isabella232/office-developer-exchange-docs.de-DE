---
title: Disconnect-Vorgange (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Disconnect
api_type:
- schema
ms.assetid: a987000b-d6e6-49d7-944c-e9c278d0236f
description: Der Disconnect-Vorgang beendet den Aufruf, der von der angegebenen CallId (UM-Webdienst) identifiziert wird.
ms.openlocfilehash: 42e069233fbfc255d43983571c0bb28475a1fe90
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522012"
---
# <a name="disconnect-operation-um-web-service"></a>Disconnect-Vorgange (UM-Webdienst)

Der Disconnect-Vorgang beendet den Aufruf, der durch die angegebene [CallId (UM-Webdienst)](callid-um-web-service.md)identifiziert wird.
  
## <a name="disconnect-request-example"></a>Disconnect-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Disconnect-Anforderung zeigt, wie Sie eine Anforderung zum Trennen eines Anrufs erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <Disconnect xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <CallId>MDlkZjllZGMtNGUyMy00NzA5LWJkYWYtN2JlMjBjYjBhZTU2QGRmLWV1bS0wMS5leGNoYW5nZS5jb3JwLm1pY3Jvc29mdC5jb20=</CallId>
    </Disconnect>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-disconnect-response-example"></a>Beispiel für erfolgreiche Disconnect-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Disconnect-Antwort zeigt eine Antwort auf die Disconnect-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <DisconnectResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch

- [Disconnect (UM-Webdienst)](disconnect-um-web-service.md) 
- [DisconnectResponse (UM-Webdienst)](disconnectresponse-um-web-service.md) 
- [CallId (UM-Webdienst)](callid-um-web-service.md)

