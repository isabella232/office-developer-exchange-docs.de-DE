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
description: Das Time-Element stellt die Übergangszeit von Tag zu und von Standardzeit und Sommerzeit dar.
ms.openlocfilehash: 97c89fbcbdb85fcdd4d32a1d44075ac42adef053
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460295"
---
# <a name="time"></a>Time

Das **time** -Element stellt die Übergangszeit von Tag zu und von Standardzeit und Sommerzeit dar. 
  
```xml
<Time>...</Time>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Standard Time](standardtime.md) <br/> | Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, dargestellt durch das Element [Bias (UTC)](bias-utc.md) . Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.  <br/><br/>  Im folgenden finden Sie die XPath-Ausdrücke für das [Standard](standardtime.md) Time-Element: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.  <br/><br/>  Im folgenden finden Sie die XPath-Ausdrücke für das [Daylight](daylighttime.md) -Element:  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt Stunden, Minuten und Sekunden im folgenden Format dar: hh: mm: SS.
  
## <a name="remarks"></a>Bemerkungen

Wenn das **time** -Element im [Sommer](daylighttime.md) Zeitelement auftritt, stellt dies die Tageszeit dar, zu der der Übergang von Sommerzeit zu Standardzeit erfolgt. Wenn das [time](time.md) -Element im [Standard](standardtime.md) Time-Element auftritt, stellt dies die Tageszeit dar, zu der der Übergang von Standardzeit zu Sommerzeit erfolgt. 
  
Dieses Element hat ein Mindestvorkommen von 0 (null) und ein Maximum des Auftretens von 1.
  
## <a name="example"></a>Beispiel

Der folgende Teil einer Anforderung stellt eine Übergangszeit von 2 Uhr dar. von Standardzeit zu Sommerzeit.
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

