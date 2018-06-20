---
title: GetUMProperties-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: Der Vorgang GetUMProperties Ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers, der die Anforderung stellt.
ms.openlocfilehash: 8878099bbd907fe0648f7d64dde3cd9600c2c45f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829678"
---
# <a name="getumproperties-operation-um-web-service"></a>GetUMProperties-Vorgang (UM-Webdienst)

Der Vorgang GetUMProperties Ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers, der die Anforderung stellt.
  
## <a name="getumproperties-request-example"></a>Anforderungsbeispiel GetUMProperties

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung GetUMProperties veranschaulicht eine Anforderung zum Abrufen der Unified Messaging-Eigenschaften eines Postfachs zu bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a>Erfolgreiche GetUMProperties antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort GetUMProperties zeigt eine Antwort auf die Anforderung GetUMProperties.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
      <GetUMPropertiesResponse>
        <OofStatus>false</OofStatus> 
        <MissedCallNotificationEnabled>true</MissedCallNotificationEnabled> 
        <PlayOnPhoneDialString>12345</PlayOnPhoneDialString> 
        <TelephoneAccessNumbers>54321</TelephoneAccessNumbers> 
        <TelephoneAccessFolderEmail>AAAAAGsd2rbQLVtLobUGbrq/9IUBAEX2ikn/L8JJtI5WHI0FAW8AAAFXHhsAAA==</TelephoneAccessFolderEmail> 
      </GetUMPropertiesResponse>
    </GetUMPropertiesResponse>
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[GetUMProperties (UM-Webdienst)](getumproperties-um-web-service.md)
  
[GetUMPropertiesResponse (UM-Webdienst)](getumpropertiesresponse-um-web-service.md)

