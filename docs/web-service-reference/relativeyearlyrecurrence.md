---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: Das RelativeYearlyRecurrence-Element beschreibt ein relatives jährliches Serienmuster.
ms.openlocfilehash: 2abe09ddfe52c24211ef5d0a392ddecaf15bf7bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456729"
---
# <a name="relativeyearlyrecurrence"></a>RelativeYearlyRecurrence

Das **RelativeYearlyRecurrence** -Element beschreibt ein relatives jährliches Serienmuster. 
  
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
|[DaysOfWeek (dayofweektype)](daysofweek-dayofweektype.md) <br/> |Beschreibt die Wochentage, die in Element Serien Mustern verwendet werden.  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |Beschreibt, welche Woche in einem Monat in einem relativen jährlichen Serienmuster verwendet wird.  <br/> |
|[Month (Elementserie)](month-item-recurrence.md) <br/> |Beschreibt den Monat, in dem ein jährliches wiederkehrendes Element auftritt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Enthält Serieninformationen für wiederkehrende Vorgänge.  <br/> |
|[Serie (serietype)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> |
|[Standard](standard.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.  <br/> |
|[Sommer](daylight.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

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

