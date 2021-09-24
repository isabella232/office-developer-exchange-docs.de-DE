---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: Das WeeklyRecurrence-Element beschreibt ein wöchentliches Serienmuster.
ms.openlocfilehash: 408116dd85fb31fce8f5f3b5b4cde92945783f5d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509336"
---
# <a name="weeklyrecurrence"></a>WeeklyRecurrence

Das **WeeklyRecurrence-Element** beschreibt ein wöchentliches Serienmuster. 
  
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
|[Intervall](interval.md) <br/> |Definiert das Intervall in Wochen zwischen zwei aufeinander folgenden wöchentlichen Serienmusterelementen. Der Wert kann im Bereich von 1 bis 99 liegen.  <br/> |
|[DaysOfWeek (DaysOfWeekType)](daysofweek-daysofweektype.md) <br/> |Beschreibt, welche Wochentage im wöchentlichen Serienmuster liegen.  <br/> |
|[FirstDayOfWeek](firstdayofweek.md) <br/> |Gibt den ersten Tag der Woche an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Enthält Serieninformationen für wiederkehrende Vorgänge.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Zeitzonenversatzinformationen gehen verloren, wenn das [Start-](start.md) und [Enddatum ](end-ex15websvcsotherref.md) des Serienmasterelements kein Datum aufweisen, das dem ersten Auftreten eines wöchentlichen Serienmusters entspricht. 
  
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

