---
title: CalendarEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CalendarEvent
api_type:
- schema
ms.assetid: 91958c01-1fcb-4ac0-8601-5e5b434c988a
description: Das CalendarEvent-Element stellt ein eindeutiges Kalenderelement-Vorkommen dar.
ms.openlocfilehash: fd57517595659f2081c82fe9f4665ce2c39059fe
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514823"
---
# <a name="calendarevent"></a>CalendarEvent

Das **CalendarEvent-Element** stellt ein eindeutiges Kalenderelement-Vorkommen dar. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[FreeBusyResponseArray](freebusyresponsearray.md)
  
[FreeBusyResponse](freebusyresponse.md)
  
[FreeBusyView](freebusyview.md)
  
[CalendarEventArray](calendareventarray.md)
  
[CalendarEvent](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 **CalendarEvent**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Stellt den Anfang eines Kalenderereignisses dar. Dies ist ein erforderliches untergeordnetes Element.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende eines Kalenderereignisses dar. Dies ist ein erforderliches untergeordnetes Element.  <br/> |
|[BusyType](busytype.md) <br/> |Stellt den Frei/Gebucht-Status für ein Kalenderereignis dar. Dies ist ein erforderliches untergeordnetes Element.  <br/> |
|[CalendarEventDetails](calendareventdetails.md) <br/> |Stellt zusätzliche Informationen für ein Kalenderereignis bereit. Dies ist ein optionales untergeordnetes Element.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarEventArray](calendareventarray.md) <br/> |Enthält eine Reihe eindeutiger Kalenderelementvorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen.  <br/> Es folgt der XPath 2.0-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Termin- und Besprechungszeiten werden in der Zeitzone des Clients zurückgegeben. Alle untergeordneten Elemente werden in der Reihenfolge aufgelistet, in der sie auftreten. Die Detailebene, die von diesem Element bereitgestellt wird, hängt von den Berechtigungen ab, die dem Anforderer erteilt wurden.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

