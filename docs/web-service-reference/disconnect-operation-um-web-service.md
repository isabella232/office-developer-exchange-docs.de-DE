---
title: Trennungsvorgang (um-Webdienst)
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
description: Durch den Vorgang zum Trennen der Verbindung wird der Anruf beendet, der durch den angegebenen Aufrufer (um-Webdienst) identifiziert wird.
ms.openlocfilehash: a1268f9ea3d879f472e019bf1847fc13d65d1819
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529070"
---
# <a name="disconnect-operation-um-web-service"></a>Trennungsvorgang (um-Webdienst)

Durch den Vorgang zum Trennen der Verbindung wird der Anruf beendet, der durch den angegebenen [Aufrufer (um-Webdienst)](callid-um-web-service.md)identifiziert wird.
  
## <a name="disconnect-request-example"></a>Trenn Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer Anforderung für eine Trennung wird gezeigt, wie eine Anforderung zum Trennen eines Anrufs bildet.
  
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

## <a name="successful-disconnect-response-example"></a>Beispiel für erfolgreiche Trennungs Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Disconnect-Antwort zeigt eine Antwort auf die Anforderung zum Trennen der Verbindung.
  
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

- [Trennen (um-Webdienst)](disconnect-um-web-service.md) 
- [DisconnectResponse (um-Webdienst)](disconnectresponse-um-web-service.md) 
- [Anrufdienst (um-Webdienst)](callid-um-web-service.md)

