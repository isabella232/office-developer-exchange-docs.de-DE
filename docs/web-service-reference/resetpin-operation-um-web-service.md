---
title: ResetPIN-Vorgang (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: Der ResetPIN-Vorgang ändert die PIN (TUI Password) in einen neuen Zufallswert.
ms.openlocfilehash: 8de64ce7a47e9c426f8eb9298e1ca00508fb616c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465492"
---
# <a name="resetpin-operation-um-web-service"></a>ResetPIN-Vorgang (um-Webdienst)

Der ResetPIN-Vorgang ändert die PIN (TUI Password) in einen neuen Zufallswert.
  
## <a name="remarks"></a>Bemerkungen

Mit dem ResetPIN-Vorgang wird eine neue PIN basierend auf den PIN-Richtlinien erstellt. Wenn der Vorgang erfolgreich war, wird eine e-Mail-Nachricht mit der neuen PIN an das Postfach des Benutzers gesendet. Wenn der Vorgang fehlschlägt, wird eine Ausnahme ausgelöst, die Informationen über den Fehler enthält.
  
## <a name="resetpin-request-example"></a>ResetPIN-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer ResetPIN-Anforderung zeigt, wie Sie eine Anforderung zum Zurücksetzen der PIN für ein Postfach bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>Erfolgreiches ResetPIN-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer ResetPIN-Antwort wird eine Antwort auf die ResetPIN-Anforderung angezeigt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[ResetPIN (um-Webdienst)](resetpin-um-web-service.md)
  
[ResetPINResponse (um-Webdienst)](resetpinresponse-um-web-service.md)

