---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: Das RecurringDayTransition-Element stellt einen Zeitzonenübergang dar, der jedes Jahr am gleichen Tag erfolgt.
ms.openlocfilehash: 44c2a6ec4dbaaa52a2772cb5c35a84b14dd77f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468467"
---
# <a name="recurringdaytransition"></a>RecurringDayTransition

Das **RecurringDayTransition** -Element stellt einen Zeitzonenübergang dar, der jedes Jahr am gleichen Tag erfolgt. 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 **RecurringDayTransitionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[To](to.md) <br/> |Gibt den [Zeitraum](period.md) oder die [Transitions](transitionsgroup.md) an, der das Ziel des Zeit Zonen Übergangs darstellt.  <br/> |
|[Offset](timeoffset.md) <br/> |Stellt den Offset für die Dauer der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitzonenübergang dar.  <br/> |
|[Month (Zeitzonenübergang)](month-time-zone-transition.md) <br/> |Stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.  <br/> |
|[DayOfWeek (Zeitzone)](dayofweek-timezone.md) <br/> |Stellt den Wochentag dar, an dem der Zeitzonenübergang erfolgt.  <br/> |
|[Vorkommen (Zeitzonenübergang)](occurrence-time-zone-transition.md) <br/> |Stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Übergänge](transitions.md) <br/> |Stellt eine Auflistung von Zeit Zonen Übergängen dar.  <br/> |
|[Transitiongroup](transitionsgroup.md) <br/> |Stellt eine Auflistung von Zeit Zonen Übergängen dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Ein Beispiel für einen Zeitzonenübergang, der durch das [RecurringDayTransition](recurringdaytransition.md) -Element dargestellt werden kann, ist ein Übergang, der jedes Jahr am zweiten Dienstag im Februar stattfindet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

