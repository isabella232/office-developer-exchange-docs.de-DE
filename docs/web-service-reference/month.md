---
title: Monat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
description: The Month element represents the transition month of the year to and from standard time and daylight saving time.
ms.openlocfilehash: aca81faf2767e17dab956db9a208245fbd0b7d83
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520430"
---
# <a name="month"></a>Monat

The **Month** element represents the transition month of the year to and from standard time and daylight saving time. 
  
```xml
<Month>...</Month>
```

 **Kurz**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (COORDINATED Universal Time, UTC) dar, die durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird. Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird. <br/> <br/>  Es folgen die XPath-Ausdrücke für das [StandardTime-Element:](standardtime.md) <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias -Element (UTC)](bias-utc.md) in Regionen, in denen Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt.  <br/><br/>  Es folgen die XPath-Ausdrücke für das [DaylightTime-Element:](daylighttime.md)  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert stellt die Ordnungsrangfolge des Monats nach Vorkommen dar und muss eine Zahl zwischen 1 und 12 sein. Dies ist ein kurzer ganzzahliger Datentyp.
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein [StandardTime-Element,](standardtime.md) das ein [DayOrder-Element](dayorder.md) mit dem Wert 5, ein **Month-Element** mit dem Wert 10 und ein [DayOfWeek (TimeZone)-Element](dayofweek-timezone.md) mit dem Wert Sonntag enthält, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt. 
  
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

