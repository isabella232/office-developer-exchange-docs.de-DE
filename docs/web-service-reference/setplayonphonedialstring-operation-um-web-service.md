---
title: SetPlayOnPhoneDialString-Vorgang (um-Webdienst)
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
description: Mit dem SetPlayOnPhoneDialString-Vorgang wird die Wählzeichenfolge festgelegt, die als Standard für den PlayOnPhone-Vorgang (um-Webdienst) und den PlayOnPhoneGreeting-Vorgang (um-Webdienst) verwendet werden soll.
ms.openlocfilehash: 7df806eedc2d6d037394f31ec4ccbfe28aaf3372
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458642"
---
# <a name="setplayonphonedialstring-operation-um-web-service"></a>SetPlayOnPhoneDialString-Vorgang (um-Webdienst)

Mit dem SetPlayOnPhoneDialString-Vorgang wird die Wählzeichenfolge festgelegt, die als Standard für den [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) und den [PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)verwendet werden soll.
  
## <a name="setplayonphonedialstring-request-example"></a>SetPlayOnPhoneDialString-Anforderungs Beispiel

### <a name="description"></a>Beschreibung

Das folgende Beispiel einer SetPlayOnPhoneDialString-Anforderung zeigt, wie Sie eine Anforderung zum Festlegen der standardmäßigen Wählzeichenfolge für ein Postfach bilden.
  
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

## <a name="successful-setplayonphonedialstring-response-example"></a>Erfolgreiches SetPlayOnPhoneDialString-Antwortbeispiel

### <a name="description"></a>Beschreibung

Im folgenden Beispiel einer SetPlayOnePhoneDialString-Antwort wird eine Antwort auf die SetPlayOnPhoneDialString-Anforderung angezeigt.
  
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



[SetPlayOnPhoneDialString (um-Webdienst)](setplayonphonedialstring-um-web-service.md)
  
[SetPlayOnPhoneDialStringResponse (um-Webdienst)](setplayonphonedialstringresponse-um-web-service.md)
  
[Wähl Dienst (um-Webdienst)](dialstring-um-web-service.md)

