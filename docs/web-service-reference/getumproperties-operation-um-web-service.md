---
title: GetUMProperties-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- GetUMProperties
api_type:
- schema
ms.assetid: 301fb9a3-67df-44c4-8ffe-0600237fc344
description: Der GetUMProperties-Vorgang ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers ab, der die Anforderung stellt.
ms.openlocfilehash: 8d051196e83e1f927692b517e1ab3e95bb0060db
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515817"
---
# <a name="getumproperties-operation-um-web-service"></a>GetUMProperties-Vorgang (UM-Webdienst)

Der GetUMProperties-Vorgang ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers ab, der die Anforderung stellt.
  
## <a name="getumproperties-request-example"></a>GetUMProperties-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer GetUMProperties-Anforderung zeigt, wie Sie eine Anforderung zum Abrufen der Unified Messaging-Eigenschaften eines Postfachs erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a>Beispiel für erfolgreiche GetUMProperties-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer GetUMProperties-Antwort zeigt eine Antwort auf die GetUMProperties-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <GetUMPropertiesResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
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

