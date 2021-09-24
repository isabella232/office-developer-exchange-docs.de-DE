---
title: Wert (Nachrichtenverfolgung)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Value
api_type:
- schema
ms.assetid: cb2f228f-775a-4c7d-82e7-41c7c953c808
description: Das Value-Element stellt den Eigenschaftswert für einen Nachrichtenverfolgungsbericht dar.
ms.openlocfilehash: c8aa4f3cc41e76b633ee1b244371de2f5410c944
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513962"
---
# <a name="value-message-tracking"></a>Wert (Nachrichtenverfolgung)

Das **Value-Element** stellt den Eigenschaftswert für einen Nachrichtenverfolgungsbericht dar. 
  
```xml
<Value/>
```

**String**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TrackingPropertyType](trackingpropertytype.md) <br/> |Stellt ein Name-Wert-Zeichenfolgenpaar dar, das zum Erstellen von Eigenschaften für Nachrichtenverfolgungsberichte verwendet wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert ist optional.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element kann höchstens einmal im [TrackingPropertyType-Element](trackingpropertytype.md) auftreten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

