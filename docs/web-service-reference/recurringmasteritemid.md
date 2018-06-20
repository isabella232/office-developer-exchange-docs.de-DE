---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: Das RecurringMasterItemId-Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen.
ms.openlocfilehash: ae59e33ece55d85435ece4c9030ccda32eb62eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831015"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

Das **RecurringMasterItemId** -Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**OccurrenceId** <br/> |Gibt ein einzelnes Vorkommen des ein wiederkehrendes master-Objekt. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Identifiziert eine bestimmte Version für ein einzelnes Auftreten eines sich wiederholenden master-Elements an. Darüber hinaus wird wiederkehrenden master-Objekts auch identifiziert, da es und die einzelnen Vorkommen der gleichen Änderungsschlüssel enthalten. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.  <br/> |
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates auf das Element anwenden. <br/> <br/> Es folgt der XPath-Ausdruck, der dieses Element: <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[Artikelnummern ein.](itemids.md) <br/> | Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Das folgende Beispiel identifiziert die wiederkehrenden master-Objekts durch das Identifizieren von eine der Vorkommen mit der ID 56lkjh6.
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [OccurrenceItemId](occurrenceitemid.md)
- [FindConversation Operation](findconversation-operation.md)

