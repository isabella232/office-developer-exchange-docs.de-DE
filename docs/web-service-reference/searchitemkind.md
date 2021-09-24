---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: Das SearchItemKind-Element gibt den Typ der Elemente an, die nach einem FindMailboxStatisticsByKeyword-Vorgang durchsucht werden.
ms.openlocfilehash: 93803d181f32d88c30ab0fa9a72bb92f22907dde
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59510855"
---
# <a name="searchitemkind"></a>SearchItemKind

Das **SearchItemKind-Element** gibt den Typ der Elemente an, die nach einem **FindMailboxStatisticsByKeyword-Vorgang** durchsucht werden. 
  
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

Der Textwert des **SearchItemKind-Elements** ist der Elementtyp, nach dem nach Schlüsselwörtern gesucht wird. Die folgende Liste enthält die Textwerte, die im **SearchItemKind-Element** verwendet werden können. 
  
- **E-Mail** – Gibt an, dass E-Mail-Nachrichten nach Schlüsselwörtern durchsucht werden. 
    
- **Besprechungen** – Gibt an, dass Besprechungen nach Schlüsselwörtern durchsucht werden. 
    
- **Aufgaben** – Gibt an, dass nach Stichwörtern gesucht wird. 
    
- **Notizen** – Gibt an, dass nach Schlüsselwörtern gesucht wird. 
    
- **Dokumente** – Gibt an, dass Dokumente nach Schlüsselwörtern durchsucht werden. 
    
-  Stichwörter – Gibt an, dass nach Schlüsselwörtern gesucht wird. 
    
- **Kontakte** – Gibt an, dass Kontakte nach Schlüsselwörtern durchsucht werden. 
    
- **Chat** – Gibt an, dass sofort nach Schlüsselwörtern gesucht wird. 
    
- **Voicemail** – Gibt an, dass Voicemails nach Schlüsselwörtern durchsucht werden. 
    
- **Faxe** – Gibt an, dass Faxe nach Schlüsselwörtern durchsucht werden. 
    
- **Beiträge** – Gibt an, dass Beiträge nach Schlüsselwörtern durchsucht werden. 
    
- **Rssfeeds** – Gibt an, dass RSS-Feeds nach Schlüsselwörtern gesucht werden. 
    
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

