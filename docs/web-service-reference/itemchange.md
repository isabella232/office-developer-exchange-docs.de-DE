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
description: Das ItemChange-Element enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.
ms.openlocfilehash: 916ef1ba2c7a709ec1fd80ababd72999506773c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459917"
---
# <a name="itemchange"></a>ItemChange

Das **ItemChange** -Element enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen. 
  
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
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher. Dieses Element ist erforderlich, wenn das [OccurrenceItemId](occurrenceitemid.md) -oder das [RecurringMasterItemId](recurringmasteritemid.md) -Element nicht verwendet wird.  <br/> |
|[OccurrenceItemId](occurrenceitemid.md) <br/> |Gibt ein einzelnes Vorkommen eines wiederkehrenden Elements an. Dieses Element ist erforderlich, wenn es verwendet wird. Dieses Element ist erforderlich, wenn das [RecurringMasterItemId](recurringmasteritemid.md) -oder [ItemID](itemid.md) -Element nicht verwendet wird.  <br/> |
|[RecurringMasterItemId](recurringmasteritemid.md) <br/> |Identifiziert ein Serienmasterelement durch Identifizieren eines der Bezeichner des zugehörigen vorkommen Elements. Dieses Element ist erforderlich, wenn es verwendet wird. Dieses Element ist erforderlich, wenn das [OccurrenceItemId](occurrenceitemid.md) -oder [ItemID](itemid.md) -Element nicht verwendet wird.  <br/> |
|[Updates (Element)](updates-item.md) <br/> |Enthält ein Array, das Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definiert. Dieses Element ist erforderlich.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemChanges](itemchanges.md) <br/> |Enthält ein Array von [ItemChange](itemchange.md) -Elementen, mit denen Elemente identifiziert werden, und die Updates, die auf die Elemente angewendet werden sollen.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a>Bemerkungen

In einem **ItemChange** -Element kann nur ein einzelnes [ItemID](itemid.md)-, [OccurrenceItemId](occurrenceitemid.md)-oder [RecurringMasterItemId](recurringmasteritemid.md) -Element verwendet werden. 
  
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

