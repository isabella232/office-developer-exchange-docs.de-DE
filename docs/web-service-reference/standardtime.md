---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: Das StandardTime-Element stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, die durch das Bias -Element (UTC) dargestellt wird. Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird.
ms.openlocfilehash: ceddc511bf1883078c88dee240fc308d02024220
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544661"
---
# <a name="standardtime"></a>StandardTime

Das **StandardTime-Element** stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, die durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird. Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird. 
  
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
|[Bias](bias.md) <br/> |Stellt den Offset vom UTC-Offset dar, der vom [Bias -Element (UTC)](bias-utc.md) für Standardzeit und Sommerzeit identifiziert wird. Dieser Wert wird in Minuten angegeben.  <br/> |
|[Time](time.md) <br/> |Stellt die Übergangszeit des Tages zu und von Standardzeit und Sommerzeit dar.  <br/> |
|[DayOrder](dayorder.md) <br/> |Stellt das _n_th Vorkommen des Tags dar, der im [DayOfWeek (TimeZone)-Element](dayofweek-timezone.md) angegeben ist, das das Datum des Übergangs von und zu Standardzeit und Sommerzeit darstellt.  <br/> |
|[Month](month.md) <br/> |Stellt den Übergangsmonat des Jahres zu und von Standardzeit und Sommerzeit dar.  <br/> |
|[DayOfWeek (TimeZone)](dayofweek-timezone.md) <br/> |Stellt den Wochentag dar, an dem der Übergang zu und von Standardzeit und Sommerzeit erfolgt.  <br/> |
|[Jahr](year.md) <br/> |Definiert eine Zeitzone, die sich je nach Jahr ändert. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZone (Verfügbarkeit)](timezone-availability.md) <br/> | Enthält Elemente, die Zeitzoneninformationen identifizieren. Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit. <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **StandardTime-Element** stellt eine Offsetzeit dar, die durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird. Wenn das untergeordnete [Bias-Element](bias.md) gleich 0 ist, entspricht die Standardzeit dem Bias-Offset von UTC, der durch das [Bias -Element (UTC)](bias-utc.md) dargestellt wird. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt eine Region, in der Sommerzeit beobachtet wird. Der Übergang von Sommerzeit zu Standardzeit wird um 14:00 Uhr beobachtet. am fünften Sonntag des zehnten Monats.
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

