---
title: EndTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: Das EndTime-Element darstellt, das Ende einer bestimmten Zeitspanne.
ms.openlocfilehash: 7d3d186618a7bcc05ad82532e13e03d2e67a0e40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758254"
---
# <a name="endtime"></a>EndTime

Das **EndTime** -Element darstellt, das Ende einer bestimmten Zeitspanne. 
  
```xml
<EndTime>dateTime</EndTime>
```

 **dateTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zeitfenster](timewindow.md) <br/> |Gibt die Zeitspanne für die Verfügbarkeit Benutzerinformationen abgefragt.<br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.<br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Dauer (' UserOofSettings ')](duration-useroofsettings.md) <br/> | Gibt die Dauer, für die der Status von Office (OOF) aktiviert ist, wenn das Element [OofState](oofstate.md) auf **Geplante Tasks**festgelegt ist.  <br/><br/>  Im folgenden sind die möglichen XPath-Ausdrücke auf dieses Element:<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Vorkommen](occurrence.md) <br/> |Stellt ein einzelnes geändertes Vorkommen des ein wiederkehrendes Kalenderelement.  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Stellt eine einzelne Kalender Element vorkommen. Dies ist für Verfügbarkeit Abfragen verwendet. Das **EndTime** -Element ist im **CalendarEvent** -Element erforderlich. Das **EndTime** -Element im **CalendarEvent** -Element ist für den Typ **CalendarEvent** eindeutig.<br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich.
  
## <a name="remarks"></a>Hinweise

Das [StartTime](starttime.md) -Element darstellt, das Ende einer bestimmten Zeitspanne. 
  
Die Endzeit darstellt der Client-Zeit.
  
Das Schema enthält viele [EndTime](endtime.md) Elemente. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
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

