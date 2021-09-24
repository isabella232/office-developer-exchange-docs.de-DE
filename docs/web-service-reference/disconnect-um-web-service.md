---
title: Disconnect (UM-Webdienst)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- Disconnect
api_type:
- schema
ms.assetid: 2f8c1e8c-3bd4-4988-96b9-735c347b29f7
description: Das Disconnect-Element definiert eine Anforderung zum Trennen eines Anrufs.
ms.openlocfilehash: 6aaff910d85a963a926e7c2a74a91963b120392c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538373"
---
# <a name="disconnect-um-web-service"></a>Disconnect (UM-Webdienst)

Das **Disconnect-Element** definiert eine Anforderung zum Trennen eines Anrufs. 
  
- [Disconnect (UM-Webdienst)](disconnect-um-web-service.md)
  
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
|[CallId (UM-Webdienst)](callid-um-web-service.md) <br/> |Der Bezeichner des Anrufs, der getrennt werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Disconnect-Vorgange (UM-Webdienst)](disconnect-operation-um-web-service.md)  
- [PlayOnPhone-Vorgang (UM-Webdienst)](playonphone-operation-um-web-service.md) 
- [PlayOnPhoneGreeting-Vorgang (UM-Webdienst)](playonphonegreeting-operation-um-web-service.md)  
- [CallId (UM-Webdienst)](callid-um-web-service.md)

