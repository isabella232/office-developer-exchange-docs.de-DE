---
title: Action (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: Das Action-Element enthält die Aktion, die für die durch das Conversation-Element angegebene Konversation ausgeführt werden soll.
ms.openlocfilehash: f97b04b98cdc29bee9aff5fa1fc6f37400b8314c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527544"
---
# <a name="action-conversationactiontypetype"></a>Action (ConversationActionTypeType)

Das **Action** -Element enthält die Aktion, die für die durch das [Conversation](conversationid.md) -Element angegebene Konversation ausgeführt werden soll. 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [Unterhaltung](conversationaction.md)
  
- [Action (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
```XML
<Action> AlwaysCategorize | AlwaysDelete | AlwaysMove | Delete | Move | Copy | SetReadState </Action>
```

 **ConversationActionTypeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung](conversationaction.md) <br/> |Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Action** -Elements gibt an, welche Aktion für eine Unterhaltung ausgeführt wird. Im folgenden sind die möglichen Text Werte und die entsprechenden Aktionen: 
  
- **AlwaysCategorize** – die aktuellen Elemente und neuen Elemente in der Unterhaltung werden automatisch mit den Kategorien festgelegt, die im [Categories](categories-ex15websvcsotherref.md) -Element angegeben sind. 
    
- **Alwaysdeleteolalwaysdelete** – die aktuellen Elemente und neuen Elemente in der Unterhaltung werden automatisch gelöscht. Der Löschmodus wird durch das [deleteType](deletetype.md) -Element festgelegt. 
    
- **AlwaysMove** – die aktuellen Elemente und neuen Elemente in der Unterhaltung werden automatisch in den Ordner verschoben, der durch das [DestinationFolderId](destinationfolderid.md) -Element identifiziert wird. 
    
- **Delete** – die aktuellen Elemente in der Unterhaltung werden gelöscht. Nachfolgende Elemente in der Unterhaltung werden nicht gelöscht. Der Löschmodus wird durch das [deleteType](deletetype.md) -Element festgelegt. 
    
- **Move** – die aktuellen Elemente in der Unterhaltung werden in den durch das [DestinationFolderId](destinationfolderid.md) -Element identifizierten Ordner verschoben. Nachfolgende Elemente in der Unterhaltung werden nicht verschoben. 
    
- **Copy** – die aktuellen Elemente in der Unterhaltung werden in den durch das [DestinationFolderId](destinationfolderid.md) -Element identifizierten Ordner kopiert. Nachfolgende Elemente in der Unterhaltung werden nicht kopiert. 
    
- **SetReadState** – für die aktuellen Elemente in der Unterhaltung ist der Lesestatus festgelegt. Der Read-Zustand wird durch das [isread](isread.md) -Element festgelegt. 
    
- **Flag** – für die aktuellen Elemente in der Unterhaltung wird ein Flag festgelegt, das durch das [Flag](flag.md) -Element definiert ist. 
    
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ApplyConversationAction-Vorgang](applyconversationaction-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

