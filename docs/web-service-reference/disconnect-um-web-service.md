---
title: Trennen (um-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- Disconnect
api_type:
- schema
ms.assetid: 2f8c1e8c-3bd4-4988-96b9-735c347b29f7
description: Das Disconnect-Element definiert eine Anforderung zum Trennen eines Anrufs.
ms.openlocfilehash: a00d957927a7a97d12c0d8c0c662956a18529cde
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458453"
---
# <a name="disconnect-um-web-service"></a>Trennen (um-Webdienst)

Das **Disconnect** -Element definiert eine Anforderung zum Trennen eines Anrufs. 
  
- [Trennen (um-Webdienst)](disconnect-um-web-service.md)
  
```xml
<Disconnect>
  <CallId>   </CallId>
</Disconnect>
```

 **complexType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anrufdienst (um-Webdienst)](callid-um-web-service.md) <br/> |Der Bezeichner des Anrufs, der getrennt werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Trennungsvorgang (um-Webdienst)](disconnect-operation-um-web-service.md)  
- [PlayOnPhone-Vorgang (um-Webdienst)](playonphone-operation-um-web-service.md) 
- [PlayOnPhoneGreeting-Vorgang (um-Webdienst)](playonphonegreeting-operation-um-web-service.md)  
- [Anrufdienst (um-Webdienst)](callid-um-web-service.md)

