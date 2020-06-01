---
title: Zeitzone (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: Das TimeZone-Element enthält Elemente, die Zeitzoneninformationen identifizieren. Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.
ms.openlocfilehash: ba4b0a4805dba54450e01e89c5e9ef746404b716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460274"
---
# <a name="timezone-availability"></a>Zeitzone (Verfügbarkeit)

Das **TimeZone** -Element enthält Elemente, die Zeitzoneninformationen identifizieren. Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit. 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 **SerializableTimeZone**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bias (UTC)](bias-utc.md) <br/> |Stellt den allgemeinen Offset von koordinierter Weltzeit (Coordinated Universal Time, UTC) dar. Dieser Wert wird in Minuten angegeben.  <br/> |
|[Standard Time](standardtime.md) <br/> |Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) . Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.  <br/> |
|[DaylightTime](daylighttime.md) <br/> |Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Informationen zur Benutzerverfügbarkeit verwendet werden. Dies ist ein Stammelement.  <br/> Das **TimeZone** -Element in der GetUserAvailabilityRequest-Nachricht stellt die Zeitzone dar, in der die DateTime-Werte in der Anforderung angegeben werden. Die vom Verfügbarkeitsdienst zurückgegebenen DateTime-Werte befinden sich ebenfalls in dieser Zeitzone.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.  <br/> Das **TimeZone** -Element in der GetUserAvailabilityResponse-Nachricht stellt die Zeitzoneneinstellungen des angeforderten Postfachbenutzers dar.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist im [GetUserAvailabilityRequest](getuseravailabilityrequest.md) -Element erforderlich. Dieses Element tritt höchstens einmal oder mindestens null mal auf, wenn das übergeordnete Element das [WorkingHours](workinghours-ex15websvcsotherref.md) -Element ist. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von einer UTC von 8 Stunden in der Clientanwendung identifiziert.
  
```XML
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>11</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>2</DayOrder>
    <Month>3</Month>
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



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[Bias](bias.md)


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

