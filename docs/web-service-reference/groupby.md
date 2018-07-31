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
description: GroupBy-Element gibt eine beliebige Gruppierung für FindItem Abfragen an.
ms.openlocfilehash: cdf9b9906025bc91768bb4a14acb2573801c4e12
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353217"
---
# <a name="groupby"></a>GroupBy

**GroupBy** -Element gibt eine beliebige Gruppierung für FindItem Abfragen an. 
  
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
|**Order** <br/> | Bestimmt die Reihenfolge der Gruppen im Array gruppierten Element, das in der Antwort zurückgegeben wird. Dieses Attribut ist vom Typ SortDirectionType.  <br/> |
   
#### <a name="order-attribute-values"></a>Reihenfolge-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Ascending  <br/> |Die Gruppen werden in aufsteigender Reihenfolge sortiert.  <br/> |
|Absteigend  <br/> |Die Gruppen werden in absteigender Reihenfolge sortiert.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldURI](fielduri.md) <br/> |Identifiziert die Eigenschaften von URI häufig verwiesen wird.  <br/> |
|[IndexedFieldURI](indexedfielduri.md) <br/> |Einzelne Elemente eines Wörterbuchs identifiziert.  <br/> |
|[ExtendedFieldURI](extendedfielduri.md) <br/> |Bezeichnet die extended MAPI-Eigenschaften zum Abrufen oder festlegen, oder erstellen.  <br/> |
|[AggregateOn](aggregateon.md) <br/> |Stellt das dar, das verwendet wird, um die Reihenfolge der Gruppen in einer Antwort zu bestimmen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/><br/> Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Die Antwort FindItem enthält eine Auflistung von Gruppen. Jede Gruppe enthält alle Elemente, die übereinstimmenden Werte für die **GroupBy** -Eigenschaft. Die Eigenschaft, die bestimmt, die Gruppierung wird im [FieldURI](fielduri.md), [IndexedFieldURI](indexedfielduri.md)oder [ExtendedFieldURI](extendedfielduri.md) -Element identifiziert. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [FindItem-Vorgang](finditem-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Finding Items](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

