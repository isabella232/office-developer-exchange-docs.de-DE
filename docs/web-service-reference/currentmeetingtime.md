---
title: CurrentMeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CurrentMeetingTime
api_type:
- schema
ms.assetid: 1ff68154-24b5-465a-a31c-3d3bab0d491e
description: Das Element CurrentMeetingTime stellt die Anfangszeit der eine Besprechung, die Sie mit einer von einem Besprechungsteilnehmer vorgeschlagenen Besprechungszeit aktualisieren möchten.
ms.openlocfilehash: 88adbe566270d759986e9b55afd4827c0513ca43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757824"
---
# <a name="currentmeetingtime"></a>CurrentMeetingTime

Das Element **CurrentMeetingTime** stellt die Anfangszeit der eine Besprechung, die Sie mit einer von einem Besprechungsteilnehmer vorgeschlagenen Besprechungszeit aktualisieren möchten. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[CurrentMeetingTime](currentmeetingtime.md)
  
```xml
<CurrentMeetingTime>...</CurrentMeetingTime>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Enthält die Optionen zum Abrufen von Besprechungsinformationen Vorschlag.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist nicht erforderlich.
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

