---
title: ConversationActions
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConversationActions
api_type:
- schema
ms.assetid: 3d6c663d-4bd9-4eec-b95a-cd683f592672
description: Das ConversationActions-Element enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden.
ms.openlocfilehash: 3dff7ff66f758f1cd2eb3cd7b8126294d2799fc0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757699"
---
# <a name="conversationactions"></a>ConversationActions

Das **ConversationActions** -Element enthält eine Auflistung von Unterhaltungen und die Aktionen darauf anwenden. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
```XML
<ConversationActions>
   <ConversationAction/>
</ConversationActions>
```

 **NonEmptyArrayOfApplyConversationActionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ApplyConversationAction](applyconversationaction.md) <br/> |Definiert eine Anforderung an die Aktionen auf Elemente in einer Unterhaltung anwenden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)

