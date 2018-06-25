---
title: IsUMEnabled-Vorgang (UM-Webdienst)
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
description: Der Vorgang IsUMEnabled bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
ms.openlocfilehash: 9d94a359d6b11e41762d21aa2fe5501bd9f7b577
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830107"
---
# <a name="isumenabled-operation-um-web-service"></a>IsUMEnabled-Vorgang (UM-Webdienst)

Der Vorgang IsUMEnabled bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
  
## <a name="isumenabled-request-example"></a>Anforderungsbeispiel IsUMEnabled

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird einer Anforderung IsUMEnabled veranschaulicht das Formular einer Anforderung, um zu bestimmen, ob ein Postfach für Unified Messaging aktiviert ist.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>Erfolgreiche IsUMEnabled antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel zeigt eine erfolgreiche Antwort auf eine Anforderung IsUMEnabled.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <IsUMEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <IsUMEnabledResponse>true</IsUMEnabledResponse> 
    </IsUMEnabledResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[IsUMEnabled (UM-Webdienst)](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse (UM-Webdienst)](isumenabledresponse-um-web-service.md)


[Unified Messaging Web Service XML-Elemente für Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

