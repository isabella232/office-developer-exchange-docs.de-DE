---
title: DayOfWeek (TimeZone)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: Das DayOfWeek-Element stellt den Wochentag dar, an dem der Zeitzonenübergang stattfindet.
ms.openlocfilehash: 5b51a3692a1836d2d2448df88b0ec07ccf1d79a5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519898"
---
# <a name="dayofweek-timezone"></a>DayOfWeek (TimeZone)

Das **DayOfWeek-Element** stellt den Wochentag dar, an dem der Zeitzonenübergang stattfindet. 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

**DayOfWeekType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (COORDINATED Universal Time, UTC) dar, die durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird.<br/><br/>Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias -Element (UTC)](bias-utc.md) in Regionen, in denen Sommerzeit beobachtet wird.<br/><br/>Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[RecurringDayTransition](recurringdaytransition.md) <br/> |Stellt einen Zeitzonenübergang dar, der jedes Jahr am selben Tag erfolgt.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert wird durch eine Aufzählung dargestellt, die die folgenden möglichen Werte aufweist:
  
- Sonntag    
- Montag    
- Dienstag    
- Mittwoch    
- Donnerstag    
- Freitag    
- Samstag    
- Tag    
- Wochentag   
- WeekendDay
    
## <a name="remarks"></a>HinwBemerkungeneise

Ein [StandardTime-Element,](standardtime.md) das ein [DayOrder-Element](dayorder.md) mit dem Wert 5, ein [Month-Element](month.md) mit dem Wert 10 und ein **DayOfWeek-Element** mit dem Wert Sonntag enthält, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
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

