---
title: Beginn
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: Das Start-Element stellt den Anfang des eine Dauer dar.
ms.openlocfilehash: 8d013990e650b497abfa947938a69eed3fed7474
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831545"
---
# <a name="start"></a>Beginn

Das Element **Starten** stellt den Anfang des eine Dauer dar. 
  
```xml
<Start/>
```

**DateTime**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[DeletedOccurrence](deletedoccurrence.md) <br/> |Stellt eine gelöschte Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[Vorkommen](occurrence.md) <br/> |Stellt ein einzelnes geändertes Vorkommen des ein wiederkehrendes Kalenderelement.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Anfang des eine Dauer dar.
  
## <a name="remarks"></a>Hinweise

UpdateItem-Vorgang kann die Zeit [Start](start.md) und [End](end-ex15websvcsotherref.md) eines Exchange-Speicher-Elements festgelegt. In einer Anforderung UpdateItem kann **die Startzeit** festgelegt werden, ohne auch **die Endzeit** festzulegen. Dies kann einen Fehler verursachen, wenn **die Startzeit** **die Endzeit** liegt. Beachten Sie, dass Clientanwendungen Anpassungen **Endzeit** ausführen müssen, wenn **diese Startzeit** geändert wird, um die Dauer beibehalten. 
  
> [!NOTE]
> Die Zeitzone Offset Informationen geht verloren, wenn die [ [Starten](start.md) und](end-ex15websvcsotherref.md) Enddatum des wiederkehrenden master-Objekts nicht über ein Datum verfügen, das das erste Auftreten des ein wöchentliches Serienmuster gleich ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [WeeklyRecurrence](weeklyrecurrence.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

