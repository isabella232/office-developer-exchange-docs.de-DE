---
title: Typ (ElcFolderType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 6faad98f-1a92-4373-bde5-dd12af61765f
description: Das Type-Element gibt den Typ des Ordners in einer Aufbewahrungsrichtlinie verwendet.
ms.openlocfilehash: f679a9237a577d26d4b28e1b25f3e135f7193903
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839268"
---
# <a name="type-elcfoldertype"></a>Typ (ElcFolderType)

Das **Type** -Element gibt den Typ des Ordners in einer Aufbewahrungsrichtlinie verwendet. 
  
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

Der Textwert der **Type** -Element ist der Ordner, die in einer Aufbewahrungsrichtlinie verwendet. Der Textwert kann eine der folgenden Werte, die einen Standardtyp Ordner darstellen: Kalender, Kontakte, DeletedItems, Entwürfe, Posteingang, JunkEmail, Journal, Notizen, Postausgang, gesendete Elemente, Aufgaben, All, ManagedCustomFolder, RssSubscriptions, SyncIssues, ConversationHistory, persönlich, RecoverableItems oder NonIpmRoot 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

