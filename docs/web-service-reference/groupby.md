---
title: GroupBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupBy
api_type:
- schema
ms.assetid: 9728619b-4674-4b9d-9f6c-e75c6165966c
description: Das GroupBy-Element gibt eine beliebige Gruppierung für FindItem-Abfragen an.
ms.openlocfilehash: 0d681e5376e4dd71921cc97f270211e49179db85
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530099"
---
# <a name="groupby"></a>GroupBy

Das **GroupBy** -Element gibt eine beliebige Gruppierung für FindItem-Abfragen an. 
  
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

**Groupbytype**

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
|Absteigender  <br/> |Die Gruppen werden in absteigender Reihenfolge sortiert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert häufig referenzierte Eigenschaften nach URI.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Identifiziert einzelne Member eines Wörterbuchs.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Identifiziert erweiterte MAPI-Eigenschaften zum Abrufen, festlegen oder erstellen.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Stellt das Feld dar, das verwendet wird, um die Reihenfolge der Gruppen in einer Antwort zu bestimmen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/><br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/FindItem` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Die FindItem-Antwort enthält eine Auflistung von Gruppen. Jede Gruppe enthält alle Elemente mit übereinstimmenden Werten für die **GroupBy** -Eigenschaft. Die Eigenschaft, die die Gruppierung bestimmt, wird im [FieldURI](fielduri.md)-, [IndexedFieldURI](indexedfielduri.md)-oder [ExtendedFieldURI](extendedfielduri.md) -Element identifiziert. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Suchen von Elementen](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

