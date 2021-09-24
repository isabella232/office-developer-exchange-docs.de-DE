---
title: NumberOfMembersWithNoData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- NumberOfMembersWithNoData
api_type:
- schema
ms.assetid: 7ca9c57c-9519-442c-a9f4-dca2b0309716
description: Das NumberOfMembersWithNoData-Element stellt die Anzahl der Verteilerlistenmitglieder dar, die keine Frei/Gebucht-Daten veröffentlicht haben, die mit einer vorgeschlagenen Besprechungszeit verglichen werden sollen. Dieses Element stellt Mitglieder einer Verteilerliste dar, die zu groß ist, oder Mitglieder, die den Status "Keine Daten" aufweisen.
ms.openlocfilehash: 4b021ce75a84eca3e1b5a66cf51f6b5d7adec86b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529685"
---
# <a name="numberofmemberswithnodata"></a>NumberOfMembersWithNoData

Das **NumberOfMembersWithNoData-Element** stellt die Anzahl der Verteilerlistenmitglieder dar, die keine Frei/Gebucht-Daten veröffentlicht haben, die mit einer vorgeschlagenen Besprechungszeit verglichen werden sollen. Dieses Element stellt Mitglieder einer Verteilerliste dar, die zu groß ist, oder Mitglieder, die den Status **"Keine Daten"** aufweisen. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Vorschlag](suggestion.md)
  
[AttendeeConflictDataArray](attendeeconflictdataarray.md)
  
[GroupAttendeeConflictData](groupattendeeconflictdata.md)
  
[NumberOfMembersWithNoData](numberofmemberswithnodata.md)
  
```xml
<NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
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
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer, die Konflikte haben, und die Anzahl der Benutzer, die keine Verfügbarkeitsinformationen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit haben.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Ein Kontakt in einer Gruppe, der nicht über ein Postfach verfügt, ist ein Beispiel für ein Verteilerlistenmitglied, das keine Kalenderdaten besitzt. Ein Kontakt hat möglicherweise auch aus den folgenden Gründen **keinen Datenstatus:** 
  
- Berechtigungen sind nicht ausreichend.
    
- Die Verteilerliste ist zu groß, um sie zu erweitern.
    
- Der Active Directory-Verzeichnisdienst ist nicht verfügbar.
    
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

