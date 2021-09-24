---
title: Offset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Offset
api_type:
- schema
ms.assetid: dcbb9d85-d90c-4363-b4c9-d081ad03f407
description: Das Offset-Element beschreibt den Offset von BaseOffset. Zusammen mit dem BaseOffset-Element gibt das Offset-Element an, ob die Zeit Standard- oder Sommerzeit ist.
ms.openlocfilehash: af9a2f7a94ae0cd736a4fe6f11b8a5a77673bbe3
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515390"
---
# <a name="offset"></a>Offset

Das **Offset-Element** beschreibt den Offset von [BaseOffset](baseoffset.md). Zusammen mit dem **BaseOffset-Element** gibt das **Offset-Element** an, ob die Zeit Standard- oder Sommerzeit ist. 
  
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
|[Daylight](daylight.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Sommerzeit in Standardzeit geändert wird.  <br/> |
|[Standard](standard.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Sommerzeit in Standardzeit geändert wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Offset der koordinierten Weltzeit (COORDINATED Universal Time, UTC) dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

