---
title: EndTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- EndTime
api_type:
- schema
ms.assetid: 82e4ef4f-a557-4044-b9b7-d91622f4ac55
description: Das EndTime-Element stellt das Ende einer Zeitspanne dar.
ms.openlocfilehash: 9b7dde6c318bb198e1ec25df19cf3a053feff5cf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540055"
---
# <a name="endtime"></a>EndTime

Das **EndTime-Element** stellt das Ende einer Zeitspanne dar. 
  
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
|[TimeWindow](timewindow.md) <br/> |Gibt die Zeitspanne an, die für die Benutzerverfügbarkeitsinformationen abgefragt wird.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt die Zeitspanne an, für die detaillierte Informationen zu vorgeschlagenen Besprechungszeiten abgefragt werden.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow`.  <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> | Gibt die Dauer an, für die der Status Out of Office (OOF) aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled** festgelegt ist.  <br/><br/>  Es folgen die möglichen XPath-Ausdrücke für dieses Element:<br/><br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[Vorkommen](occurrence.md) <br/> |Stellt ein einzelnes geändertes Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Stellt ein eindeutiges Kalenderelement dar. Dies wird für Verfügbarkeitsanfragen verwendet. Das **EndTime-Element** ist im **CalendarEvent-Element** erforderlich. Das **EndTime-Element** im **CalendarEvent-Element** ist für den **CalendarEvent-Typ** eindeutig.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das [StartTime-Element](starttime.md) stellt den Anfang einer Zeitspanne dar. 
  
Die Endzeit stellt die Uhrzeit des Clients dar.
  
Das Schema enthält viele [EndTime-Elemente.](endtime.md) 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
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

