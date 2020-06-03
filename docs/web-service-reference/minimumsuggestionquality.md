---
title: MinimumSuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MinimumSuggestionQuality
api_type:
- schema
ms.assetid: 3725cbd4-9bc1-4f7d-8929-b2c68cb46114
description: Das MinimumSuggestionQuality-Element definiert die Qualität von Besprechungs Vorschlägen, die in der Antwort zurückgegeben werden sollen.
ms.openlocfilehash: c85cbf65a63ac0b09408c14e01889f97a05b27b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467480"
---
# <a name="minimumsuggestionquality"></a>MinimumSuggestionQuality

Das **MinimumSuggestionQuality** -Element definiert die Qualität von Besprechungs Vorschlägen, die in der Antwort zurückgegeben werden sollen. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[MinimumSuggestionQuality](minimumsuggestionquality.md)
  
```xml
<MinimumSuggestionQuality>...</MinimumSuggestionQuality>
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
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt:
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|**Hervorragend** <br/> |0% der Teilnehmer haben einen Konflikt mit der vorgeschlagenen Besprechungszeit.  <br/> |
|**Gut** <br/> |Der Prozentsatz, der als "gut" gilt, wird mithilfe des [GoodThreshold](goodthreshold.md) -Elements festgelegt.  <br/> |
|**Messe** <br/> |Der Prozentsatz, der als fair betrachtet wird, wird mithilfe des [GoodThreshold](goodthreshold.md) -Elements festgelegt.  <br/> |
|**mangelhaft** <br/> |50% oder mehr der Teilnehmer haben einen Konflikt mit der vorgeschlagenen Besprechungszeit.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetUserAvailability-Vorgang](getuseravailability-operation.md)


[Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

