---
title: ResetPIN-Vorgang (UM-Webdienst)
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
description: Der Vorgang ResetPIN die PIN-Nummer (TUI Kennwort) in einen neuen zufällig ausgewählten Wert geändert.
ms.openlocfilehash: e6417b86ce17c0d34fe857cf1209a18972cbef63
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831146"
---
# <a name="resetpin-operation-um-web-service"></a>ResetPIN-Vorgang (UM-Webdienst)

Der Vorgang ResetPIN die PIN-Nummer (TUI Kennwort) in einen neuen zufällig ausgewählten Wert geändert.
  
## <a name="remarks"></a>Hinweise

Der Vorgang ResetPIN erstellt eine neue PIN basierend auf PIN-Richtlinien. Wenn der Vorgang erfolgreich ist, wird eine E-mail-Nachricht, die die neue PIN an das Postfach des Benutzers gesendet. Wenn der Vorgang fehlschlägt, wird eine Ausnahme ausgelöst, die Informationen über den Fehler enthält.
  
## <a name="resetpin-request-example"></a>Anforderungsbeispiel ResetPIN

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung ResetPIN veranschaulicht eine Anforderung zum Zurücksetzen der PIN für ein Postfach zu bilden.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <ResetPIN xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" />
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-resetpin-response-example"></a>Erfolgreiche ResetPIN antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort ResetPIN zeigt eine Antwort auf die Anforderung ResetPIN.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <ResetPINResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[ResetPIN (UM-Webdienst)](resetpin-um-web-service.md)
  
[ResetPINResponse (UM-Webdienst)](resetpinresponse-um-web-service.md)

