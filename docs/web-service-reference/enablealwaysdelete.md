---
title: EnableAlwaysDelete
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EnableAlwaysDelete
api_type:
- schema
ms.assetid: 7753aec5-3f93-4aeb-a28e-8b9b42ca7f9b
description: Das EnableAlwaysDelete-Element gibt eine Kennung, die für alle neuen Elemente in einer Unterhaltung löschen kann.
ms.openlocfilehash: f86765c641604afbf13ac962f4b34fbd8de56200
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758220"
---
# <a name="enablealwaysdelete"></a>EnableAlwaysDelete

Das **EnableAlwaysDelete** -Element gibt eine Kennung, die für alle neuen Elemente in einer Unterhaltung löschen kann. 
  
[ApplyConversationAction](applyconversationaction.md)
  
[ConversationActions](conversationactions.md)
  
[ConversationAction](conversationaction.md)
  
[EnableAlwaysDelete](enablealwaysdelete.md)
  
```XML
<EnableAlwaysDelete/>
```

 **xs: Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **EnableAlwaysDelete** -Elements ist **true,** um das Löschen aller Elemente in der Unterhaltung zu aktivieren. anderenfalls **false**.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)

