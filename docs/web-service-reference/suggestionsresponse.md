---
title: SuggestionsResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SuggestionsResponse
api_type:
- schema
ms.assetid: d25ca143-f80c-4458-b669-346fda29a5a7
description: Das SuggestionsResponse-Element enthält Antwortstatusinformationen und Vorschlagsdaten für angeforderte Besprechungsvorschläge.
ms.openlocfilehash: 92dfac3cc0a6ddce9485a8cb266f072795b18bd5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544528"
---
# <a name="suggestionsresponse"></a>SuggestionsResponse

Das **SuggestionsResponse-Element** enthält Antwortstatusinformationen und Vorschlagsdaten für angeforderte Besprechungsvorschläge. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
```xml
<SuggestionsResponse>
   <ResponseMessage>...</ResponseMessage>
   <SuggestionDayResultArray>...</SuggestionDayResultArray>
</SuggestionsResponse>
```

 **SuggestionsResponseType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ResponseMessage](responsemessage.md) <br/> |Enthält beschreibende Informationen zum Antwortstatus.  <br/> |
|[SuggestionDayResultArray](suggestiondayresultarray.md) <br/> |Enthält ein Array von Besprechungsvorschlägen, die nach Datum organisiert sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetUserAvailabilityResponse](getuseravailabilityresponse.md) <br/> |Enthält die Verfügbarkeitsinformationen der angeforderten Benutzer.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist nicht in einer GetUserAvailability-Antwort enthalten, wenn [SuggestionsViewOptions](suggestionsviewoptions.md) nicht in der GetUserAvailability-Anforderungsnachricht festgelegt ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)


[Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

