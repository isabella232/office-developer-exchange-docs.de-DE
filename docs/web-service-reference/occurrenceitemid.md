---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: Das OccurrenceItemId-Element identifiziert ein einzelnes Vorkommen eines wiederkehrenden Elements.
ms.openlocfilehash: ac6fc081e67f3897880ad30fcc1b62fe2e844459
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515418"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

Das **OccurrenceItemId-Element** identifiziert ein einzelnes Vorkommen eines wiederkehrenden Elements. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Gibt den Serienmaster einer Terminserie an. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Identifiziert eine bestimmte Version des Serienmasters oder eines Elementvorkommens. Wenn sich der Serienmaster oder eines seiner Vorkommen ändert, wird der **ChangeKey** geändert. The **ChangeKey** is the same for the recurring master and all occurrences.  <br/> |
|**InstanceIndex** <br/> |Gibt den Index des Elementvorkommens an. Dieses Attribut ist erforderlich. Dieser Wert stellt eine ganze Zahl dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Elementbezeichnern für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[ItemIds](itemids.md) <br/> | Enthält die eindeutigen Identitäten von Elementen, Vorkommenselementen und wiederkehrenden Masterelementen, die zum Löschen, Senden, Abrufen, Verschieben oder Kopieren von Elementen im Exchange Speicher verwendet werden. <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**HINWEIS:** [MoveItem-Vorgang](moveitem-operation.md) und [CopyItem-Vorgang](copyitem-operation.md) funktionieren nur mit einzelnen Kalenderelementen und wiederkehrenden Masterelementen. Elementvorkommen sind bei diesen Vorgängen ungültig.           |
|[ItemChange](itemchange.md) <br/> |Enthält einen Elementbezeichner und die Aktualisierungen, die auf das Element angewendet werden sollen.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das vierte Vorkommen einer Terminserie mit der Identität 34vswe4 identifiziert.
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [RecurringMasterItemId](recurringmasteritemid.md)
- [FindConversation-Vorgang](findconversation-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

