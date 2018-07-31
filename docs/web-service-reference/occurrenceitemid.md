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
description: Das OccurrenceItemId-Element gibt ein einzelnes Vorkommen des eine Terminserie.
ms.openlocfilehash: 073639ecbca6ffda872e9253b7c7e44c3541f13b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353462"
---
# <a name="occurrenceitemid"></a>OccurrenceItemId

Das **OccurrenceItemId** -Element gibt ein einzelnes Vorkommen des eine Terminserie. 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

**OccurrenceItemIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**RecurringMasterId** <br/> |Identifiziert den wiederkehrenden Master-Objekt vom eine Terminserie. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Identifiziert eine bestimmte Version von sich wiederholenden Master oder ein Element vorkommen. Wenn das wiederkehrende Master-Shape oder eine der Vorkommen ändern, ändert sich der **ChangeKey** . Die **ChangeKey** entspricht der Vorgehensweise für das wiederkehrende Master-Shape und alle Vorkommen.  <br/> |
|**InstanceIndex** <br/> |Den Index des Vorkommens Element identifiziert. Dieses Attribut ist erforderlich. Dieser Wert gibt eine ganze Zahl.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.  <br/> |
|[ItemIds](itemids.md) <br/> | Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher. <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/>**Hinweis**: [MoveItem-Vorgang](moveitem-operation.md) und einen optimalen [Betrieb CopyItem](copyitem-operation.md) nur arbeiten mit einzelnen Kalenderelemente und Terminserien Master-Shape. Element vorkommen sind mit diesen Verfahren ungültig.           |
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates auf das Element anwenden.<br/><br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel identifiziert das vierte Vorkommen eines sich wiederholenden-Elements, das die Identität 34vswe4 verfügt.
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [RecurringMasterItemId](recurringmasteritemid.md)
- [FindConversation-Vorgang](findconversation-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

