---
title: SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- SetPlayOnPhoneDialString
api_type:
- schema
ms.assetid: a68479f2-d900-4dd8-a5ce-dbea8247e841
description: SetPlayOnPhoneDialString-Vorgang wird die Zugriffsnummer Zeichenfolge, die als Standard für den Vorgang PlayOnPhone (UM-Webdienst) und den PlayOnPhoneGreeting-Vorgang (UM-Webdienst) verwenden.
ms.openlocfilehash: 0d1a879784740777e5eab0cbd5f85e59a6479461
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831446"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>SetPlayOnPhoneDialString-Vorgang (UM-Webdienst)

SetPlayOnPhoneDialString-Vorgang wird die Zugriffsnummer Zeichenfolge, die als Standard für den [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwenden.
  
## <a name="setplayonphonedialstring-request-example"></a>Anforderungsbeispiel SetPlayOnPhoneDialString

### <a name="description"></a>Beschreibung

Im folgenden Beispiel wird eine Anforderung SetPlayOnPhoneDialString veranschaulicht das Formular einer Anforderung an die Standardzeichenfolge Zugriffsnummern für ein Postfach festgelegt.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8"?>
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/">
  <soap:Body>
    <SetPlayOnPhoneDialString xmlns="http://schemas.microsoft.com/exchange/services/2006/messages">
        <dialString>12345</dialString>
    </SetPlayOnPhoneDialString>
  </soap:Body>
</soap:Envelope>
```

## <a name="successful-setplayonphonedialstring-response-example"></a>Erfolgreiche SetPlayOnPhoneDialString antwortbeispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer Antwort SetPlayOnePhoneDialString zeigt eine Antwort auf die Anforderung SetPlayOnPhoneDialString.
  
### <a name="code"></a>Code

```XML
<?xml version="1.0" encoding="utf-8" ?> 
<soap:Envelope xmlns:soap="http://schemas.xmlsoap.org/soap/envelope/" xmlns:xsi="http://www.w3.org/2001/XMLSchema-instance" xmlns:xsd="http://www.w3.org/2001/XMLSchema">
  <soap:Body>
    <SetPlayOnPhoneDialStringResponse xmlns="http://schemas.microsoft.com/exchange/services/2006/messages" /> 
  </soap:Body>
</soap:Envelope>
```

## <a name="see-also"></a>Siehe auch



[SetPlayOnPhoneDialString (UM-Webdienst)](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse (UM-Webdienst)](setplayonphonedialstringresponse-um-web-service.md)
  
[DialString (UM-Webdienst)](dialstring-um-web-service.md)

