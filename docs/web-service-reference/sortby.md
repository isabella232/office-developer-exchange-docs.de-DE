---
title: SortBy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 3dc4ab23-26b0-42b3-8930-f1c7eefecdeb
description: Das SortBy-Element enthält eine Item-Eigenschaft, die zum Sortieren des Suchergebnisses verwendet wird.
ms.openlocfilehash: cf2b1e633bc66e526028078833afade363e4c5e0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468397"
---
# <a name="sortby"></a>SortBy

Das **SortBy** -Element enthält eine Item-Eigenschaft, die zum Sortieren des Suchergebnisses verwendet wird. 
  
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
|Reihenfolge  <br/> |Der Textwert des **Order** -Attributs ist die Sortierreihenfolge. Der Textwert **Aufsteigend** gibt an, dass die Ergebnisse in aufsteigender Reihenfolge angezeigt werden. Der Textwert **Absteigend** gibt an, dass sich die Ergebnisse in absteigender Reihenfolge befinden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[FieldURI](fielduri.md)  |  [IndexedFieldURI](indexedfielduri.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxes](searchmailboxes.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> ||
   

