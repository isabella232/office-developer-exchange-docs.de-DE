---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: Das SearchItemKind-Element gibt den Typ der Elemente, die für einen Vorgang FindMailboxStatisticsByKeyword durchsucht werden.
ms.openlocfilehash: 1c099fc49ec882c1672b265ff0e3aa2c71c5f95b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831298"
---
# <a name="searchitemkind"></a>SearchItemKind

Das **SearchItemKind** -Element gibt den Typ der Elemente, die für einen Vorgang **FindMailboxStatisticsByKeyword** durchsucht werden. 
  
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

Der Textwert des **SearchItemKind** -Elements ist der Typ des Elements, die nach Schlüsselwörtern durchsucht wird. Die folgende Liste enthält die Textwerte, die im **SearchItemKind** -Element verwendet werden können. 
  
- **E-Mail** – gibt an, dass e-Mail-Nachrichten nach Schlüsselwörtern durchsucht werden. 
    
- **Besprechungen** - gibt an, dass Besprechungen nach Schlüsselwörtern durchsucht werden. 
    
- **Aufgaben** - gibt an, dass Aufgaben nach Schlüsselwörtern durchsucht werden. 
    
- **Notes** - gibt an, dass Notizen nach Schlüsselwörtern durchsucht werden. 
    
- **Dokumente** – gibt an, dass Dokumente nach Schlüsselwörtern durchsucht werden. 
    
- **Journale** - gibt an, dass Journale nach Schlüsselwörtern durchsucht werden. 
    
- **Kontakte** – gibt an, dass Kontakte nach Schlüsselwörtern durchsucht werden. 
    
- **Instant Messaging** - gibt an, dass Sofortnachrichten nach Schlüsselwörtern durchsucht werden. 
    
- **Voicemail** - gibt an, dass Voicemails nach Schlüsselwörtern durchsucht werden. 
    
- **Faxe** - gibt an, dass Faxe nach Schlüsselwörtern durchsucht werden. 
    
- **Beiträge** – gibt an, dass Beiträge nach Schlüsselwörtern durchsucht werden. 
    
- **Rssfeeds** - gibt an, dass RSS-Feeds für Schlüsselwörter durchsucht werden. 
    
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

