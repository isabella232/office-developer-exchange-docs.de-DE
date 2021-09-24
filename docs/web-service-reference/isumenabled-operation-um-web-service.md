---
title: IsUMEnabled-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- IsUMEnabled
api_type:
- schema
ms.assetid: fbe6cd95-f7a5-42b9-8a9d-b6159a269d55
description: Der IsUMEnabled-Vorgang bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
ms.openlocfilehash: 2c637711fc34a1d1ccc484b14be3199632aaaaa3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514459"
---
# <a name="isumenabled-operation-um-web-service"></a>IsUMEnabled-Vorgang (UM-Webdienst)

Der IsUMEnabled-Vorgang bestimmt, ob ein Postfach für Unified Messaging aktiviert ist.
  
## <a name="isumenabled-request-example"></a>IsUMEnabled-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer IsUMEnabled-Anforderung zeigt, wie Sie eine Anforderung erstellen, um zu bestimmen, ob ein Postfach für Unified Messaging aktiviert ist.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <IsUMEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-isumenabled-response-example"></a>Beispiel für erfolgreiche IsUMEnabled-Antwort

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



[IsUMEnabled (UM-Webdienst)](isumenabled-um-web-service.md)
  
[IsUMEnabledResponse (UM-Webdienst)](isumenabledresponse-um-web-service.md)


[UNIFIED Messaging-Webdienst-XML-Elemente für Exchange](unified-messaging-web-service-xml-elements-for-exchange.md)

