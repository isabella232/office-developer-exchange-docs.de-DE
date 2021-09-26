---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: Das SortBy-Element enthält eine Elementeigenschaft, die zum Sortieren des Suchergebnisses verwendet wird.
ms.openlocfilehash: 8718bad3749a0409be2715b0e03001b97a4fb87e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544689"
---
# <a name="sortby"></a>SortBy

Das **SortBy-Element** enthält eine Elementeigenschaft, die zum Sortieren des Suchergebnisses verwendet wird. 
  
```XML
<SortBy Order="">
   <FieldURI/>
   <IndexedFieldURI/>
</SortBy>
```

 **FieldOrderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Reihenfolge  <br/> |Der Textwert des Order-Attributs ist die Sortierreihenfolge.  Der Textwert **Ascending** gibt an, dass sich die Ergebnisse in aufsteigender Reihenfolge befinden. Der Textwert **Descending** gibt an, dass sich die Ergebnisse in absteigender Reihenfolge befinden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[FieldURI](fielduri.md)  |  [IndexedFieldURI](indexedfielduri.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxes](searchmailboxes.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

