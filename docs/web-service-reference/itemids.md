---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: Das Artikelnummern ein.-Element enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.
ms.openlocfilehash: 1bd4d6f4593a7c3b418561269d8b29707cc6030c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830155"
---
# <a name="itemids"></a>ItemIds
  
Das **Artikelnummern ein.** -Element enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

**NonEmptyArrayOfBaseItemIdsType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert. 
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Gibt ein einzelnes Vorkommen des eine Terminserie.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Gibt ein Master-Shape Recurrence-Element durch das Identifizieren von seine Vorkommen verwandte Elemente-Bezeichner.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Definiert eine Anforderung zum Löschen von Elementen im Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |Das Stammelement, das eine Anforderung zum Senden von Elementen im Exchange-Speicher definiert.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Definiert eine Anforderung zum Abrufen von Elementen aus dem Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung an die Elemente im Exchange-Speicher zu verschieben.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung zum Kopieren von Elementen im Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteItem-Operation](deleteitem-operation.md)
- [SendItem Operation](senditem-operation.md) 
- [GetItem Operation](getitem-operation.md)
- [MoveItem Operation](moveitem-operation.md)
- [CopyItem Operation](copyitem-operation.md)
- [FindConversation Operation](findconversation-operation.md)

