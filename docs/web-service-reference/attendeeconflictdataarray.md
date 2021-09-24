---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: Das AttendeeConflictDataArray-Element enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im GetUserAvailability-Vorgang identifiziert wurden.
ms.openlocfilehash: 1054fba62c7e0746a13471433d6d619a304ff848
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524360"
---
# <a name="attendeeconflictdataarray"></a>AttendeeConflictDataArray

Das **AttendeeConflictDataArray-Element** enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.
  
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
|[UnknownAttendeeConflictData](unknownattendeeconflictdata.md) <br/> |Stellt einen nicht lösbaren Teilnehmer oder einen Teilnehmer dar, der kein Benutzer, keine Verteilerliste oder kein Kontakt ist.  <br/> |
|[IndividualAttendeeConflictData](individualattendeeconflictdata.md) <br/> |Enthält den Frei/Gebucht-Status eines Benutzers oder Kontakts für ein Zeitfenster, das zur gleichen Zeit wie die im [Suggestion-Element](suggestion.md) identifizierte vorgeschlagene Besprechungszeit auftritt.  <br/> |
|[TooBigGroupAttendeeConflictData](toobiggroupattendeeconflictdata.md) <br/> |Stellt einen Teilnehmer dar, der als Verteilerliste aufgelöst wurde, die zu groß zum Erweitern war.  <br/> |
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer, die Konflikte haben, und die Anzahl der Benutzer, die keine Verfügbarkeitsinformationen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit haben.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Vorschlag](suggestion.md) <br/> |Stellt einen einzelnen Besprechungszeitvorschlag dar.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die Position der einzelnen Elemente im **AttendeeConflictDataArray entspricht** der Position der abgefragten Teilnehmer im [MailboxDataArray-Element.](mailboxdataarray.md) Jeder abgefragte Teilnehmer muss einem der **untergeordneten AttendeeConflictDataArray-Elemente** entsprechen. Diese Elemente stellen einen einzelnen Konflikt mit der vorgeschlagenen Besprechungszeit dar, die im [Suggestion-Element](suggestion.md) angegeben ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md) 
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

