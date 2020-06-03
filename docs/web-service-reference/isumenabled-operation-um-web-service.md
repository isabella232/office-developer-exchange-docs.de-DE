---
title: IsUMEnabled-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: Der IsUMEnabled-Vorgang bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
ms.openlocfilehash: b1478f5a113059251fe1b036ac7d77e5a4ab4f50
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458236"
---
# <a name="isumenabled-operation-um-web-service"></a>IsUMEnabled-Vorgang (um-Webdienst)

Der IsUMEnabled-Vorgang bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
  
## <a name="isumenabled-request-example"></a>IsUMEnabled-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer IsUMEnabled-Anforderung wird gezeigt, wie Sie eine Anforderung zum bestimmen, ob ein Postfach für Unified Messaging aktiviert ist, bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>Erfolgreiches IsUMEnabled-Antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine IsUMEnabled-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[IsUMEnabled (um-Webdienst)](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse (um-Webdienst)](isumenabledresponse-um-web-service.md)


[XML-Elemente des Unified Messaging-Webdiensts für Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

