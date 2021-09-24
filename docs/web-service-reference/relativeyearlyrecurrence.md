---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: Das RelativeYearlyRecurrence-Element beschreibt ein relatives jährliches Serienmuster.
ms.openlocfilehash: ce6d724735cb23fb08bf541123341ede35011c4c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512499"
---
# <a name="relativeyearlyrecurrence"></a>RelativeYearlyRecurrence

Das **RelativeYearlyRecurrence-Element** beschreibt ein relatives jährliches Serienmuster. 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 **RelativeYearlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[DaysOfWeek (DayOfWeekType)](daysofweek-dayofweektype.md) <br/> |Beschreibt die Wochentage, die in Elementserienmustern verwendet werden.  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |Beschreibt, welche Woche in einem Monat in einem relativen jahresweisen Serienmuster verwendet wird.  <br/> |
|[Monat (Elementserie)](month-item-recurrence.md) <br/> |Beschreibt den Monat, in dem ein jährlich wiederkehrendes Element auftritt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Enthält Serieninformationen für wiederkehrende Vorgänge.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> |
|[Standard](standard.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Sommerzeit in Standardzeit geändert wird.  <br/> |
|[Daylight](daylight.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.  <br/> |
   
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

