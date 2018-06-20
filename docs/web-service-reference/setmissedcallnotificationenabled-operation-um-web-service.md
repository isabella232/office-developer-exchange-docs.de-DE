---
title: SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: Der Vorgang SetMissedCallNotificationEnabled aktiviert oder deaktiviert die Benachrichtigungen über verpasste Anrufe.
ms.openlocfilehash: be9479d6ed2c5238ed19c3d22e028fca62b8deed
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831434"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)

Der Vorgang SetMissedCallNotificationEnabled aktiviert oder deaktiviert die Benachrichtigungen über verpasste Anrufe.
  
## <a name="setmissedcallnotificationenabled-request-example"></a>Anforderungsbeispiel SetMissedCallNotificationEnabled

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung SetMissedCallNotificationEnabled veranschaulicht eine Anforderung zum Aktivieren von Benachrichtigungen über verpasste Anrufe bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>Erfolgreiche SetMissedCallNotificationEnabled antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort PlayOnPhoneGreeting zeigt eine Antwort auf die Anforderung SetMissedCallNotificationEnabled.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetMissedCallNotificationEnabled (UM-Webdienst)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (UM-Webdienst)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status (UM-Webdienst - SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)

