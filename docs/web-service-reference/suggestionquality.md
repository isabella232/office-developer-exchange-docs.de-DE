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
description: Das SuggestionQuality-Element stellt die Qualität der vorgeschlagenen Besprechungszeit dar.
ms.openlocfilehash: 3f8c15ccabd03687dc386a0328020cbc0bc802c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44457977"
---
# <a name="suggestionquality"></a>SuggestionQuality

Das **SuggestionQuality** -Element stellt die Qualität der vorgeschlagenen Besprechungszeit dar. 
  
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
|[Vorschlag](suggestion.md) <br/> |Stellt einen einzelnen Besprechungszeit Vorschlag dar.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen **SuggestionQuality** -Wert darstellt, ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt: 
  
- **Ausgezeichnete** 100% der Benutzer und Ressourcen sind für die vorgeschlagene Besprechungszeit verfügbar. 
    
- **Guten** Der minimale Prozentsatz der verfügbaren Benutzer und Ressourcen ist größer oder gleich dem Wert des [GoodThreshold](goodthreshold.md) -Elements plus 50. 
    
- **Fair** Der maximale Prozentsatz an Benutzern und Ressourcen, die für eine vorgeschlagene Besprechungszeit zur Verfügung stehen, entspricht dem Wert des [GoodThreshold](goodthreshold.md) -Elements plus 50. Der Mindestwert für eine Besprechungszeit in **angemessener** Qualität beträgt 50 Prozent. 
    
- **Schlecht** Weniger als 50 Prozent der Benutzer und Ressourcen stehen für die vorgeschlagene Besprechungszeit zur Verfügung. 
    
## <a name="remarks"></a>Bemerkungen

Der **SuggestionQuality** -Typ ist auch der Typ für die [DayQuality](dayquality.md) und die [MinimumSuggestionQuality](minimumsuggestionquality.md) -Elemente. 
  
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


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

