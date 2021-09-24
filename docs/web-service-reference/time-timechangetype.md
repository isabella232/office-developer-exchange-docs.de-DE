---
title: Zeit (TimeChangeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Time
api_type:
- schema
ms.assetid: be12e41e-6871-4f6b-b2d4-3dfa404f9ea1
description: Das Time-Element beschreibt die Zeit, zu der sich die Zeit zwischen Standardzeit und Sommerzeit ändert.
ms.openlocfilehash: 0c669340778496958ef6dff082e48b5b7f6209b5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523307"
---
# <a name="time-timechangetype"></a>Zeit (TimeChangeType)

Das **Time-Element** beschreibt die Zeit, zu der sich die Zeit zwischen Standardzeit und Sommerzeit ändert. 
  
```xml
<Time/>
```

 **Time**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Daylight](daylight.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Sommerzeit in Standardzeit geändert wird.  <br/> |
|[Standard](standard.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Sommerzeit in Standardzeit geändert wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die Zeit dar, zu der sich die Zeit zwischen Standardzeit und Sommerzeit ändert.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

