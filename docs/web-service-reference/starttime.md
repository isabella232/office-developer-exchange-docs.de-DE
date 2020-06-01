---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: Das StartTime-Element stellt den Anfang einer Zeitspanne dar.
ms.openlocfilehash: 16bee698b65dc512a709e2af9ddfe8629347fee3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458565"
---
# <a name="starttime"></a>StartTime

Das **StartTime-Element stellt** den Anfang einer Zeitspanne dar. 
  
```xml
<StartTime/
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
|[TimeWindow](timewindow.md) <br/> |Gibt den Zeitraum an, der für die Informationen zur Benutzerverfügbarkeit abgefragt wird.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt den Zeitraum an, der nach detaillierten Informationen zu vorgeschlagenen Besprechungszeiten abgefragt wird.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:  <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> | Gibt die Dauer an, für die der Abwesenheit (Out of Office, OOF) Status aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled**festgelegt ist.  <br/><br/>  Im folgenden sind die möglichen XPath-Ausdrücke für dieses Element angegeben: <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Stellt ein eindeutiges Kalenderelement vorkommen dar. Dies wird für Verfügbarkeitsabfragen verwendet. Das **StartTime** -Element ist im **CalendarEvent** -Element erforderlich. Das **StartTime** -Element im **CalendarEvent** -Element ist für den **CalendarEvent** -Typ eindeutig, obwohl es dieselben Facet-Werte enthält, die die **StartTime** -Elemente im **Duration** -Typ enthalten.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich.
  
## <a name="remarks"></a>Bemerkungen

Das [EndTime](endtime.md) -Element stellt das Ende der Zeitspanne dar. 
  
Das Schema enthält viele [StartTime](starttime.md) -Elemente. 
  
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
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

