---
title: Versetzt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: Das Offset-Element beschreibt den Offset aus der BaseOffset. Zusammen mit dem BaseOffset-Element identifiziert das Offset-Element an, ob die Zeit Standard- oder Sommerzeit.
ms.openlocfilehash: d85fef0d67633733f6aa1943d70413ea70a528d6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830642"
---
# <a name="offset"></a>Versetzt

Das **Offset** -Element beschreibt den Offset aus der [BaseOffset](baseoffset.md). Zusammen mit dem **BaseOffset** -Element identifiziert das **Offset** -Element an, ob die Zeit Standard- oder Sommerzeit. 
  
```xml
<Offset/>
```

 **duration**
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

Der Textwert stellt den Offset von der koordinierten Weltzeit (UTC).
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

