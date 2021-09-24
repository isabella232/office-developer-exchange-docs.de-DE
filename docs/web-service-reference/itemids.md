---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: Das ItemIds-Element enthält die eindeutigen Identitäten von Elementen, Vorkommenselementen und wiederkehrenden Masterelementen, die zum Löschen, Senden, Abrufen, Verschieben oder Kopieren von Elementen im Exchange Speicher verwendet werden.
ms.openlocfilehash: 7341b8214b4d61564bd87707a9d8c76fbca07628
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522887"
---
# <a name="itemids"></a>ItemIds
  
Das **ItemIds-Element** enthält die eindeutigen Identitäten von Elementen, Vorkommenselementen und wiederkehrenden Masterelementen, die zum Löschen, Senden, Abrufen, Verschieben oder Kopieren von Elementen im Exchange Speicher verwendet werden.
  
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
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements im Exchange Speicher.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifiziert ein einzelnes Vorkommen einer Terminserie.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifiziert ein Serienmasterelement, indem einer seiner zugehörigen Bezeichner für vorkommende Elemente identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
|[DeleteItem](deleteitem.md) <br/> |Definiert eine Anforderung zum Löschen von Elementen im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/DeleteItem` <br/> |
|[SendItem](senditem.md) <br/> |Das Stammelement, das eine Anforderung zum Senden von Elementen im Exchange Speicher definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/SendItem` <br/> |
|[GetItem](getitem.md) <br/> |Definiert eine Anforderung zum Abrufen von Elementen aus dem Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/GetItem` <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung zum Verschieben von Elementen im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung zum Kopieren von Elementen im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteItem-Vorgang](deleteitem-operation.md)
- [SendItem-Vorgang](senditem-operation.md) 
- [GetItem-Vorgang](getitem-operation.md)
- [MoveItem-Vorgang](moveitem-operation.md)
- [CopyItem-Vorgang](copyitem-operation.md)
- [FindConversation-Vorgang](findconversation-operation.md)

