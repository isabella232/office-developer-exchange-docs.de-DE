---
title: Zeit
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: Das Time-Element stellt die Übergangszeit des Tages zu und von Standardzeit und Sommerzeit dar.
ms.openlocfilehash: d9cd83a7dcb0a296693e3daa1874b12294de5857
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513269"
---
# <a name="time"></a>Zeit

Das **Time-Element** stellt die Übergangszeit des Tages zu und von Standardzeit und Sommerzeit dar. 
  
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
|[StandardTime](standardtime.md) <br/> | Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (COORDINATED Universal Time, UTC) dar, die durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird. Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird.  <br/><br/>  Es folgen die XPath-Ausdrücke für das [StandardTime-Element:](standardtime.md) <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias -Element (UTC)](bias-utc.md) in Regionen, in denen Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt.  <br/><br/>  Es folgen die XPath-Ausdrücke für das [DaylightTime-Element:](daylighttime.md)  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt Stunden, Minuten und Sekunden im folgenden Format dar: hh:mm:ss.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das **Time-Element** im [DaylightTime-Element](daylighttime.md) auftritt, stellt es die Tageszeit dar, zu der der Übergang von Sommerzeit zu Standardzeit erfolgt. Wenn das [Time-Element](time.md) im [StandardTime-Element](standardtime.md) auftritt, stellt es die Tageszeit dar, zu der der Übergang von Standardzeit zu Sommerzeit erfolgt. 
  
Dieses Element weist ein Minimales Vorkommen von Null und ein maximales Vorkommen von 1 auf.
  
## <a name="example"></a>Beispiel

Der folgende Teil einer Anforderung stellt eine Übergangszeit von 14:00 Uhr dar. von Standardzeit zu Sommerzeit.
  
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
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

