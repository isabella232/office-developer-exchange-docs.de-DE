---
title: Updates (Element)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: Das Updates-Element enthält eine Reihe von Elementen, die Anfüge-, Festlegen- und Löschen-Änderungen an Elementeigenschaften definieren.
ms.openlocfilehash: b4a343d941d29e9b25ebedfbf25894c7ec9b22d7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517406"
---
# <a name="updates-item"></a>Updates (Element)

Das  Updates-Element enthält eine Reihe von Elementen, die Anfüge-, Festlegen- und Löschen-Änderungen an Elementeigenschaften definieren. 
  
- [UpdateItem](updateitem.md)
  
- [ItemChanges](itemchanges.md)
  
- [ItemChange](itemchange.md)
  
- [Updates (Element)](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

**NonEmptyArrayOfItemChangeDescriptionsType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToItemField](appendtoitemfield.md) <br/> |Stellt Daten dar, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements angefügt werden sollen.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines [UpdateItem-Vorgangs](updateitem-operation.md)dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |Enthält einen Elementbezeichner und die Aktualisierungen, die auf das Element angewendet werden sollen.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typenschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateItem-Vorgang](updateitem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

