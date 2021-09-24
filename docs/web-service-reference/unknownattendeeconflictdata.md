---
title: UnknownAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- UnknownAttendeeConflictData
api_type:
- schema
ms.assetid: 70e41268-c231-4587-9d23-e46927fe5272
description: Das UnknownAttendeeConflictData-Element stellt einen nicht lösbaren Teilnehmer oder einen Teilnehmer dar, der kein Benutzer, keine Verteilerliste oder kein Kontakt ist.
ms.openlocfilehash: e7aec79a2aa15cfd149e47affb1efb2b215497e1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515089"
---
# <a name="unknownattendeeconflictdata"></a>UnknownAttendeeConflictData

Das **UnknownAttendeeConflictData-Element** stellt einen nicht lösbaren Teilnehmer oder einen Teilnehmer dar, der kein Benutzer, keine Verteilerliste oder kein Kontakt ist. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Vorschlag](suggestion.md)
  
[AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
[UnknownAttendeeConflictData](unknownattendeeconflictdata.md)
  
```xml
<UnknownAttendeeConflictData/>
```

 **UnknownAttendeeConflictData**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AttendeeConflictDataArray](attendeeconflictdataarray.md) <br/> |Enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Teilnehmer ist unbekannt, wenn er nicht für ein Active Directory-Verzeichnisdienstobjekt aufgelöst werden kann. Ein Teilnehmer ist nicht aufgelöst, wenn nicht festgestellt werden kann, dass es sich um einen Benutzer, eine Gruppe oder einen Kontakt handelt. Beispielsweise wird ein Teilnehmer nicht aufgelöst, wenn es sich um einen E-Mail-aktivierten öffentlichen Ordner handelt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

