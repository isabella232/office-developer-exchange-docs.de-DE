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
description: Das GroupAttendeeConflictData-Element enthält aggregierte Konfliktinformationen über die Anzahl der Benutzer, die verfügbar sind, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die keine Informationen zur Verfügbarkeit in einer Verteilerliste für auf ein Vorgeschlagene Besprechungszeit.
ms.openlocfilehash: 382b4d866c95de98bd444cd6226d71813889d4f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829757"
---
# <a name="groupattendeeconflictdata"></a>GroupAttendeeConflictData

Das **GroupAttendeeConflictData** -Element enthält aggregierte Konfliktinformationen über die Anzahl der Benutzer, die verfügbar sind, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die keine Informationen zur Verfügbarkeit in einer Verteilerliste für einen Zeitraum vorgeschlagenen Besprechung. 
  
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
|[NumberOfMembers](numberofmembers.md) <br/> |Die Anzahl von Benutzern, Ressourcen und Chatrooms in einer Verteilerliste darstellt.  <br/> |
|[NumberOfMembersAvailable](numberofmembersavailable.md) <br/> |Stellt die Anzahl der Mitglieder der Verteilerliste, die für einen Zeitraum vorgeschlagenen Besprechung zur Verfügung stehen. Dieses Element stellt Member für die der Status **frei**ist.  <br/> |
|[NumberOfMembersWithConflict](numberofmemberswithconflict.md) <br/> |Stellt die Anzahl der Mitglieder der Verteilerliste, die einen Konflikt mit einer vorgeschlagenen Besprechungszeit haben. Dieses Element stellt Mitglieder, die den Status **beschäftigt**, **ABWESEND**oder **mit Vorbehalt** aufweisen.  <br/> |
|[NumberOfMembersWithNoData](numberofmemberswithnodata.md) <br/> |Stellt die Anzahl der Mitglieder, die nicht veröffentlichte Frei/Gebucht-Daten mit einer vorgeschlagenen Besprechung Uhrzeit verglichen verfügen. Dieses Element stellt die Mitglieder von Verteilerlisten, die zu groß ist oder Mitglieder, die **Keine Daten** Status aufweisen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Enthält ein Array von Conflict-Daten für die abgefragte Teilnehmer bei der [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>Hinweise

Das **GroupAttendeeConflictData** -Element wird in der Antwort vorhanden ist, wenn ein Teilnehmer in der [GetUserAvailabilityRequest](getuseravailabilityrequest.md) in einer Verteilerliste aufgelöst wird. Das **GroupAttendeeConflictData** -Element identifiziert drei Zustände für Mitglieder von Verteilerlisten: verfügbar, Konflikt, oder keine Daten. Verteilerlistenerweiterung unterstützt bis zu 100 Elemente. Aus diesem Grund kann das [NumberOfMembers](numberofmembers.md) -Element ein Maximum von bis zu 100 Mitgliedern enthalten. Die Erweiterung der Verteilerliste ist rekursiv. Wenn eine Verteilerliste eine Verteilerliste untergeordneten enthält, die das mehr als 100 Mitgliedern die Mitgliedschaft insgesamt übergeordneten erweitert, die untergeordneten Verteilerliste nicht erweitert werden und wird als nur ein Eintrag für die Anzahl der [NumberOfMembersWithNoData](numberofmemberswithnodata.md) zählen. Wenn eine Verteilerliste untergeordneten erweitert werden kann und die gesamte übergeordnete Mitgliedschaft wird nicht mehr als 100 Mitgliedern erweitert, deren Mitgliedschaft wird erweitert, und die untergeordneten Elemente des Elements **GroupAttendeeConflictData** die Elementanzahl hinzugefügt werden. 
  
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

