---
title: Sortierreihenfolge (ConversationNodeSortOrder)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9c4295c-8089-4533-b92f-2051eae9afeb
description: Das Element "Sort" gibt die Sortierreihenfolge an, die für das Ergebnis einer GetConversationItems-Anforderung verwendet wird.
ms.openlocfilehash: 69d362b9f769749bcc9692825b64ff486e8b60a0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530965"
---
# <a name="sortorder-conversationnodesortorder"></a>Sortierreihenfolge (ConversationNodeSortOrder)

Das **Element "Sort" gibt** die Sortierreihenfolge an, die für das Ergebnis einer **GetConversationItems** -Anforderung verwendet wird. 
  
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

Der Textwert des Elements " **Sortier** Reihenfolge" ist die Reihenfolge, in der Unterhaltungen sortiert wurden. Der Textwert **TreeOrderAscending** gibt an, dass die Unterhaltungen entsprechend der Unterhaltungs Struktur in aufsteigender Reihenfolge sortiert werden. Der Textwert **TreeOrderDescending** gibt an, dass die Unterhaltungen entsprechend der Unterhaltungs Struktur in absteigender Reihenfolge sortiert werden. Der Textwert **DateOrderAscending** gibt an, dass die Unterhaltungen entsprechend dem Unterhaltungs Datum in aufsteigender Reihenfolge sortiert werden. Der Textwert **DateOrderDescending** gibt an, dass die Unterhaltungen entsprechend dem Unterhaltungs Datum in absteigender Reihenfolge sortiert werden. 
  
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
   

