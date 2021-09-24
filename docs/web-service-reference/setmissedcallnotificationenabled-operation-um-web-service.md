---
title: SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetMissedCallNotificationEnabled
api_type:
- schema
ms.assetid: 6693b5db-ac6b-43bc-af83-a9c94fc425bf
description: Der SetMissedCallNotificationEnabled-Vorgang aktiviert oder deaktiviert Benachrichtigungen über verpasste Anrufe.
ms.openlocfilehash: 31f59887041aac02e5876b596931902373870203
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521417"
---
# <a name="setmissedcallnotificationenabled-operation-um-web-service"></a>SetMissedCallNotificationEnabled-Vorgang (UM-Webdienst)

Der SetMissedCallNotificationEnabled-Vorgang aktiviert oder deaktiviert Benachrichtigungen über verpasste Anrufe.
  
## <a name="setmissedcallnotificationenabled-request-example"></a>SetMissedCallNotificationEnabled-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetMissedCallNotificationEnabled-Anforderung zeigt, wie Sie eine Anforderung zum Aktivieren von Benachrichtigungen über verpasste Anrufe erstellen.
  
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

## <a name="successful-setmissedcallnotificationenabled-response-example"></a>Beispiel für erfolgreiche "SetMissedCallNotificationEnabled"-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer PlayOnPhoneGreeting-Antwort zeigt eine Antwort auf die Anforderung "SetMissedCallNotificationEnabled".
  
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



[SetMissedCallNotificationEnabled (UM-Webdienst)](setmissedcallnotificationenabled-um-web-service.md)
  
[SetMissedCallNotificationEnabledResponse (UM-Webdienst)](setmissedcallnotificationenabledresponse-um-web-service.md)
  
[Status (UM-Webdienst – SetMissedCallNotificationEnabled)](status-um-web-servicesetmissedcallnotificationenabled.md)

