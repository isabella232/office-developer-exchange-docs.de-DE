---
title: Serie (RecurrenceType)
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
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: Recurrence-Element enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.
ms.openlocfilehash: f26ccf5912848a6d7fbbfa7d0a19d41635c896e0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831004"
---
# <a name="recurrence-recurrencetype"></a>Serie (RecurrenceType)

**Recurrence** -Element enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen. 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 **RecurrenceType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Wird ein relativer jährliches Serienmuster beschrieben.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Stellt ein jährliches Serienmuster dar.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Beschreibt ein relative monatliches Serienmuster wiederkehrende Kalenderelemente.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Stellt ein monatliches Serienmuster dar.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Wochen und die Tage, die ein Kalenderelement oder eine Aufgabe wiederholt.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Tagen, in dem ein Kalenderelement oder eine Aufgabe wiederholt.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Beschreibt ein Serienmuster, die nicht über einen definierten Enddatum verfügt.  <br/> Die Verwendung dieses Elements schließt die Verwendung der [EndDateRecurrence](enddaterecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.  <br/> Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Beschreibt das Startdatum und die Anzahl der Vorkommen eines sich wiederholenden-Elements.  <br/> Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [EndDateRecurrence](enddaterecurrence.md) Elemente.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanfrage im Exchange-Speicher  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat. 
  
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

