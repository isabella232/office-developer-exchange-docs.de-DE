---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: Das GroupAttendeeConflictData-Element enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer, die Konflikte haben, und die Anzahl der Benutzer, die keine Verfügbarkeitsinformationen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit haben.
ms.openlocfilehash: 19ac366da5ad48cbc6c9e2aaa710a8c5f00e1151
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519555"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

Das **GroupAttendeeConflictData-Element** enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer, die Konflikte haben, und die Anzahl der Benutzer, die keine Verfügbarkeitsinformationen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit haben. 
  
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
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |Stellt die Anzahl der Mitglieder der Verteilerliste dar, die für eine vorgeschlagene Besprechungszeit verfügbar sind. Dieses Element stellt Elemente dar, für die der Status **Kostenlos** ist.  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |Stellt die Anzahl der Mitglieder der Verteilerliste dar, die einen Konflikt mit einer vorgeschlagenen Besprechungszeit haben. Dieses Element stellt Elemente dar, die den Status **"Beschäftigt",** **"OOF"** oder **"Mit Vorbehalt"** haben.  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |Stellt die Anzahl der Gruppenmitglieder dar, die keine Frei/Gebucht-Daten veröffentlicht haben, die mit einer vorgeschlagenen Besprechungszeit verglichen werden sollen. Dieses Element stellt Mitglieder einer Verteilerliste dar, die zu groß ist, oder Mitglieder, die den Status **"Keine Daten"** aufweisen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **GroupAttendeeConflictData-Element** ist in der Antwort vorhanden, wenn ein Teilnehmer in [getUserAvailabilityRequest](getuseravailabilityrequest.md) in eine Verteilerliste aufgelöst wird. Das **GroupAttendeeConflictData-Element** identifiziert drei Zustände für Mitglieder einer Verteilerliste: verfügbare, in Konflikt stehende oder keine Daten. Die Erweiterung der Verteilerliste unterstützt bis zu 100 Mitglieder. Daher kann das [NumberOfMembers-Element](numberofmembers.md) maximal 100 Elemente enthalten. Die Erweiterung der Verteilerliste ist rekursiv. Wenn eine Verteilerliste eine untergeordnete Verteilerliste enthält, die die gesamt übergeordnete Mitgliedschaft auf über 100 Mitglieder erweitert, wird die untergeordnete Verteilerliste nicht erweitert und als einzelner Eintrag der Anzahl der [NumberOfMembersWithNoData-Elemente](numberofmemberswithnodata.md) gezählt. Wenn eine untergeordnete Verteilerliste erweitert werden kann und die gesamt übergeordnete Mitgliedschaft nicht auf mehr als 100 Mitglieder erweitert wird, wird die Mitgliedschaft erweitert, und die Mitgliederanzahl wird den untergeordneten Elementen des **GroupAttendeeConflictData-Elements** hinzugefügt. 
  
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

