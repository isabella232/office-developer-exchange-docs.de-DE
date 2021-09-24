---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: Das RecurringDateTransition-Element stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum erfolgt.
ms.openlocfilehash: 864f3f539c5440fbfc539ca6c2042b3d9edca267
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529363"
---
# <a name="recurringdatetransition"></a>RecurringDateTransition

Das **RecurringDateTransition-Element** stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum erfolgt. 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 **RecurringDateTransitionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[To](to.md) <br/> |Gibt den [Zeitraum](period.md) oder die [TransitionsGroup](transitionsgroup.md) an, die das Ziel des Zeitzonenübergangs ist.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Stellt den Zeitoffset der koordinierten Weltzeit (COORDINATED Universal Time, UTC) für den Zeitzonenübergang dar.  <br/> |
|[Monat (Zeitzonenübergang)](month-time-zone-transition.md) <br/> |Stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.  <br/> |
|[Day](day.md) <br/> |Stellt den Tag des Monats dar, an dem der Zeitzonenübergang erfolgt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Übergänge](transitions.md) <br/> |Stellt eine Auflistung von Zeitzonenübergängen dar.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Stellt eine Auflistung von Zeitzonenübergängen dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Beispiel für einen Zeitzonenübergang, der durch das [RecurringDateTransition-Element](recurringdatetransition.md) dargestellt werden könnte, ist ein Übergang, der jedes Jahr am 15. März stattfindet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

