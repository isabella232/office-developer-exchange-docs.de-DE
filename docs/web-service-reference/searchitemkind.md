---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: Das SearchItemKind-Element gibt den Typ der Elemente an, die nach einer FindMailboxStatisticsByKeyword-Operation durchsucht werden.
ms.openlocfilehash: e0625ac169c3083702494c094da15d38d220fe67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44464000"
---
# <a name="searchitemkind"></a>SearchItemKind

Das **SearchItemKind** -Element gibt den Typ der Elemente an, die nach einer **FindMailboxStatisticsByKeyword** -Operation durchsucht werden. 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 **SearchItemKindType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MessageTypes](messagetypes.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SearchItemKind** -Elements ist der Typ des Elements, das nach Schlüsselwörtern durchsucht wird. Die folgende Liste enthält die Text Werte, die im **SearchItemKind** -Element verwendet werden können. 
  
- **E-Mail** : gibt an, dass e-Mail-Nachrichten nach Stichwörtern durchsucht werden. 
    
- **Besprechungen** – gibt an, dass Besprechungen nach Stichwörtern durchsucht werden. 
    
- **Aufgaben** : gibt an, dass Aufgaben nach Schlüsselwörtern durchsucht werden. 
    
- **Hinweise** : gibt an, dass Notizen nach Stichwörtern durchsucht werden. 
    
- **Docs** : gibt an, dass Dokumente nach Stichwörtern durchsucht werden. 
    
- **Journals** – gibt an, dass Journale nach Stichwörtern durchsucht werden. 
    
- **Kontakte** : gibt an, dass Kontakte nach Stichwörtern durchsucht werden. 
    
- **Sofortnachrichten – gibt** an, dass Nachrichten nach Stichwörtern durchsucht werden. 
    
- **Voicemail** : gibt an, dass Voicemails nach Stichwörtern durchsucht werden. 
    
- **Faxnachrichten** – gibt an, dass Faxnachrichten nach Stichwörtern durchsucht werden. 
    
- **Beiträge** : gibt an, dass Beiträge nach Stichwörtern durchsucht werden. 
    
- **RSSfeeds** – gibt an, dass RSS-Feeds nach Stichwörtern durchsucht werden. 
    
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

