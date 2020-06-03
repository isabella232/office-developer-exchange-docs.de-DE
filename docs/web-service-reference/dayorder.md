---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: Das DayOrder-Element stellt das n-te Vorkommen des im DayOfWeek-Element (TimeZone) angegebenen Tags dar, das das Datum des Übergangs von und zur Standardzeit und zur Sommerzeit darstellt.
ms.openlocfilehash: 53a8cb979bdb7aefead5623b4680f4c1a4ef5509
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526963"
---
# <a name="dayorder"></a>DayOrder

Das **DayOrder** -Element stellt das _n_th Vorkommen des Tags dar, der im [DayOfWeek-Element (TimeZone)](dayofweek-timezone.md) angegeben ist, das das Datum des Übergangs von und zur Standardzeit und zur Sommerzeit darstellt. 
  
```xml
<DayOrder>...</DayOrder>
```

**kurz**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Standard Time](standardtime.md) <br/> | Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .<br/><br/>Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.<br/><br/>Im folgenden finden Sie die XPath-Ausdrücke für das [Standard](standardtime.md) Time-Element:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird.<br/><br/>Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.<br/><br/>Im folgenden finden Sie die XPath-Ausdrücke für das [Daylight](daylighttime.md) -Element:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert für das **DayOrder** -Element kann 1 bis 5 sein. Der maximale Wert für dieses Element kann entweder 4 oder 5 sein, je nach Monat und Jahr. 
  
## <a name="remarks"></a>Bemerkungen

Ein [Standard](standardtime.md) Time-Element, das ein **DayOrder** -Element mit dem Wert 5, einem [Month](month.md) -Element mit dem Wert 10 und einem DayOfWeek-Element [(TimeZone)](dayofweek-timezone.md) enthält, das den Wert "Sunday" aufweist, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt. 
  
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

