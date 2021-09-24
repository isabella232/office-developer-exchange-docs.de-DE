---
title: SearchParameters
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SearchParameters
api_type:
- schema
ms.assetid: 34602cb1-dc33-4552-a98c-3e77f614daa3
description: Das SearchParameters-Element stellt die Parameter dar, die einen Suchordner definieren.
ms.openlocfilehash: a6a421ea6e8cfa0a2453d5cc86f6780010b6f7de
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521627"
---
# <a name="searchparameters"></a>SearchParameters

Das **SearchParameters-Element** stellt die Parameter dar, die einen Suchordner definieren. 
  
```xml
<SearchParameters Traversal="">
   <Restriction/>
   <BaseFolderIds/>
</SearchParameters>
```

 **SearchParametersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Traversal** <br/> |Beschreibt, wie ein Suchordner die Ordnerhierarchie durchläuft. Die Optionen sind für eine **Deep-** oder eine **Shallow-Suche.**  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Restriction](restriction.md) <br/> |Stellt die Einschränkung oder Abfrage dar, die zum Filtern von Elementen oder Ordnern in FindItem/FindFolder und Suchordnervorgängen verwendet wird.  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Stellt die Auflistung von Ordnern dar, die minimiert werden, um den Inhalt eines Suchordners zu bestimmen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner dar, der in einem Postfach enthalten ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

