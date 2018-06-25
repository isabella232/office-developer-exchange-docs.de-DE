---
title: DetailedSuggestionsWindow
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DetailedSuggestionsWindow
api_type:
- schema
ms.assetid: 7b348d63-6a7d-45f4-9562-5c42243d63a5
description: Das DetailedSuggestionsWindow-Element gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird.
ms.openlocfilehash: 8a3af0178d0c96b50f4dd641716a9f7a7be8f7a2
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757966"
---
# <a name="detailedsuggestionswindow"></a>DetailedSuggestionsWindow

Das **DetailedSuggestionsWindow** -Element gibt die Zeitspanne, die ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt wird. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md) 
- [SuggestionsViewOptions](suggestionsviewoptions.md) 
- [DetailedSuggestionsWindow](detailedsuggestionswindow.md)
  
```xml
<DetailedSuggestionsWindow>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
</DetailedSuggestionsWindow>
```

 **Duration**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTime](starttime.md) <br/> |Stellt den Anfang des Zeitraums ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt.  <br/> |
|[EndTime](endtime.md) <br/> |Stellt das Ende des Zeitraums ausführliche Informationen zum vorgeschlagenen Besprechungszeiten abgefragt.  <br/> |
   
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

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

