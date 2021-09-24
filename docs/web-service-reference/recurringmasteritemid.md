---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: Das RecurringMasterItemId-Element identifiziert ein Serienmasterelement, indem die Bezeichner eines seiner zugehörigen Vorkommenselemente identifiziert werden.
ms.openlocfilehash: d00794f2b5b1893e1829a3f09df9f3e88266964d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523629"
---
# <a name="recurringmasteritemid"></a>RecurringMasterItemId

Das **RecurringMasterItemId-Element** identifiziert ein Serienmasterelement, indem die Bezeichner eines seiner zugehörigen Vorkommenselemente identifiziert werden. 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 **RecurringMasterItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**OccurrenceId** <br/> |Identifiziert ein einzelnes Vorkommen eines wiederkehrenden Masterelements. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Identifiziert eine bestimmte Version eines einzelnen Vorkommens eines wiederkehrenden Masterelements. Darüber hinaus wird das wiederkehrende Masterelement auch identifiziert, da es und das einzelne Vorkommen denselben Änderungsschlüssel enthalten. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GlobalItemIds](globalitemids.md) <br/> |Enthält die Auflistung von Elementbezeichnern für alle Unterhaltungselemente in einem Postfach.  <br/> |
|[ItemChange](itemchange.md) <br/> |Enthält einen Elementbezeichner und die Aktualisierungen, die auf das Element angewendet werden sollen. <br/> <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:  <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[ItemIds](itemids.md) <br/> | Enthält die eindeutigen Identitäten von Elementen, Vorkommenselementen und wiederkehrenden Masterelementen, die zum Löschen, Senden, Abrufen, Verschieben oder Kopieren von Elementen im Exchange Speicher verwendet werden. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="example"></a>Beispiel

Im folgenden Beispiel wird das wiederkehrende Masterelement identifiziert, indem eines seiner Vorkommen mit dem Bezeichner 56lkjh6 identifiziert wird.
  
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

