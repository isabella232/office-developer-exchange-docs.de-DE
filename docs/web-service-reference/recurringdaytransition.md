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
description: Das RecurringDayTransition-Element stellt einen Zeitzone Übergang, der am gleichen Tag pro Jahr auftritt, dar.
ms.openlocfilehash: 913345188547ce9903809fdc1cbbbe3e20ae7f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831012"
---
# <a name="recurringdaytransition"></a>RecurringDayTransition

Das **RecurringDayTransition** -Element stellt einen Zeitzone Übergang, der am gleichen Tag pro Jahr auftritt, dar. 
  
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
|[To](to.md) <br/> |Gibt den [Zeitraum](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.  <br/> |
|[TimeOffset](timeoffset.md) <br/> |Stellt den Offset für die Dauer von koordinierte Weltzeit (UTC) für den Übergang zur Zeitzone dar.  <br/> |
|[Monat (Übergang Zeitzone)](month-time-zone-transition.md) <br/> |Stellt den Monat, in dem der Übergang zur Zeitzone auftritt.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Stellt den Tag der Woche auf der erfolgt der Übergang zur Zeitzone.  <br/> |
|[Vorkommen (Übergang Zeitzone)](occurrence-time-zone-transition.md) <br/> |Stellt das Vorkommen des Tags der Woche des Monats, der der Übergang zur Zeitzone auftritt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Übergänge](transitions.md) <br/> |Stellt eine Auflistung der Zeitzone Übergänge.  <br/> |
|[TransitionsGroup](transitionsgroup.md) <br/> |Stellt eine Auflistung der Zeitzone Übergänge.  <br/> |
   
## <a name="remarks"></a>Hinweise

Einen Übergang, der am zweiten Dienstag Februar jährlich auftritt, ist ein Beispiel für einen Übergang Zeitzone, der durch das [RecurringDayTransition](recurringdaytransition.md) -Element dargestellt werden könnte. 
  
Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

