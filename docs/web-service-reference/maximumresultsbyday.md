---
title: MaximumResultsByDay
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MaximumResultsByDay
api_type:
- schema
ms.assetid: d581a12a-2b8e-4960-ae14-c8c4aa0b1849
description: Das MaximumResultsByDay-Element gibt die Anzahl der vorgeschlagenen Besprechungszeiten pro Tag an, die in der Antwort zurückgegeben werden.
ms.openlocfilehash: 6a355843e3c4a6b5ce20f812b4eb9bcc7a3283bc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523933"
---
# <a name="maximumresultsbyday"></a>MaximumResultsByDay

Das **MaximumResultsByDay-Element** gibt die Anzahl der vorgeschlagenen Besprechungszeiten pro Tag an, die in der Antwort zurückgegeben werden. 
  
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
|[SuggestionsViewOptions](suggestionsviewoptions.md) <br/> |Enthält die Optionen zum Abrufen von Besprechungsvorschlagsinformationen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt eine ganze Zahl dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions-Element](suggestionsviewoptions.md) verwendet wird. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft ausgeführt wird® Exchange Server 2007, auf dem die Clientzugriffsserverrolle installiert ist. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

