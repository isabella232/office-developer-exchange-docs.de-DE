---
title: Serie (TaskRecurrenceType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: Recurrence-Element enthält Serieninformationen für wiederkehrende Aufgaben.
ms.openlocfilehash: ae2bb35e89a0a50c7ca67cb0e580427150afb99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831006"
---
# <a name="recurrence-taskrecurrencetype"></a>Serie (TaskRecurrenceType)

**Recurrence** -Element enthält Serieninformationen für wiederkehrende Aufgaben. 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 **TaskRecurrenceType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Ein relative jährliches Serienmuster für einen sich wiederholenden Vorgang beschreibt.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Stellt ein jährliches Serienmuster für einen sich wiederholenden Vorgang dar.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Ein relative monatliches Serienmuster für einen sich wiederholenden Vorgang beschreibt.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Stellt ein monatliches Serienmuster für einen sich wiederholenden Vorgang dar.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Wochen und die Tage, an denen eine Aufgabe wiederholt ausgeführt.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Tagen, in denen eine Aufgabe wiederholt ausgeführt.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Beschreibt, wie viele Tage nach dem Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Beschreibt, wie viele Wochen nach Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Beschreibt, wie viele Monate nach Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Beschreibt, wie viele Jahre nach Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Beschreibt ein Serienmuster, die nicht über einen definierten Enddatum verfügt.  <br/> Die Verwendung dieses Elements schließt die Verwendung der [EndDateRecurrence](enddaterecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.  <br/> Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.  <br/> [EndDateRecurrence](enddaterecurrence.md) kann nicht zusammen mit einem Muster mithilfe verwendet werden.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Beschreibt das Startdatum und die Anzahl der Vorkommen eines sich wiederholenden-Elements.  <br/> Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [EndDateRecurrence](enddaterecurrence.md) Elemente.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

