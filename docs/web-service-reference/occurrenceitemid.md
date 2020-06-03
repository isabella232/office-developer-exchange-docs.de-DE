---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: Das OccurrenceItemId-Element identifiziert ein einzelnes Vorkommen eines wiederkehrenden Elements.
ms.openlocfilehash: 37c3a2442afb3302bca88ef0301e98013ff0319b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468376"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

Das **OccurrenceItemId** -Element identifiziert ein einzelnes Vorkommen eines wiederkehrenden Elements. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Gibt den wiederkehrenden Master eines wiederkehrenden Elements an. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Gibt eine bestimmte Version des wiederkehrenden Masters oder ein Element Vorkommen an. Wenn sich entweder der wiederkehrende Master oder eines seiner vorkommen ändert, ändert sich die **ChangeKey** . Die **ChangeKey** ist für den wiederkehrenden Master und alle Vorkommen identisch.  <br/> |
|**InstanceIndex** <br/> |Gibt den Index des Element Vorkommens an. Dieses Attribut ist erforderlich. Dieser Wert stellt eine ganze Zahl dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[ItemIds](itemids.md) <br/> | Enthält die eindeutigen Identitäten von Elementen, Element Elementen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden. <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**Hinweis**: der [MoveItem-Vorgang](moveitem-operation.md) und der CopyItem- [Vorgang](copyitem-operation.md) funktionieren nur mit einzelnen Kalenderelementen und wiederkehrenden Master Elementen. Element vorkommen sind bei diesen Vorgängen ungültig.           |
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das vierte Vorkommen eines wiederkehrenden Elements identifiziert, das über die Identität 34vswe4 verfügt.
  
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

