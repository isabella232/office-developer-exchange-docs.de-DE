---
title: Zeit
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: Time-Element stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone.
ms.openlocfilehash: 716487fb7ed64dbaa6fa97caf1ea608e4673d2ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839188"
---
# <a name="time"></a>Zeit

**Time** -Element stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone. 
  
```xml
<Time>...</Time>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC) dargestellt durch das Element [Bias (UTC)](bias-utc.md) . Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.  <br/><br/>  Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.  <br/><br/>  Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert darstellt, Stunden, Minuten und Sekunden im folgenden Format: hh: mm:.
  
## <a name="remarks"></a>Hinweise

**Time** -Element im [DaylightTime](daylighttime.md) -Element auftritt, stellt die Tageszeit des Übergangs von Sommerzeit auf Normalzeit dar. [Time](time.md) -Element im [StandardTime](standardtime.md) -Element auftritt, stellt die Tageszeit des Übergangs von der Standardzeit zur Sommerzeit dar. 
  
Dieses Element hat eine minimale Vorkommen von 0 (null) und eine maximale Vorkommen eines.
  
## <a name="example"></a>Beispiel

Der folgende Teil einer Anforderung stellt eine Übergangszeit 2 Uhr von der Standardzeit zur Sommerzeit.
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

