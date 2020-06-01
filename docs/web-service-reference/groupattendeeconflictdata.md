---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: Das GroupAttendeeConflictData-Element enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer mit Konflikten sowie die Anzahl der Benutzer, die in einer Verteilerliste keine Verfügbarkeitsinformationen für eine vorgeschlagene Besprechungszeit haben.
ms.openlocfilehash: c75a4e6f8fdff7fb2514f448350fee9f1acb9775
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462929"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

Das **GroupAttendeeConflictData** -Element enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer mit Konflikten sowie die Anzahl der Benutzer, die in einer Verteilerliste keine Verfügbarkeitsinformationen für eine vorgeschlagene Besprechungszeit haben. 
  
- [GetUserAvailabilityResponse](getuseravailabilityresponse.md)
- [SuggestionsResponse](suggestionsresponse.md)
- [SuggestionDayResultArray](suggestiondayresultarray.md)
- [SuggestionDayResult](suggestiondayresult.md)
- [SuggestionArray](suggestionarray.md)
- [Vorschlag](suggestion.md)
- [AttendeeConflictDataArray](attendeeconflictdataarray.md)
- [GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

**GroupAttendeeConflictData**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[NumberOfMembers](numberofmembers.md) <br/> |Stellt die Anzahl der Benutzer, Ressourcen und Räume in einer Verteilerliste dar.  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |Stellt die Anzahl der Verteilerlistenmitglieder dar, die für eine vorgeschlagene Besprechungszeit zur Verfügung stehen. Dieses Element stellt Elemente dar, für die der Status **frei**ist.  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |Gibt die Anzahl der Verteilerlistenmitglieder an, die einen Konflikt mit einer vorgeschlagenen Besprechungszeit haben. Dieses Element stellt Elemente dar, die den Status " **beschäftigt**", " **Abwesend**" oder " **vorläufig** " aufweisen.  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |Gibt die Anzahl der Gruppenmitglieder an, die keine Frei/Gebucht-Daten veröffentlicht haben, die mit einer vorgeschlagenen Besprechungszeit verglichen werden sollen. Dieses Element stellt Elemente einer Verteilerliste dar, die zu groß sind, oder Mitglieder, die **keinen Daten** Status aufweisen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **GroupAttendeeConflictData** -Element ist in der Antwort vorhanden, wenn ein Teilnehmer im [GetUserAvailabilityRequest](getuseravailabilityrequest.md) in eine Verteilerliste aufgelöst wird. Das **GroupAttendeeConflictData** -Element identifiziert drei Zustände für Mitglieder einer Verteilerliste: verfügbar, widersprüchlich oder keine Daten. Die Erweiterung für Verteilerlisten unterstützt bis zu 100 Mitglieder. Das [NumberOfMembers](numberofmembers.md) -Element kann daher maximal 100 Mitglieder enthalten. Die Erweiterung der Verteilerliste ist rekursiv. Wenn eine Verteilerliste eine untergeordnete Verteilerliste enthält, die die gesamte übergeordnete Mitgliedschaft auf über 100 Mitglieder erweitert, wird die untergeordnete Verteilerliste nicht erweitert und wird als ein einzelner Eintrag der [NumberOfMembersWithNoData](numberofmemberswithnodata.md) -Elementanzahl gezählt. Wenn eine untergeordnete Verteilerliste erweitert werden kann und die gesamte übergeordnete Mitgliedschaft nicht auf mehr als 100 Mitglieder erweitert wird, wird die Mitgliedschaft erweitert, und die Mitgliederanzahl wird den untergeordneten Elementen des **GroupAttendeeConflictData** -Elements hinzugefügt. 
  
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
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

