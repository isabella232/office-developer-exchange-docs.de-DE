---
title: Aktion (ConversationActionTypeType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Action
api_type:
- schema
ms.assetid: 8bbc12f2-76c5-4fda-828f-56b2086a0454
description: Das Action-Element enthält die Aktion, die für die vom ConversationId-Element angegebene Unterhaltung ausgeführt werden soll.
ms.openlocfilehash: e75d9d5df75894d1de9831b0022269e7ace4fa63
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514893"
---
# <a name="action-conversationactiontypetype"></a>Aktion (ConversationActionTypeType)

Das Action-Element enthält die Aktion, die für die vom [ConversationId-Element](conversationid.md) angegebene Unterhaltung ausgeführt werden soll.  
  
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
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **Action-Elements** gibt an, welche Aktion für eine Unterhaltung ausgeführt wird. Es folgen die möglichen Textwerte und die entsprechenden Aktionen: 
  
- **AlwaysCategorize** – Die aktuellen und neuen Elemente in der Unterhaltung werden automatisch mit den Kategorien festgelegt, die im [Categories-Element](categories-ex15websvcsotherref.md) identifiziert werden. 
    
- **AlwaysDelete** – Die aktuellen und neuen Elemente in der Unterhaltung werden automatisch gelöscht. Der Löschmodus wird durch das [DeleteType-Element](deletetype.md) festgelegt. 
    
- **AlwaysMove** – Die aktuellen und neuen Elemente in der Unterhaltung werden automatisch in den Ordner verschoben, der vom [DestinationFolderId-Element](destinationfolderid.md) identifiziert wird. 
    
- **Löschen** – Die aktuellen Elemente in der Unterhaltung werden gelöscht. Nachfolgende Elemente in der Unterhaltung werden nicht gelöscht. Der Löschmodus wird durch das [DeleteType-Element](deletetype.md) festgelegt. 
    
- **Verschieben** – Die aktuellen Elemente in der Unterhaltung werden in den ordner verschoben, der durch das [DestinationFolderId-Element](destinationfolderid.md) identifiziert wird. Nachfolgende Elemente in der Unterhaltung werden nicht verschoben. 
    
- **Kopieren** – Die aktuellen Elemente in der Unterhaltung werden in den ordner kopiert, der durch das [DestinationFolderId-Element](destinationfolderid.md) identifiziert wird. Nachfolgende Elemente in der Unterhaltung werden nicht kopiert. 
    
- **SetReadState** : Für die aktuellen Elemente in der Unterhaltung wird der Lesestatus festgelegt. Der Lesestatus wird durch das [IsRead-Element](isread.md) festgelegt. 
    
- **Flag** – Für die aktuellen Elemente in der Unterhaltung wird ein Kennzeichen festgelegt, wie durch das [Flag-Element](flag.md) definiert. 
    
## <a name="remarks"></a>HinwBemerkungeneise

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

