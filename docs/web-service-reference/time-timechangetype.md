---
title: Zeit (TimeChangeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: be12e41e-6871-4f6b-b2d4-3dfa404f9ea1
description: Time-Element wird beschrieben, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird.
ms.openlocfilehash: db44ef494561b75dc55c93229cec3901f04235ad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839181"
---
# <a name="time-timechangetype"></a>Zeit (TimeChangeType)

**Time** -Element wird beschrieben, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird. 
  
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
|[Sommerzeit](daylight.md) <br/> |Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.  <br/> |
|[Standard](standard.md) <br/> |Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert darstellt, wenn die Zeit zwischen Standardzeit und Sommerzeit geändert wird.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

