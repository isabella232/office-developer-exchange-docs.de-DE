---
title: SetOofStatus-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetOofStatus
api_type:
- schema
ms.assetid: 97c271e9-506e-43eb-89cd-46803fc47ee5
description: Der SetOofStatus-Vorgang legt einen Wert fest, der angibt, ob die OOF-Begrüßung (Out of Office) für den Benutzer wiedergegeben werden soll, der die Anforderung sendet.
ms.openlocfilehash: ce736e7d7bea39f65843923187af3ae616ae1c86
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544752"
---
# <a name="setoofstatus-operation-um-web-service"></a>SetOofStatus-Vorgang (UM-Webdienst)

Der SetOofStatus-Vorgang legt einen Wert fest, der angibt, ob die OOF-Begrüßung (Out of Office) für den Benutzer wiedergegeben werden soll, der die Anforderung sendet.
  
## <a name="setoofstatus-request-example"></a>SetOofStatus-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetOofStatus-Anforderung zeigt, wie Sie eine Anforderung zum Aktivieren der Out of Office-Begrüßung für ein Postfach erstellen.
  
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

## <a name="successful-setoofstatus-response-example"></a>Beispiel für erfolgreiche SetOofStatus-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetOofStatus-Antwort zeigt eine Antwort auf die SetOofStatus-Anforderung.
  
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



[SetOofStatus (UM-Webdienst)](setoofstatus-um-web-service.md)
  
[SetOofStatusResponse (UM-Webdienst)](setoofstatusresponse-um-web-service.md)
  
[Status (UM-Webdienst – SetOofStatus)](status-um-web-servicesetoofstatus.md)

