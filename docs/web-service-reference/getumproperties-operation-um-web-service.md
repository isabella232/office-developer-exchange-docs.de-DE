---
title: GetUMProperties-Vorgang (um-Webdienst)
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
description: Der GetUMProperties-Vorgang ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers ab, der die Anforderung macht.
ms.openlocfilehash: 42176d9cd0288af6515aeea616a4f216a419410c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462472"
---
# <a name="getumproperties-operation-um-web-service"></a>GetUMProperties-Vorgang (um-Webdienst)

Der GetUMProperties-Vorgang ruft alle Unified Messaging-Eigenschaften für das Postfach des Benutzers ab, der die Anforderung macht.
  
## <a name="getumproperties-request-example"></a>GetUMProperties-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer GetUMProperties-Anforderung wird gezeigt, wie Sie eine Anforderung zum Abrufen der Unified Messaging-Eigenschaften eines Postfachs bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <GetUMProperties xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-getumproperties-response-example"></a>Erfolgreiches GetUMProperties-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer GetUMProperties-Antwort wird eine Antwort auf die GetUMProperties-Anforderung angezeigt.
  
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



[GetUMProperties (um-Webdienst)](getumproperties-um-web-service.md)
  
[GetUMPropertiesResponse (um-Webdienst)](getumpropertiesresponse-um-web-service.md)

