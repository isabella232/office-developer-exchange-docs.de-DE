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
description: Das DayOrder-Element darstellt, das n-te Vorkommen des Tages im DayOfWeek (TimeZone)-Element, das das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt.
ms.openlocfilehash: 03ee678611a6cf58a7256ded67ab4d0a8a06a7ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757882"
---
# <a name="dayorder"></a>DayOrder

Das **DayOrder** -Element darstellt, das _n_th Vorkommen des Tages im [DayOfWeek (TimeZone)](dayofweek-timezone.md) -Element, das das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt. 
  
```xml
<DayOrder>...</DayOrder>
```

**kurze**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC) dargestellt durch das Element [Bias (UTC)](bias-utc.md) .<br/><br/>Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.<br/><br/>Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.<br/><br/>Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.<br/><br/>Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert für das **DayOrder** -Element kann 1 bis 5 entsprechen. Der maximale Wert für dieses Element kann 4 oder 5, je nach Monat und Jahr sein. 
  
## <a name="remarks"></a>Hinweise

Ein [StandardTime](standardtime.md) -Element, enthält ein **DayOrder** -Element, das den Wert 5 hat, ein [Month](month.md) -Element, das einen Wert von 10 aufweist und ein [DayOfWeek (TimeZone)](dayofweek-timezone.md) -Element, das den Wert Sonntag hat, bedeutet, dass den Übergang vom Standardzeit Sommerzeit tritt am fünften Sonntag der zehnte Monat. 
  
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

