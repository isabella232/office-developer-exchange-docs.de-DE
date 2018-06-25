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
description: Das RelativeYearlyRecurrence-Element wird ein relativer jährliches Serienmuster beschrieben.
ms.openlocfilehash: ce8d2b134ce1fa34cbce8bd2fa921cab18d908a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831057"
---
# <a name="relativeyearlyrecurrence"></a>RelativeYearlyRecurrence

Das **RelativeYearlyRecurrence** -Element wird ein relativer jährliches Serienmuster beschrieben. 
  
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
|[DaysOfWeek (DayOfWeekType)](daysofweek-dayofweektype.md) <br/> |Beschreibt die Wochentage, die in Artikel Serienmuster verwendet werden.  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |Beschreibt die Woche im Monat in ein jährliches Serienmuster relative verwendet wird.  <br/> |
|[Month (Element Serie)](month-item-recurrence.md) <br/> |Beschreibt den Monat, wenn eine jährliche Terminserie erfolgt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Serieninformationen für wiederkehrende Aufgaben enthält.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.  <br/> |
|[Standard](standard.md) <br/> |Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.  <br/> |
|[Sommerzeit](daylight.md) <br/> |Das Datum und Zeitpunkt der Änderung die Zeit von Normalzeit auf Sommerzeit darstellt.  <br/> |
   
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

