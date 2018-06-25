---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: Das StandardTime-Element stellt einen Offset von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die Verschiebung (UTC) Element dargestellt wird. Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.
ms.openlocfilehash: 726c31ffba06c1c437711b88444ec5eba45b520d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831546"
---
# <a name="standardtime"></a>StandardTime

Das **StandardTime** -Element stellt einen Offset von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird. Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird. 
  
- [TimeZone (Verfügbarkeit)](timezone-availability.md)
- [StandardTime](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 **SerializableTimeZoneTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bias](bias.md) <br/> |Stellt den Offset von der UTC-Offset, der durch das Element [Bias (UTC)](bias-utc.md) für Standardzeit und Sommerzeit identifiziert wird. Dieser Wert wird in Minuten angegeben.  <br/> |
|[Time](time.md) <br/> |Stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone.  <br/> |
|[DayOrder](dayorder.md) <br/> |Stellt das _n_th Vorkommen des Tags, das im Element [DayOfWeek (TimeZone)](dayofweek-timezone.md) angegeben wird, die das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt.  <br/> |
|[Month](month.md) <br/> |Stellt den Übergang Monat des Jahres zu und von Standardzeit und Sommerzeit einer Zeitzone.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Tritt für der Übergang zu und von Standardzeit und Sommerzeit Wochentag darstellt.  <br/> |
|[Jahr](year.md) <br/> |Definiert eine Zeitzone, die sich je nach dem Jahr ändern. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZone (Verfügbarkeit)](timezone-availability.md) <br/> | Enthält Elemente, die Informationen zur Zeitzone zu identifizieren. Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit. <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>Hinweise

Das **StandardTime** -Element stellt eine Offset Zeit, die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird. Wenn das untergeordnete [Bias](bias.md) -Element gleich 0 ist, ist die Standardzeit gleich dem Bias Offset von UTC, die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Bereich, in dem Sommerzeit beobachtet wird. Der Übergang von Sommerzeit auf Normalzeit wird um 2 Uhr morgens eingehalten Klicken Sie auf der fünften Sonntag der zehnte Monat.
  
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

