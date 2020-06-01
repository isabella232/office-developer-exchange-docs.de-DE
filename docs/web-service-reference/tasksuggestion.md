---
title: TaskSuggestion
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ade9ea3b-bdf1-4999-ac7d-44c6452cef36
description: Das Task suggestion-Element enthält einen vorgangsvorschlag, der aus einer Entität resultierte, die aus einem Element extrahiert wurde.
ms.openlocfilehash: 49564c246596dabbf7fbacf2924eeb877698ea1a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468124"
---
# <a name="tasksuggestion"></a>TaskSuggestion

Das **Task Suggestion** -Element enthält einen vorgangsvorschlag, der aus einer Entität resultierte, die aus einem Element extrahiert wurde. 
  
```XML
<TaskSuggestion>
   <Position/>
   <TaskString/>
   <Assignees/>
</TaskSuggestion>
```

**TaskSuggestionType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Position](position.md)  |  [Task String](taskstring.md)  |  [Empfänger](assignees.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[TaskSuggestions](tasksuggestions.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

