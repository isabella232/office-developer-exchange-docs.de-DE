---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: Das AttendeeConflictDataArray-Element enthält ein Array von Conflict-Daten für die abgefragte Teilnehmer bei der Konflikte GetUserAvailability identifiziert.
ms.openlocfilehash: 169312b8a3d37c014ba58fbfe094d786b134fc90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757401"
---
# <a name="attendeeconflictdataarray"></a>AttendeeConflictDataArray

Das **AttendeeConflictDataArray** -Element enthält ein Array von Conflict-Daten für die abgefragte Teilnehmer bei der [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert.
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
- [SuggestionsResponse](suggestionsresponse.md)
  
- [SuggestionDayResultArray](suggestiondayresultarray.md)
  
- [SuggestionDayResult](suggestiondayresult.md)
  
- [SuggestionArray](suggestionarray.md)
  
- [Vorschlag](suggestion.md)
  
- [AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 **ArrayOfAttendeeConflictData**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UnknownAttendeeConflictData](unknownattendeeconflictdata.md) <br/> |Stellt einen Teilnehmer nicht aufgelöst werden oder einen Teilnehmer, der nicht auf einen Benutzer, der Verteilerliste oder der Kontakt ist dar.  <br/> |
|[IndividualAttendeeConflictData](individualattendeeconflictdata.md) <br/> |Enthält eines Benutzers oder Kontakts Frei/Gebucht-Status für ein Time-Fenster, das zur selben Zeit als die vorgeschlagenen auftritt, Besprechungszeit im [Vorschlag](suggestion.md) -Element identifiziert.  <br/> |
|[TooBigGroupAttendeeConflictData](toobiggroupattendeeconflictdata.md) <br/> |Stellt einen Teilnehmer, die als Verteilerliste aufgelöst, die aufgrund ihrer Größe erweitern.  <br/> |
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Enthält Konfliktinformationen über die Anzahl von Benutzern zur Verfügung, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die nicht zu Ihrer Verfügbarkeit einsehen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit verfügen aggregierte.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Vorschlag](suggestion.md) <br/> |Stellt ein einzelnes meeting Zeit Vorschlag.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a>Hinweise

Die Position jedes Elements in der **AttendeeConflictDataArray** entspricht der Position der abgefragten Teilnehmer im [MailboxDataArray](mailboxdataarray.md) -Element. Jeden abgefragte Teilnehmer muss eines der untergeordneten Elemente **AttendeeConflictDataArray** entsprechen. Diese Elemente darstellen einen einzelnen Konflikt mit der vorgeschlagenen Besprechungszeit im [Vorschlag](suggestion.md) -Element identifiziert. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md) 
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

