---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: Das GroupBy-Element gibt eine beliebige Gruppierung für FindItem-Abfragen an.
ms.openlocfilehash: 15e2d818ceae81f08ad0c52d9bdc881f7c3e2579
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539802"
---
# <a name="groupby"></a>GroupBy

Das **GroupBy-Element** gibt eine beliebige Gruppierung für FindItem-Abfragen an. 
  
- [FindItem](finditem.md)
- [GroupBy](groupby.md)
  
```xml
<GroupBy Order="">
   <FieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <ExtendededFieldURI/>
   <AggregateOn/>
</GroupBy>
```

```xml
<GroupBy Order="">
   <IndexedFieldURI/>
   <AggregateOn/>
</GroupBy>
```

**GroupByType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Order** <br/> | Bestimmt die Reihenfolge der Gruppen im gruppierten Elementarray, das in der Antwort zurückgegeben wird. Dieses Attribut ist vom Typ SortDirectionType.  <br/> |
   
#### <a name="order-attribute-values"></a>Order-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Aufsteigend  <br/> |Die Gruppen werden in aufsteigender Reihenfolge sortiert.  <br/> |
|Absteigend  <br/> |Die Gruppen werden in absteigender Reihenfolge sortiert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifies frequently referenced properties by URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Mitglieder eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert erweiterte MAPI-Eigenschaften, die abgerufen, festgelegt oder erstellt werden sollen.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Represents the field that is used to determine the order of groups in a response.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/><br/> Es folgt der XPath-Ausdruck für dieses Element:  `/FindItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die FindItem-Antwort enthält eine Sammlung von Gruppen. Jede Gruppe enthält alle Elemente mit übereinstimmenden Werten für die **GroupBy-Eigenschaft.** Die Eigenschaft, die die Gruppierung bestimmt, wird im [FieldURI-,](fielduri.md) [IndexedFieldURI-](indexedfielduri.md)oder [ExtendedFieldURI-Element](extendedfielduri.md) identifiziert. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

