---
title: NumberOfMembers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembers
api_type:
- schema
ms.assetid: 845fb877-de49-4e26-8885-6f026edd9ee9
description: Das Element NumberOfMembers stellt die Anzahl von Benutzern, Ressourcen und Chatrooms in einer Verteilerliste dar.
ms.openlocfilehash: 9777660b1a54bfb5afb6e569ba1009a1654bdef3
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830635"
---
# <a name="numberofmembers"></a>NumberOfMembers

Das Element **NumberOfMembers** stellt die Anzahl von Benutzern, Ressourcen und Chatrooms in einer Verteilerliste dar. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Vorschlag](suggestion.md)
  
[AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
[GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
[NumberOfMembers](numberofmembers.md)
  
```xml
<NumberOfMembers>...</NumberOfMembers>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Enthält Konfliktinformationen über die Anzahl von Benutzern zur Verfügung, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die nicht zu Ihrer Verfügbarkeit einsehen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit verfügen aggregierte.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a>Hinweise

Der maximale Wert des **NumberOfMembers** -Elements ist 100. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

