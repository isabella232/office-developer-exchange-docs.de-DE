---
title: SetOofStatus-Vorgang (UM-Webdienst)
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
description: Der Vorgang SetOofStatus Festlegen eines Werts, das angibt, ob die Ansage Out of Office (OOF) für den Benutzer wiedergegeben werden sollte, der die Anforderung stellt.
ms.openlocfilehash: 2bb1deeec8ddb5be56979bfb2fae3396672298a3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831445"
---
# <a name="setoofstatus-operation-um-web-service"></a>SetOofStatus-Vorgang (UM-Webdienst)

Der Vorgang SetOofStatus Festlegen eines Werts, das angibt, ob die Ansage Out of Office (OOF) für den Benutzer wiedergegeben werden sollte, der die Anforderung stellt.
  
## <a name="setoofstatus-request-example"></a>Anforderungsbeispiel SetOofStatus

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung SetOofStatus veranschaulicht das Formular einer Anforderung an den abwesenheitsansage für ein Postfach zu aktivieren.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetOofStatus xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <status>true</status>
    </SetOofStatus>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setoofstatus-response-example"></a>Erfolgreiche SetOofStatus antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort SetOofStatus zeigt eine Antwort auf die Anforderung SetOofStatus.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetOofStatusResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetOofStatus (UM-Webdienst)](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse (UM-Webdienst)](setoofstatusresponse-um-web-service.md)
  
[Status (UM-Webdienst - SetOofStatus)](status-um-web-servicesetoofstatus.md)

