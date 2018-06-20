---
title: SuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionQuality
api_type:
- schema
ms.assetid: 734f1a58-adda-4830-973e-e84bf7b870d5
description: Das SuggestionQuality-Element darstellt, die Qualität der vorgeschlagenen Besprechungszeit.
ms.openlocfilehash: e67e0149226b36c22cdd00acd78f6582f826dd3e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839136"
---
# <a name="suggestionquality"></a>SuggestionQuality

Das **SuggestionQuality** -Element darstellt, die Qualität der vorgeschlagenen Besprechungszeit. 
  
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
|[Vorschlag](suggestion.md) <br/> |Stellt ein einzelnes meeting Zeit Vorschlag.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen **SuggestionQuality** Wert darstellt, ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt: 
  
- **Hervorragend** 100 Prozent der Benutzer und Ressourcen stehen für die Uhrzeit der vorgeschlagenen Besprechung. 
    
- **Eine gute** Der minimale Prozentsatz der Benutzer und Ressourcen verfügbar ist gleich oder größer als die [GoodThreshold](goodthreshold.md) -Elementwert plus 50. 
    
- **Fair** Der maximale Prozentsatz von Benutzern und Ressourcen für einen Zeitraum vorgeschlagenen Besprechung zur Verfügung entspricht dem Elementwert [GoodThreshold](goodthreshold.md) plus 50. Der Mindestwert für eine **angemessene** Qualität Besprechungszeit ist 50 Prozent. 
    
- **Schlechte** Weniger als 50 Prozent der Benutzer und Ressourcen stehen für die Uhrzeit der vorgeschlagenen Besprechung zur Verfügung. 
    
## <a name="remarks"></a>Hinweise

Die **SuggestionQuality** ist auch der Typ für die [DayQuality](dayquality.md) und die [MinimumSuggestionQuality](minimumsuggestionquality.md) Elemente. 
  
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

