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
description: Das Serienelement enthält Serieninformationen für wiederkehrende Vorgänge.
ms.openlocfilehash: 933fd6b003d8d193e1561f2a22b65ac00237c345
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528832"
---
# <a name="recurrence-taskrecurrencetype"></a>Serie (TaskRecurrenceType)

Das **Serien** Element enthält Serieninformationen für wiederkehrende Vorgänge. 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <MonthlyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRegeneration/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
       <DailyRegeneration/> 
       <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRegeneration/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
       <MonthlyRegeneration/> 
       <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <YearlyRegeneration/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
       <MonthlyRegeneration/> 
       <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
       <DailyRecurrence/> 
       <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRegeneration/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/>
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
|[RelativeYearlyRecurrence](relativeyearlyrecurrence.md) <br/> |Beschreibt ein relatives jährliches Serienmuster für eine wiederkehrende Aufgabe.  <br/> |
|[AbsoluteYearlyRecurrence](absoluteyearlyrecurrence.md) <br/> |Stellt ein jährliches Serienmuster für eine wiederkehrende Aufgabe dar.  <br/> |
|[RelativeMonthlyRecurrence](relativemonthlyrecurrence.md) <br/> |Beschreibt ein relatives monatliches Serienmuster für eine wiederkehrende Aufgabe.  <br/> |
|[AbsoluteMonthlyRecurrence](absolutemonthlyrecurrence.md) <br/> |Stellt ein monatliches Serienmuster für eine wiederkehrende Aufgabe dar.  <br/> |
|[WeeklyRecurrence](weeklyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Wochen und die Tage, an denen eine Aufgabe erneut auftritt.  <br/> |
|[DailyRecurrence](dailyrecurrence.md) <br/> |Beschreibt die Häufigkeit in Tagen, in der eine Aufgabe erneut auftritt.  <br/> |
|[DailyRegeneration](dailyregeneration.md) <br/> |Beschreibt, wie viele Tage nach Abschluss der aktuellen Aufgabe das nächste auftreten fällig wird.  <br/> |
|[WeeklyRegeneration](weeklyregeneration.md) <br/> |Beschreibt, wie viele Wochen nach Abschluss der aktuellen Aufgabe das nächste auftreten fällig wird.  <br/> |
|[MonthlyRegeneration](monthlyregeneration.md) <br/> |Beschreibt, wie viele Monate nach Abschluss der aktuellen Aufgabe das nächste auftreten fällig wird.  <br/> |
|[YearlyRegeneration](yearlyregeneration.md) <br/> |Beschreibt, wie viele Jahre nach Abschluss der aktuellen Aufgabe das nächste Vorkommen fällig wird.  <br/> |
|[NoEndRecurrence](noendrecurrence.md) <br/> |Beschreibt ein Serienmuster, das nicht über ein definiertes Enddatum verfügt.  <br/> Die Verwendung dieses Elements schließt die Verwendung der Elemente [EndDateRecurrence](enddaterecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) aus.  <br/> |
|[EndDateRecurrence](enddaterecurrence.md) <br/> |Beschreibt das Startdatum und das Enddatum eines Element Serienmusters.  <br/> Die Verwendung dieses Elements schließt die Verwendung der Elemente [NoEndRecurrence](noendrecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) aus.  <br/> [EndDateRecurrence](enddaterecurrence.md) kann nicht zusammen mit einem Regenerierungs Muster verwendet werden.  <br/> |
|[NumberedRecurrence](numberedrecurrence.md) <br/> |Beschreibt das Startdatum und die Anzahl der Vorkommen eines wiederkehrenden Elements.  <br/> Die Verwendung dieses Elements schließt die Verwendung der Elemente [NoEndRecurrence](noendrecurrence.md) und [EndDateRecurrence](enddaterecurrence.md) aus.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

