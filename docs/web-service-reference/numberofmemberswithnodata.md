---
title: NumberOfMembersWithNoData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersWithNoData
api_type:
- schema
ms.assetid: 7ca9c57c-9519-442c-a9f4-dca2b0309716
description: Das Element NumberOfMembersWithNoData stellt die Anzahl der Mitglieder der Verteilerliste, die nicht veröffentlichte Frei/Gebucht-Daten mit einer vorgeschlagenen Besprechung Uhrzeit verglichen verfügen. Dieses Element stellt die Mitglieder von Verteilerlisten, die zu groß ist oder Mitglieder, die keine Daten Status aufweisen.
ms.openlocfilehash: f73978df47bd8240dd5dabfbbf74523525e3270f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830637"
---
# <a name="numberofmemberswithnodata"></a>NumberOfMembersWithNoData

Das Element **NumberOfMembersWithNoData** stellt die Anzahl der Mitglieder der Verteilerliste, die nicht veröffentlichte Frei/Gebucht-Daten mit einer vorgeschlagenen Besprechung Uhrzeit verglichen verfügen. Dieses Element stellt die Mitglieder von Verteilerlisten, die zu groß ist oder Mitglieder, die **Keine Daten** Status aufweisen. 
  
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
|[GroupAttendeeConflictData](groupattendeeconflictdata.md) <br/> |Enthält Konfliktinformationen über die Anzahl der Benutzer, die verfügbar sind, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die nicht zu Ihrer Verfügbarkeit einsehen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit verfügen aggregierte.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a>Hinweise

Ein Kontakt in einer Gruppe, die nicht über ein Postfach verfügt ist ein Beispiel eines Mitglieds der Verteilergruppe, das Kalenderdaten nicht vorhanden ist. Ein Kontakt möglicherweise auch **Ohne Daten** Status aus den folgenden Gründen: 
  
- Berechtigungen sind nicht ausreichend.
    
- Die Verteilerliste ist zu groß, um zu erweitern.
    
- Der Active Directory-Dienst ist nicht verfügbar.
    
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

