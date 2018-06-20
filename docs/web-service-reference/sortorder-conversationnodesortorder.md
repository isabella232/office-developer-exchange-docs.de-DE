---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: Das SortOrder-Element gibt die Sortierreihenfolge für das Ergebnis einer Anforderung GetConversationItems verwendet.
ms.openlocfilehash: 397aead62d32e72f991af783bff02e79a6e4b0fb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831520"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder (ConversationNodeSortOrder)

Das **SortOrder** -Element gibt die Sortierreihenfolge für das Ergebnis einer Anforderung **GetConversationItems** verwendet. 
  
```XML
<SortOrder>TreeOrderAscending | TreeOrderDescending | DateOrderAscending | DateOrderDescending</SortOrder>
```

 **ConversationNodeSortOrder**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetConversationItems](getconversationitems.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SortOrder** -Elements ist die Reihenfolge, in denen Unterhaltungen bestellt. Ein Textwert der **TreeOrderAscending** gibt an, dass die Kommunikation entsprechend der Struktur des Unterhaltung in aufsteigender Reihenfolge sortiert sind. Ein Textwert der **TreeOrderDescending** gibt an, dass die Kommunikation entsprechend der Struktur des Unterhaltung in absteigender Reihenfolge sortiert sind. Ein Textwert der **DateOrderAscending** gibt an, dass die Unterhaltungen entsprechend dem Datum Unterhaltung in aufsteigender Reihenfolge sortiert sind. Ein Textwert der **DateOrderDescending** gibt an, dass die Unterhaltungen entsprechend der Unterhaltung Datum in absteigender Reihenfolge sortiert sind. 
  
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
   

