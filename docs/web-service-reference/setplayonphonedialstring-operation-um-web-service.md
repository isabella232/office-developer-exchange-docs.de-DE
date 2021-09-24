---
title: SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: Der SetPlayOnPhoneDialString-Vorgang legt fest, dass die Wählzeichenfolge als Standard für den PlayOnPhone-Vorgang (UM-Webdienst) und den PlayOnPhoneGreeting-Vorgang (UM-Webdienst) verwendet wird.
ms.openlocfilehash: 89f83d7b0a1d56cb0adeccbf4fa0bb67f1197253
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531909"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)

Der SetPlayOnPhoneDialString-Vorgang legt fest, dass die Wählzeichenfolge als Standard für den [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwendet wird.
  
## <a name="setplayonphonedialstring-request-example"></a>SetPlayOnPhoneDialString-Anforderungsbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetPlayOnPhoneDialString-Anforderung zeigt, wie Sie eine Anforderung zum Festlegen der Standardwählzeichenfolge für ein Postfach erstellen.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="https://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a>Beispiel für erfolgreiche "SetPlayOnPhoneDialString"-Antwort

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetPlayOnePhoneDialString-Antwort zeigt eine Antwort auf die SetPlayOnPhoneDialString-Anforderung.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="https://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetPlayOnPhoneDialString (UM-Webdienst)](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse (UM-Webdienst)](setplayonphonedialstringresponse-um-web-service.md)
  
[dialString (UM-Webdienst)](dialstring-um-web-service.md)

