---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: Das ItemChange-Element enthält eine Element-ID und die Updates auf das Element anwenden.
ms.openlocfilehash: 42484c8deecb106e05023215342af3c7d996d852
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353511"
---
# <a name="itemchange"></a>ItemChange

Das **ItemChange** -Element enthält eine Element-ID und die Updates auf das Element anwenden. 
  
- [UpdateItem](updateitem.md) 
- [ItemChanges](itemchanges.md)
- [ItemChange](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

**ItemChangeType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher. Dieses Element ist erforderlich, wenn das Element [OccurrenceItemId](occurrenceitemid.md) oder [RecurringMasterItemId](recurringmasteritemid.md) nicht verwendet wird.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Gibt ein einzelnes Vorkommen des eine Terminserie. Dieses Element ist erforderlich, wenn verwendet. Dieses Element ist erforderlich, wenn das Element [RecurringMasterItemId](recurringmasteritemid.md) oder [ItemId](itemid.md) nicht verwendet wird.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Gibt ein Master-Shape Recurrence-Element durch das Identifizieren von seine Vorkommen verwandte Elemente-Bezeichner. Dieses Element ist erforderlich, wenn verwendet. Dieses Element ist erforderlich, wenn das Element [OccurrenceItemId](occurrenceitemid.md) oder [ItemId](itemid.md) nicht verwendet wird.  <br/> |
|[Updates (Element)](updates-item.md) <br/> |Enthält ein Array, definiert anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Enthält ein Array von [ItemChange](itemchange.md) -Elementen, die Elemente und die Updates auf Elemente anwenden zu identifizieren.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>Hinweise

In einem **ItemChange** -Element kann nur ein einzelnes Element [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)oder [RecurringMasterItemId](recurringmasteritemid.md) verwendet werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateItem-Vorgang](updateitem-operation.md)

