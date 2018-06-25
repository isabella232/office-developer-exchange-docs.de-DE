---
title: Übergänge
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transitions
api_type:
- schema
ms.assetid: 26f38f1c-96a3-440e-805c-1437886d11c5
description: Übergänge-Element stellt ein Array von Zeitzone Übergänge.
ms.openlocfilehash: df7cacdef71c3fdfaa3ecadb486843ea30e6109d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839259"
---
# <a name="transitions"></a>Übergänge

**Übergänge** -Element stellt ein Array von Zeitzone Übergänge. 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 **ArrayOfTransitionsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Den eindeutigen Bezeichner der Zeitzonendefinition darstellt.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzone Übergang, der auftritt, an einem angegebenen Tag des Jahres dar.  <br/> |
|[Übergang](transition.md) <br/> |Stellt einen Zeitzone Übergang dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTimeZone-Zeitzone](starttimezone.md) <br/> |Definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).  <br/> |
|[Zeitzonendefinition](timezonedefinition.md) <br/> |Definiert eine Zeitzone.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

