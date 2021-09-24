---
title: Start
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Start
api_type:
- schema
ms.assetid: 7cfe9979-c893-4f9b-b3a1-8f9e17515a4b
description: Das Start-Element stellt den Anfang einer Dauer dar.
ms.openlocfilehash: 7342e285e57a165ec4a9ba0b8551bfbe045d3b9c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521270"
---
# <a name="start"></a>Start

Das **Start-Element** stellt den Anfang einer Dauer dar. 
  
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
|[DeletedOccurrence](deletedoccurrence.md) <br/> |Stellt ein gelöschtes Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[Vorkommen](occurrence.md) <br/> |Stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Anfang einer Dauer dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der UpdateItem-Vorgang kann die [Start-](start.md) und [Endzeit ](end-ex15websvcsotherref.md) eines Exchange-Speicherelements festlegen. In einer UpdateItem-Anforderung kann die **Startzeit** festgelegt werden, ohne auch die **Endzeit** festzulegen. Dies kann einen Fehler verursachen, wenn die **Startzeit** später als die **Endzeit** ist. Beachten Sie, dass Clientanwendungen Anpassungen an der **Endzeit** vornehmen müssen, wenn diese **Startzeit** geändert wird, um die Dauer beizubehalten. 
  
> [!NOTE]
> Die Zeitzonenversatzinformationen gehen verloren, wenn das [Start-](start.md) und [Enddatum ](end-ex15websvcsotherref.md) des Serienmasterelements kein Datum aufweisen, das dem ersten Auftreten eines wöchentlichen Serienmusters entspricht. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [WeeklyRecurrence](weeklyrecurrence.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

