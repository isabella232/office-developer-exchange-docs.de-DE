---
title: ResetPIN-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- ResetPIN
api_type:
- schema
ms.assetid: c0f14a15-3389-4311-8bac-f87930c5f5d4
description: Der ResetPIN-Vorgang ändert die PIN (PASSWORD-Kennwort) in einen neuen Zufallswert.
ms.openlocfilehash: 12f1e5719184df84f6c29ab3d02cc362f87abc76
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539108"
---
# <a name="resetpin-operation-um-web-service"></a>ResetPIN-Vorgang (UM-Webdienst)

Der ResetPIN-Vorgang ändert die PIN (PASSWORD-Kennwort) in einen neuen Zufallswert.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der ResetPIN-Vorgang erstellt eine neue PIN basierend auf den PIN-Richtlinien. Wenn der Vorgang erfolgreich ist, wird eine E-Mail-Nachricht mit der neuen PIN an das Postfach des Benutzers gesendet. Wenn der Vorgang fehlschlägt, wird eine Ausnahme ausgelöst, die Informationen zu dem Fehler enthält.
  
## <a name="resetpin-request-example"></a>ResetPIN-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer ResetPIN-Anforderung zeigt, wie Sie eine Anforderung zum Zurücksetzen der PIN für ein Postfach erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>Beispiel für erfolgreiche ResetPIN-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer ResetPIN-Antwort zeigt eine Antwort auf die ResetPIN-Anforderung.
  
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



[ResetPIN (UM-Webdienst)](resetpin-um-web-service.md)
  
[ResetPINResponse (UM-Webdienst)](resetpinresponse-um-web-service.md)

