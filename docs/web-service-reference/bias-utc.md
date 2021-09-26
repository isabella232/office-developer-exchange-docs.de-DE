---
title: Bias (UTC)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Bias
api_type:
- schema
ms.assetid: 15790d5a-5134-457b-8f2b-d9dee1f807a2
description: The Bias element represents the general offset from Coordinated Universal Time (UTC). Dieser Wert wird in Minuten angegeben.
ms.openlocfilehash: c7dc50d13eecab72d06927ce02762e57ec2f8a3e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543653"
---
# <a name="bias-utc"></a>Bias (UTC)

The **Bias** element represents the general offset from Coordinated Universal Time (UTC). Dieser Wert wird in Minuten angegeben. 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
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
|[TimeZone (Verfügbarkeit)](timezone-availability.md) <br/> | Der Container, der die Datum-Uhrzeit-Informationen der Anforderung identifiziert. Dieses Element enthält Informationen zum Übergang zwischen Standardzeit und Sommerzeit.  <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt eine ganze Zahl dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Ein zweites [Bias-Element](bias.md) im Schema stellt den Offset vom Utc-Offset (Coordinated Universal Time) dar. 
  
## <a name="example"></a>Beispiel

Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von 8 Stunden von UTC in der Clientanwendung identifiziert.
  
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
- [Bias](bias.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

