---
title: Typ (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Das Type-Element gibt den Typ des Ordners an, der in einer Aufbewahrungsrichtlinie verwendet wird.
ms.openlocfilehash: f6fcc7942a530ada2d6e72c3e38286a7595b09ec
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465107"
---
# <a name="type-elcfoldertype"></a>Typ (ElcFolderType)

Das **Type** -Element gibt den Typ des Ordners an, der in einer Aufbewahrungsrichtlinie verwendet wird. 
  
```XML
<Type> Calendar | Contacts | DeletedItems | Drafts | Inbox | JunkEmail | Journal | Notes | Outbox | SentItems | Tasks | All | ManagedCustomFolder | RssSubscriptions | SyncIssues | ConversationHistory | Personal | RecoverableItems | NonIpmRoot <Type>
```

 **ElcFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **Type** -Elements ist der Ordnertyp, der in einer Aufbewahrungsrichtlinie verwendet wird. Der Textwert kann einer der folgenden Werte sein, die einen Standardordnertyp darstellen: Kalender, Kontakte, DeletedItems, Entwürfe, Posteingang, JunkEmail, Journal, Notizen, Postausgang, gesendete Elemente, Aufgaben, alle, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, persönlich, RecoverableItems oder NonIpmRoot 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

