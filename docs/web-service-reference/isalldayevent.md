---
title: IsAllDayEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsAllDayEvent
api_type:
- schema
ms.assetid: 29140a64-9d7a-4a14-a10d-c98197c9831b
description: Das IsAllDayEvent-Element gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt.
ms.openlocfilehash: f0c975deecf96e94599a47ef2c33e54a7d1a80b9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526536"
---
# <a name="isalldayevent"></a>IsAllDayEvent

Das **IsAllDayEvent** -Element gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt. 
  
```xml
<IsAllDayEvent/>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich, wenn dieses Element enthalten ist. Der Wert **true** gibt an, dass das Element ein ganztägiges Ereignis darstellt. Der Wert **false** gibt an, dass das Element weniger als die Arbeitszeiten eines Benutzers umfasst. 
  
## <a name="remarks"></a>Bemerkungen

Ein ganztägiges Ereignis umfasst die Dauer der Arbeitsstunden, die für ein Postfach definiert ist.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

