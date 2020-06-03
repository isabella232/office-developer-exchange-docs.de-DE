---
title: SetOofStatus-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: Der SetOofStatus-Vorgang legt einen Wert fest, der angibt, ob die Abwesenheit (Out of Office, OOF) Begrüßung für den Benutzer wiedergegeben werden soll, der die Anforderung stellt.
ms.openlocfilehash: 2311b6137ac25d15ad3d06668450c1d0f7ec1fad
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467354"
---
# <a name="setoofstatus-operation-um-web-service"></a>SetOofStatus-Vorgang (um-Webdienst)

Der SetOofStatus-Vorgang legt einen Wert fest, der angibt, ob die Abwesenheit (Out of Office, OOF) Begrüßung für den Benutzer wiedergegeben werden soll, der die Anforderung stellt.
  
## <a name="setoofstatus-request-example"></a>SetOofStatus-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SetOofStatus-Anforderung wird gezeigt, wie Sie eine Anforderung zum Aktivieren der Abwesenheits Begrüßung für ein Postfach bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a>Erfolgreiches SetOofStatus-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SetOofStatus-Antwort wird eine Antwort auf die SetOofStatus-Anforderung angezeigt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetOofStatus (um-Webdienst)](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse (um-Webdienst)](setoofstatusresponse-um-web-service.md)
  
[Status (um-Webdienst – SetOofStatus)](status-um-web-servicesetoofstatus.md)

