---
title: StartTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StartTime
api_type:
- schema
ms.assetid: 1fac7937-7a06-4d66-9d2a-14423bcb3b37
description: Das StartTime-Element stellt den Anfang einer Zeitspanne dar.
ms.openlocfilehash: e6d9034fa1b01f0f0969837761f4da7c36cea752
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531653"
---
# <a name="starttime"></a>StartTime

Das **StartTime-Element** stellt den Anfang einer Zeitspanne dar. 
  
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
|[TimeWindow](timewindow.md) <br/> |Gibt die Zeitspanne an, die für die Benutzerverfügbarkeitsinformationen abgefragt wird.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/><br/>  `/GetUserAvailabilityRequest/FreeBusyViewOptions/TimeWindow` <br/> |
|[DetailedSuggestionsWindow](detailedsuggestionswindow.md) <br/> |Gibt die Zeitspanne an, für die detaillierte Informationen zu vorgeschlagenen Besprechungszeiten abgefragt werden.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:  <br/> <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions/DetailedSuggestionsWindow` <br/> |
|[Dauer (UserOofSettings)](duration-useroofsettings.md) <br/> | Gibt die Dauer an, für die der Status Out of Office (OOF) aktiviert ist, wenn das [OofState](oofstate.md) -Element auf **Scheduled** festgelegt ist.  <br/><br/>  Es folgen die möglichen XPath-Ausdrücke für dieses Element: <br/> <br/>  `/SetUserOofSettingsRequest/UserOofSettings/Duration` <br/><br/>  `/GetUserOofSettingsResponse/OofSettings/Duration` <br/> |
|[CalendarEvent](calendarevent.md) <br/> |Stellt ein eindeutiges Kalenderelement dar. Dies wird für Verfügbarkeitsanfragen verwendet. Das **StartTime-Element** ist im **CalendarEvent-Element** erforderlich. Das **StartTime-Element** im **CalendarEvent-Element** ist für den **CalendarEvent-Typ** eindeutig, obwohl es dieselben Facetwerte enthält, die die **StartTime-Elemente** im **Duration-Typ** enthalten.  <br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray/CalendarEvent[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das [EndTime-Element](endtime.md) stellt das Ende der Zeitspanne dar. 
  
Das Schema enthält viele [StartTime-Elemente.](starttime.md) 
  
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

