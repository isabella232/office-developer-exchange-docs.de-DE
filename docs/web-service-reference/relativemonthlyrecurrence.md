---
title: RelativeMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeMonthlyRecurrence
api_type:
- schema
ms.assetid: a76595db-7460-44ac-ac2a-53241caa33a7
description: Das RelativeMonthlyRecurrence-Element wird ein relativer monatliches Serienmuster beschrieben.
ms.openlocfilehash: 9b695052c38e2693946837bf99f03baea093df08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831053"
---
# <a name="relativemonthlyrecurrence"></a>RelativeMonthlyRecurrence

Das **RelativeMonthlyRecurrence** -Element wird ein relativer monatliches Serienmuster beschrieben. 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 **RelativeMonthlyRecurrencePatternType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Intervall](interval.md) <br/> |Definiert das Intervall zwischen zwei aufeinander folgenden monatliche Muster Terminserien. Der Bereich für diesen Wert ist 1 bis 99.  <br/> |
|[DaysOfWeek (DayOfWeekType)](daysofweek-dayofweektype.md) <br/> |Beschreibt, welche die Wochentage in das relative monatliches Serienmuster sind.  <br/> |
|[DayOfWeekIndex](dayofweekindex.md) <br/> |Beschreibt, welche Woche in ein monatliches Serienmuster relative verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.  <br/> |
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Serieninformationen für wiederkehrende Aufgaben enthält.  <br/> |
   
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

