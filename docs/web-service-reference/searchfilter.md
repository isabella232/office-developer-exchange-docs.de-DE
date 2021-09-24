---
title: SearchFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: Das SearchFilter-Element enthält die Abfragezeichenfolge zum Filtern der Postfächer, die von einer GetSearchableMailboxes-Anforderung zurückgegeben werden sollen.
ms.openlocfilehash: 19bb3109942c9a3064cbeaae4a19380d97c94feb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509357"
---
# <a name="searchfilter"></a>SearchFilter

Das **SearchFilter-Element** enthält die Abfragezeichenfolge zum Filtern der Postfächer, die von einer **GetSearchableMailboxes-Anforderung** zurückgegeben werden sollen. 
  
```XML
<SearchFilter></SearchFilter>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetSearchableMailboxes](getsearchablemailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SearchFilter-Elements** ist eine Abfragezeichenfolge zum Filtern von Postfächern für die Ermittlungssuche. 
  
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
   

