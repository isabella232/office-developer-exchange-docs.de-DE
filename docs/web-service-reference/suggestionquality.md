---
title: SuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SuggestionQuality
api_type:
- schema
ms.assetid: 734f1a58-adda-4830-973e-e84bf7b870d5
description: Das SuggestionQuality-Element stellt die Qualität der vorgeschlagenen Besprechungszeit dar.
ms.openlocfilehash: 4d8a504e60e8f043bfb120080a89733e78b16b9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531552"
---
# <a name="suggestionquality"></a>SuggestionQuality

Das **SuggestionQuality-Element** stellt die Qualität der vorgeschlagenen Besprechungszeit dar. 
  
[GetUserAvailabilityResponse](getuseravailabilityresponse.md)
  
[SuggestionsResponse](suggestionsresponse.md)
  
[SuggestionDayResultArray](suggestiondayresultarray.md)
  
[SuggestionDayResult](suggestiondayresult.md)
  
[SuggestionArray](suggestionarray.md)
  
[Vorschlag](suggestion.md)
  
[SuggestionQuality](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 **SuggestionQuality**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Vorschlag](suggestion.md) <br/> |Stellt einen einzelnen Besprechungszeitvorschlag dar.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen **SuggestionQuality-Wert** darstellt, ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt: 
  
- **Hervorragende** 100 Prozent der Benutzer und Ressourcen sind für die vorgeschlagene Besprechungszeit verfügbar. 
    
- **Gut** Der Mindestprozentsatz der verfügbaren Benutzer und Ressourcen ist gleich oder größer als der Wert des [GoodThreshold-Elements](goodthreshold.md) plus 50. 
    
- **Fair** Der maximale Prozentsatz der Benutzer und Ressourcen, die für eine vorgeschlagene Besprechungszeit verfügbar sind, entspricht dem Wert des [GoodThreshold-Elements](goodthreshold.md) plus 50. Der Mindestwert für eine **Besprechungszeit mit fairer** Qualität beträgt 50 Prozent. 
    
- **Schlecht** Weniger als 50 Prozent der Benutzer und Ressourcen sind für die vorgeschlagene Besprechungszeit verfügbar. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Der **SuggestionQuality-Typ** ist auch der Typ für die [Elemente DayQuality](dayquality.md) und [MinimumSuggestionQuality.](minimumsuggestionquality.md) 
  
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

