---
title: TimeZone (Verfügbarkeit)
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
description: TimeZone-Element enthält Elemente, die Informationen zur Zeitzone zu identifizieren. Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.
ms.openlocfilehash: dc2466e8039819edc82294ff05f1746ada64cb43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839229"
---
# <a name="timezone-availability"></a>TimeZone (Verfügbarkeit)

**TimeZone** -Element enthält Elemente, die Informationen zur Zeitzone zu identifizieren. Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit. 
  
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
|[Bias (UTC)](bias-utc.md) <br/> |Stellt den allgemeinen Offset von koordinierte Weltzeit (UTC). Dieser Wert wird in Minuten angegeben.  <br/> |
|[StandardTime](standardtime.md) <br/> |Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) . Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.  <br/> |
|[DaylightTime](daylighttime.md) <br/> |Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityRequest](getuseravailabilityrequest.md) <br/> |Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet. Dies ist eine Stammelements.  <br/> Das **TimeZone** -Element in der Nachricht GetUserAvailabilityRequest stellt die Zeitzone, in dem die DateTime-Werte in der Anforderung angegeben werden. Die von den Verfügbarkeitsdienst zurückgegebenen DateTime-Werte sind auch in dieser Zeitzone.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[WorkingHours](workinghours-ex15websvcsotherref.md) <br/> |Stellt die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.  <br/> **TimeZone** -Element in der Nachricht GetUserAvailabilityResponse stellt die Einstellungen der Zeitzone des angeforderten Postfachbenutzers.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist im [GetUserAvailabilityRequest](getuseravailabilityrequest.md) -Element erforderlich. Dieses Element wird höchstens einmal oder wenn das übergeordnete Element ist mindestens Male [WorkingHours](workinghours-ex15websvcsotherref.md) -Element. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von UTC von 8 Stunden in der Clientanwendung identifiziert.
  
```XML
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[Bias](bias.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

