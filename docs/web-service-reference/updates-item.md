---
title: Updates (Element)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: Updates-Element enthält eine Reihe von Elementen, die definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.
ms.openlocfilehash: 13df458c783b942e1c868853c41b6247119cf123
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839402"
---
# <a name="updates-item"></a>Updates (Element)

**Updates** -Element enthält eine Reihe von Elementen, die definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften. 
  
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
|[AppendToItemField](appendtoitemfield.md) <br/> |Stellt Daten anfügen an eine einzelne Eigenschaft eines Elements während einer [UpdateItem Vorgang](updateitem-operation.md)dar.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[DeleteItemField](deleteitemfield.md) <br/> |Stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während einer [UpdateItem Vorgang](updateitem-operation.md)dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates auf das Element anwenden.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="remarks"></a>Hinweise

Die Updates, die von diesem Element definiert sind werden für das Element ausgeführt, die durch die Elemente [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)oder [RecurringMasterItemId](recurringmasteritemid.md) identifiziert wird. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typen-schema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateItem Operation](updateitem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

