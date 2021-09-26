---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: Das DayOrder-Element stellt das n-te Vorkommen des im DayOfWeek (TimeZone)-Element angegebenen Tages dar, das das Datum des Übergangs von und zu Standardzeit und Sommerzeit darstellt.
ms.openlocfilehash: bc216984a92fef58ac6f46dc4646a0deca837563
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543443"
---
# <a name="dayorder"></a>DayOrder

Das **DayOrder-Element** stellt das _n_th Vorkommen des im [DayOfWeek (TimeZone)-Element](dayofweek-timezone.md) angegebenen Tags dar, der das Datum des Übergangs von und zu Standardzeit und Sommerzeit darstellt. 
  
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
|[StandardTime](standardtime.md) <br/> | Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (COORDINATED Universal Time, UTC) dar, die durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird.<br/><br/>Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird.<br/><br/>Es folgen die XPath-Ausdrücke für das [StandardTime-Element:](standardtime.md)<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias -Element (UTC)](bias-utc.md) in Regionen, in denen Sommerzeit beobachtet wird.<br/><br/>Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt.<br/><br/>Es folgen die XPath-Ausdrücke für das [DaylightTime-Element:](daylighttime.md)<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert für das **DayOrder-Element** kann 1 bis 5 sein. Der Maximalwert für dieses Element kann je nach Monat und Jahr entweder 4 oder 5 sein. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein [StandardTime-Element,](standardtime.md) das ein **DayOrder-Element** mit dem Wert 5, ein [Month-Element](month.md) mit dem Wert 10 und ein [DayOfWeek (TimeZone)-Element](dayofweek-timezone.md) mit dem Wert Sonntag enthält, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

