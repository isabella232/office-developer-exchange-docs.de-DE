---
title: DaylightTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: Das DaylightTime-Element stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, der durch das Bias -Element (UTC) in Regionen dargestellt wird, in denen Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt.
ms.openlocfilehash: 95d09fe01602f2d55d1a39dc7164a3f60a328f2a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543431"
---
# <a name="daylighttime"></a>DaylightTime

Das **DaylightTime-Element** stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, der durch das [Bias -Element (UTC)](bias-utc.md) in Regionen dargestellt wird, in denen Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt. 
  
- [TimeZone (Verfügbarkeit)](timezone-availability.md) 
- [DaylightTime](daylighttime.md)
  
```xml
<DaylightTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</DaylightTime>
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
|[Jahr](year.md) <br/> |Wird verwendet, um eine Zeitzone zu definieren, die sich je nach Jahr ändert. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[TimeZone (Verfügbarkeit)](timezone-availability.md) <br/> | Enthält Elemente, die Zeitzoneninformationen identifizieren.<br/><br/>Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.<br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a>Beispiel

Die folgende partielle GetUserAvailability-Anforderung stellt eine Clientanwendung an einem Ort dar, der Sommerzeit erkennt.
  
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

