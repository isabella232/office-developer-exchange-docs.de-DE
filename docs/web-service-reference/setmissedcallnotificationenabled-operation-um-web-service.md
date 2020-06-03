---
title: SetMissedCallNotificationEnabled-Vorgang (um-Webdienst)
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
description: Der SetMissedCallNotificationEnabled-Vorgang aktiviert oder deaktiviert Benachrichtigungen über verpasste Anrufe.
ms.openlocfilehash: ca4942942a81bc187e8e18a5e6f003f8587f79d1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467396"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>SetMissedCallNotificationEnabled-Vorgang (um-Webdienst)

Der SetMissedCallNotificationEnabled-Vorgang aktiviert oder deaktiviert Benachrichtigungen über verpasste Anrufe.
  
## <a name="setmissedcallnotificationenabled-request-example"></a>SetMissedCallNotificationEnabled-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SetMissedCallNotificationEnabled-Anforderung wird gezeigt, wie Sie eine Anforderung zum Aktivieren von Benachrichtigungen über verpasste Anrufe bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetMissedCallNotificationEnabled xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetMissedCallNotificationEnabled>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>Erfolgreiches SetMissedCallNotificationEnabled-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer PlayOnPhoneGreeting-Antwort wird eine Antwort auf die SetMissedCallNotificationEnabled-Anforderung angezeigt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetMissedCallNotificationEnabledResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetMissedCallNotificationEnabled (um-Webdienst)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (um-Webdienst)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status (um-Webdienst – SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)

