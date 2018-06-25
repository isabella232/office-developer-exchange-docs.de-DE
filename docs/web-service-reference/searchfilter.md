---
title: SearchFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: Das SearchFilter-Element enthält die Abfragezeichenfolge zum Filtern der Postfächer aus einer GetSearchableMailboxes Anforderung zurückgegeben werden soll.
ms.openlocfilehash: b71d8dd862e9338afc145545df4cd29e8bcc3dc8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831285"
---
# <a name="searchfilter"></a>SearchFilter

Das **SearchFilter** -Element enthält die Abfragezeichenfolge zum Filtern der Postfächer aus einer **GetSearchableMailboxes** Anforderung zurückgegeben werden soll. 
  
```XML
<SearchFilter></SearchFilter>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetSearchableMailboxes](getsearchablemailboxes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SearchFilter** -Elements ist eine Abfragezeichenfolge an Filter Postfächer für Discovery-Suche. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

