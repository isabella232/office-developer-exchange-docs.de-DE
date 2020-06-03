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
description: Das RecurringMasterItemId-Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines der zugehörigen vorkommen Elemente.
ms.openlocfilehash: 896a9ce95d619e7bb44c8158288bc4f62ce417d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529882"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

Das **RecurringMasterItemId** -Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines der zugehörigen vorkommen Elemente. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**OccurrenceId** <br/> |Gibt ein einzelnes Vorkommen eines wiederkehrenden Hauptelements an. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Gibt eine bestimmte Version eines einzelnen Auftretens eines wiederkehrenden Hauptelements an. Darüber hinaus wird das wiederkehrende Hauptelement ebenfalls identifiziert, da es und das einzelne Vorkommen denselben Änderungsschlüssel enthalten werden. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[ItemChange](itemchange.md) <br/> |Enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen. <br/> <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:  <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Enthält die eindeutigen Identitäten von Elementen, Element Elementen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das wiederkehrende masterelement identifiziert, indem eines seiner vorkommen mit dem Bezeichner 56lkjh6 identifiziert wird.
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [OccurrenceItemId](occurrenceitemid.md)
- [FindConversation-Vorgang](findconversation-operation.md)

