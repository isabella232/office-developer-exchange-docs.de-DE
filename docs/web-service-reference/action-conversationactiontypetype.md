---
title: Aktion (ConversationActionTypeType)
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
description: Das Action-Element enthält die Aktion auf die Unterhaltung vom ConversationId-Element angegeben.
ms.openlocfilehash: b468eeaf0c2509bfa53cbd83f497f0bae20a7f68
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757207"
---
# <a name="action-conversationactiontypetype"></a>Aktion (ConversationActionTypeType)

Das **Action** -Element enthält die Aktion auf die Unterhaltung vom [ConversationId](conversationid.md) -Element angegeben. 
  
- [ApplyConversationAction](applyconversationaction.md)
  
- [ConversationActions](conversationactions.md)
  
- [ConversationAction](conversationaction.md)
  
- [Aktion (ConversationActionTypeType)](action-conversationactiontypetype.md)
  
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
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion auf einem einzelnen Gespräch angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Action** -Elements gibt an, welche Aktion für eine Unterhaltung ausgeführt wird. Im folgenden sind die möglichen Textwerte und die entsprechenden Aktionen: 
  
- **AlwaysCategorize** - die aktuelle und neue Elemente in der Unterhaltung wird automatisch mit den Kategorien in der [Categories](categories-ex15websvcsotherref.md) -Element identifiziert festgelegt. 
    
- **AlwaysDelete** - die aktuelle und neue Elemente in der Unterhaltung werden automatisch gelöscht werden. Der Modus Löschung wird vom [DeleteType](deletetype.md) -Element festgelegt. 
    
- **AlwaysMove** - die aktuelle und neue Elemente in der Unterhaltung wird automatisch in den Ordner vom [DestinationFolderId](destinationfolderid.md) -Element identifiziert verschoben werden. 
    
- **Löschen** – der aktuelle Elemente in der Unterhaltung wird gelöscht. Nachfolgende Elemente in der Unterhaltung werden nicht gelöscht werden. Der Modus Löschung wird vom [DeleteType](deletetype.md) -Element festgelegt. 
    
- **Verschieben** - aktuelle Elemente in der Unterhaltung werden in den Ordner, der durch das [DestinationFolderId](destinationfolderid.md) -Element identifiziert verschoben. Nachfolgende Elemente in der Unterhaltung werden nicht verschoben werden. 
    
- **Kopieren** - die aktuelle Elemente in der Unterhaltung werden in den Ordner, der durch das [DestinationFolderId](destinationfolderid.md) -Element identifiziert kopiert. Nachfolgende Elemente in der Unterhaltung werden nicht kopiert. 
    
- **SetReadState** - die aktuelle Elemente in der Unterhaltung müssen ihre Zustand "gelesen" festgelegt. Der Zustand "gelesen" wird durch das [IsRead](isread.md) -Element festgelegt. 
    
- **Flag** - aktuelle Elemente in der Unterhaltung wird ein Flag gesetzt, das durch das Element [Flag](flag.md) festgelegt haben. 
    
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

- [ApplyConversationAction-Vorgang](applyconversationaction-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

