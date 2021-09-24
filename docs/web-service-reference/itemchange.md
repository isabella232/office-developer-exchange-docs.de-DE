---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: Das ItemChange-Element enthält einen Elementbezeichner und die Aktualisierungen, die auf das Element angewendet werden sollen.
ms.openlocfilehash: 8ace3cf78eb902e48529a0534e39ce7d584bd164
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59537749"
---
# <a name="itemchange"></a>ItemChange

Das **ItemChange-Element** enthält einen Elementbezeichner und die Aktualisierungen, die auf das Element angewendet werden sollen. 
  
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
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements im Exchange Speicher. Dieses Element ist erforderlich, wenn das [OccurrenceItemId-](occurrenceitemid.md) oder [RecurringMasterItemId-Element](recurringmasteritemid.md) nicht verwendet wird.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Identifiziert ein einzelnes Vorkommen einer Terminserie. Dieses Element ist erforderlich, wenn es verwendet wird. Dieses Element ist erforderlich, wenn das [RecurringMasterItemId-](recurringmasteritemid.md) oder [ItemId-Element](itemid.md) nicht verwendet wird.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifiziert ein Serienmasterelement, indem einer seiner zugehörigen Bezeichner für vorkommende Elemente identifiziert wird. Dieses Element ist erforderlich, wenn es verwendet wird. Dieses Element ist erforderlich, wenn das [OccurrenceItemId-](occurrenceitemid.md) oder [ItemId-Element](itemid.md) nicht verwendet wird.  <br/> |
|[Updates (Element)](updates-item.md) <br/> |Enthält ein Array, das Das Anfügen, Festlegen und Löschen von Änderungen an Elementeigenschaften definiert. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Enthält ein Array von [ItemChange-Elementen,](itemchange.md) die Elemente und die Aktualisierungen identifizieren, die auf die Elemente angewendet werden sollen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

In einem **ItemChange-Element** kann nur ein einzelnes [ItemId-,](itemid.md) [OccurrenceItemId-](occurrenceitemid.md)oder [RecurringMasterItemId-Element](recurringmasteritemid.md) verwendet werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateItem-Vorgang](updateitem-operation.md)

