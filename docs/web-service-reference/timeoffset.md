---
title: TimeOffset
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeOffset
api_type:
- schema
ms.assetid: b70bf498-cc3a-4fa6-8236-514acb973b33
description: The TimeOffset element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition.
ms.openlocfilehash: ac2da7d6ab1d59d075111390513b1a3dd58a892e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522544"
---
# <a name="timeoffset"></a>TimeOffset

The **TimeOffset** element represents the time offset from Coordinated Universal Time (UTC) for the time zone transition. 
  
```XML
<TimeOffset/>
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
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum stattfindet.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr am selben Tag erfolgt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **TimeOffset-Elements** ist eine Dauer, die den Zeitoffset von UTC für den Zeitzonenübergang angibt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

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

