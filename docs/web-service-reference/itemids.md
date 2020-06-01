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
description: Das itemids-Element enthält die eindeutigen Identitäten von Elementen, vorkommen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.
ms.openlocfilehash: bbd594ce2610bd625b0e16a0383fda552ee9eb19
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460603"
---
# <a name="itemids"></a>ItemIds
  
Das **itemids** -Element enthält die eindeutigen Identitäten von Elementen, vorkommen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.
  
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
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Gibt ein einzelnes Vorkommen eines wiederkehrenden Elements an.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifiziert ein Serienmasterelement durch Identifizieren eines der Bezeichner des zugehörigen vorkommen Elements.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Definiert eine Anforderung zum Löschen von Elementen im Exchange-Informationsspeicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |Das Stammelement, das eine Anforderung zum Senden von Elementen im Exchange-Informationsspeicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Definiert eine Anforderung zum Abrufen von Elementen aus dem Exchange-Informationsspeicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung zum verlagern von Elementen im Exchange-Informationsspeicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung zum Kopieren von Elementen in der Exchange-Informationsspeicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteItem-Operation](deleteitem-operation.md)
- [SendItem-Vorgang](senditem-operation.md) 
- [GetItem-Vorgang](getitem-operation.md)
- [MoveItem-Vorgang](moveitem-operation.md)
- [CopyItem-Vorgang](copyitem-operation.md)
- [FindConversation-Vorgang](findconversation-operation.md)

