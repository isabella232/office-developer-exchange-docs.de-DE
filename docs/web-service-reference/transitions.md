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
description: Das Transitions-Element stellt ein Array von Zeit Zonen Übergängen dar.
ms.openlocfilehash: d48fb8872b2f7e052f733c32e5dd1c9b4d04d898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467438"
---
# <a name="transitions"></a>Übergänge

Das **Transitions** -Element stellt ein Array von Zeit Zonen Übergängen dar. 
  
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
|Id  <br/> |Stellt den eindeutigen Bezeichner der Zeitzonendefinition dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AbsoluteDateTransition](absolutedatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.  <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.  <br/> |
|[RecurringDateTransition](recurringdatetransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der an einem angegebenen Tag des Jahres erfolgt.  <br/> |
|[Übergang](transition.md) <br/> |Stellt einen Zeitzonenübergang dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |Definiert die Zeitzone für die Startzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Start Zeit.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Definiert die Zeitzone für die Endzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Datei.  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Definiert eine Zeitzone.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

