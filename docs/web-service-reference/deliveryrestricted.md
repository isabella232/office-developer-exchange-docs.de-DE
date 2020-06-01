---
title: DeliveryRestricted
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeliveryRestricted
api_type:
- schema
ms.assetid: 05989915-121c-4f26-93cc-af8d454ab442
description: Das DeliveryRestricted-Element gibt an, ob zustellungseinschränkungen verhindern, dass die Nachricht des Absenders den Empfänger erreichen kann.
ms.openlocfilehash: 58fc85873326179d7745db4ba7d4854a76ced6a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462689"
---
# <a name="deliveryrestricted"></a>DeliveryRestricted

Das **DeliveryRestricted** -Element gibt an, ob zustellungseinschränkungen verhindern, dass die Nachricht des Absenders den Empfänger erreichen kann. 
  
```XML
<DeliveryRestricted>true | false</DeliveryRestricted>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[E-Mail-Info](mailtips.md) <br/> |Stellt Werte für verschiedene Arten von e-Mail-Tipps dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert dieses Elements ist **true** , wenn zustellungseinschränkungen verhindert werden, dass die Nachricht des Absenders den Empfänger erreicht. Der Wert ist **false** , wenn zustellungseinschränkungen nicht verhindern, dass die Nachricht des Absenders den Empfänger erreichen kann. 
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

