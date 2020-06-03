---
title: MaximumResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MaximumResultsByDay
api_type:
- schema
ms.assetid: d581a12a-2b8e-4960-ae14-c8c4aa0b1849
description: Das MaximumResultsByDay-Element gibt die Anzahl der vorgeschlagenen Besprechungszeiten pro Tag an, die in der Antwort zurückgegeben werden.
ms.openlocfilehash: 46d5c35a83034b8b968901fbc4ee57d046b6c164
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468418"
---
# <a name="maximumresultsbyday"></a>MaximumResultsByDay

Das **MaximumResultsByDay** -Element gibt die Anzahl der vorgeschlagenen Besprechungszeiten pro Tag an, die in der Antwort zurückgegeben werden. 
  
[GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
[SuggestionsViewOptions](suggestionsviewoptions.md)
  
[MaximumResultsByDay](maximumresultsbyday.md)
  
```xml
<MaximumResultsByDay>...</MaximumResultsByDay>
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
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert Text stellt eine ganze Zahl dar.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft® Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

