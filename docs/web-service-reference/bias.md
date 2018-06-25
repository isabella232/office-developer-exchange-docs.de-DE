---
title: Bias
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bias
api_type:
- schema
ms.assetid: ae10aa44-e6d3-483d-a3e6-bb9c45966810
description: Bias-Element stellt den Offset vom Offset (Coordinated Universal Time, UTC) vom für Standardzeit und Sommerzeit Bias (UTC)-Element identifiziert. Dieser Wert wird in Minuten angegeben.
ms.openlocfilehash: 770bf97b030ac1293595560bc269f54896e35a15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757447"
---
# <a name="bias"></a>Bias

**Bias** -Element stellt den Offset vom Offset (Coordinated Universal Time, UTC) vom für Standardzeit und Sommerzeit [Bias (UTC)](bias-utc.md) -Element identifiziert. Dieser Wert wird in Minuten angegeben. 
  
```xml
<Bias>...</Bias>
```

**int**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> | Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) . Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.<br/><br/>Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element:<br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[DaylightTime](daylighttime.md) <br/> | Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.  <br/><br/>Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:<br/><br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt eine ganze Zahl.
  
## <a name="remarks"></a>Hinweise

Der Offset verwendet, um die Ortszeit bestimmen kann nur mithilfe eines der **Bias** Elemente bereitgestellt werden. Die Summe der Werte von dem Bias-Element zur Verfügung gestellt, durch das [DaylightTime](daylighttime.md) -Element oder das [StandardTime](standardtime.md) -Element plus [Weltzeit (UTC) Bias](bias-utc.md) -Element identifiziert die Ortszeit. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Benutzer, von der wem Sommerzeit angibt durch Anpassen der UTC-Offset von 60 Minuten verwendet. Dadurch wird effektiv die Verschiebung 420 Minuten von UTC.
  
```xml
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>5</DayOrder>
    <Month>10</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>4</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
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

