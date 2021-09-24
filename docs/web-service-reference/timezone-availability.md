---
title: TimeZone (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: Das TimeZone-Element enthält Elemente, die Zeitzoneninformationen identifizieren. Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.
ms.openlocfilehash: 7ca6f0f2d9950770055d19c04adab9b76b95c295
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538842"
---
# <a name="timezone-availability"></a>TimeZone (Verfügbarkeit)

Das **TimeZone-Element** enthält Elemente, die Zeitzoneninformationen identifizieren. Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit. 
  
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
|[Bias (UTC)](bias-utc.md) <br/> |Stellt den allgemeinen Offset von koordinierter Weltzeit (COORDINATED Universal Time, UTC) dar. Dieser Wert wird in Minuten angegeben.  <br/> |
|[StandardTime](standardtime.md) <br/> |Stellt einen Offset von der Zeit relativ zur UTC dar, die durch das [Bias (UTC)-Element](bias-utc.md) dargestellt wird. Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen Sommerzeit beobachtet wird.  <br/> |
|[DaylightTime](daylighttime.md) <br/> |Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias -Element (UTC)](bias-utc.md) in Regionen, in denen Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit von der Standardzeit erfolgt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Benutzerverfügbarkeitsinformationen verwendet werden. Dies ist ein Stammelement.  <br/> Das **TimeZone-Element** in der GetUserAvailabilityRequest-Nachricht stellt die Zeitzone dar, in der die DateTime-Werte in der Anforderung angegeben werden. Die vom Verfügbarkeitsdienst zurückgegebenen DateTime-Werte befinden sich ebenfalls in dieser Zeitzone.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.  <br/> Das **TimeZone-Element** in der GetUserAvailabilityResponse-Nachricht stellt die Zeitzoneneinstellungen des angeforderten Postfachbenutzers dar.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist im [GetUserAvailabilityRequest-Element](getuseravailabilityrequest.md) erforderlich. Dieses Element tritt höchstens einmal oder mindestens null mal auf, wenn das übergeordnete Element das [WorkingHours-Element](workinghours-ex15websvcsotherref.md) ist. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von UTC von 8 Stunden in der Clientanwendung identifiziert.
  
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


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

