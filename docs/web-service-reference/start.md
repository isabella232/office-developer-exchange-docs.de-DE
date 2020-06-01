---
title: Start
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
description: Das Start-Element stellt den Anfang einer Dauer dar.
ms.openlocfilehash: 0daf9c1422f7ba3894f9785aacac58263c5e721e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457214"
---
# <a name="start"></a>Start

Das **Start** -Element stellt den Anfang einer Dauer dar. 
  
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
  
## <a name="remarks"></a>Bemerkungen

Mit dem UpdateItem-Vorgang können die [Start](start.md) -und [Endzeit](end-ex15websvcsotherref.md) eines Exchange-Informationsspeicher Elements festgelegt werden. In einer UpdateItem-Anforderung kann die **Startzeit** festgelegt werden, ohne auch die **Endzeit** festzulegen. Dies kann zu einem Fehler führen, wenn die **Startzeit** später als die **Endzeit** ist. Beachten Sie, dass Clientanwendungen Anpassungen an **Endzeit** vornehmen müssen, wenn die **Startzeit** geändert wird, um die Dauer beizubehalten. 
  
> [!NOTE]
> Die Zeitzonenoffset Informationen gehen verloren, wenn das [anfangs](start.md) -und Enddatum des [wiederkehrenden Haupt](end-ex15websvcsotherref.md) Elements kein Datum aufweist, das dem ersten Vorkommen eines wöchentlichen Serienmusters entspricht. 
  
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

