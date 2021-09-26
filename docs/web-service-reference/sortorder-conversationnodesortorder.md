---
title: SortOrder (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: Das SortOrder-Element gibt die Sortierreihenfolge an, die für das Ergebnis einer GetConversationItems-Anforderung verwendet wird.
ms.openlocfilehash: 0091968f1359b0cf744525139b5c6a8cf1687d81
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544675"
---
# <a name="sortorder-conversationnodesortorder"></a>SortOrder (ConversationNodeSortOrder)

Das **SortOrder-Element** gibt die Sortierreihenfolge an, die für das Ergebnis einer **GetConversationItems-Anforderung** verwendet wird. 
  
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

Der Textwert des **SortOrder-Elements** ist die Reihenfolge, in der Unterhaltungen sortiert wurden. Der Textwert **TreeOrderAscending** gibt an, dass die Unterhaltungen gemäß der Unterhaltungsstruktur in aufsteigender Reihenfolge sortiert sind. Der Textwert **TreeOrderDescending** gibt an, dass die Unterhaltungen gemäß der Unterhaltungsstruktur in absteigender Reihenfolge sortiert werden. Der Textwert **DateOrderAscending** gibt an, dass die Unterhaltungen gemäß dem Unterhaltungsdatum in aufsteigender Reihenfolge sortiert werden. Ein Textwert von **DateOrderDescending** gibt an, dass die Unterhaltungen gemäß dem Unterhaltungsdatum in absteigender Reihenfolge sortiert werden. 
  
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
   

