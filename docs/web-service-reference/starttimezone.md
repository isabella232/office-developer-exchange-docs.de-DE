---
title: StartTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StartTimeZone
api_type:
- schema
ms.assetid: d38c4dc1-4ecb-42a1-8d57-a451b16a2de2
description: Das StartTimeZone-Element definiert die Zeitzone für die Startzeit eines CalendarItem- oder MeetingRequest-Elements.
ms.openlocfilehash: 720e8b98f1ff4081f8971074bbb9323cdfb3e816
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545860"
---
# <a name="starttimezone"></a>StartTimeZone

Das **StartTimeZone-Element** definiert die Zeitzone für die Startzeit eines [CalendarItem-](calendaritem.md) oder [MeetingRequest-Elements.](meetingrequest.md)
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

**TimeZoneDefinitionType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Stellt den eindeutigen Bezeichner der Zeitzonendefinition dar.  <br/> |
|Name  <br/> |Stellt den beschreibenden Namen der Zeitzonendefinition dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zeiten](periods.md) <br/> |Stellt ein Array von [Period-Elementen](period.md) dar, die den Zeitversatz in verschiedenen Phasen der Zeitzone definieren.  <br/> |
|[TransitionsGroups](transitionsgroups.md) <br/> |Stellt ein Array von [TransitionsGroup-Elementen](transitionsgroup.md) dar, die Zeitzonenübergänge angeben.  <br/> |
|[Übergänge](transitions.md) <br/> |Stellt ein Array von Zeitzonenübergängen dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

