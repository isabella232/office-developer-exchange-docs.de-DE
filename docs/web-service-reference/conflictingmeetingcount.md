---
title: ConflictingMeetingCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetingCount
api_type:
- schema
ms.assetid: 11f4d93a-b514-4a27-8d19-f4f0a35a185e
description: Das ConflictingMeetingCount-Element stellt die Anzahl der Besprechungen dar, die mit dem Kalenderelement in Konflikt stehen.
ms.openlocfilehash: d53245e1b5d1f0182b28b15bf55ba9742bbb2a07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463860"
---
# <a name="conflictingmeetingcount"></a>ConflictingMeetingCount

Das **ConflictingMeetingCount** -Element stellt die Anzahl der Besprechungen dar, die mit dem Kalenderelement in Konflikt stehen. 
  
```xml
<ConflictingMeetingCount/>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt eine ganze Zahl dar. Diese Eigenschaft ist schreibgeschützt.
  
## <a name="remarks"></a>Bemerkungen

Ein Kalenderelement wird als widersprüchlich betrachtet, wenn es, zumindest teilweise, gleichzeitig mit einem anderen Kalenderelement in demselben Kalenderordner auftritt. Wenn sich ein Kalenderelement in einem nicht-Kalender-Ordner befindet, wird es mit Kalenderelementen im Standardkalenderordner verglichen. Besprechungsanfragen werden mit Kalenderelementen im Standardkalenderordner verglichen.
  
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

