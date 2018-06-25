---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: Das WeeklyRecurrence-Element wird ein wöchentliches Serienmuster beschrieben.
ms.openlocfilehash: 78bc76dd63c6737786df02f336217dc8de9a3a67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839529"
---
# <a name="weeklyrecurrence"></a>WeeklyRecurrence

Das **WeeklyRecurrence** -Element wird ein wöchentliches Serienmuster beschrieben. 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 **WeeklyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Intervall](interval.md) <br/> |Definiert das Intervall in Wochen zwischen zwei aufeinander folgende wöchentliche Serie Muster Elemente. Der Wert kann im Bereich von 1 bis 99 sein.  <br/> |
|[DaysOfWeek (DaysOfWeekType)](daysofweek-daysofweektype.md) <br/> |Beschreibt, welche die Wochentage in wöchentliches Serienmuster sind.  <br/> |
|[FirstDayOfWeek](firstdayofweek.md) <br/> |Gibt den ersten Tag der Woche.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Serieninformationen für wiederkehrende Aufgaben enthält.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Die Zeitzone Offset Informationen geht verloren, wenn die [ [Starten](start.md) und](end-ex15websvcsotherref.md) Enddatum des wiederkehrenden master-Objekts nicht über ein Datum verfügen, das das erste Auftreten des ein wöchentliches Serienmuster gleich ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

