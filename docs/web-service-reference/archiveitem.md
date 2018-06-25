---
title: ArchiveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c2172e61-876a-4f76-bc9c-263c8be11429
description: Das ArchiveItem-Element enthält die Id des Quellordners und ein Array der Element-Ids für das Archivelement zugeordnete.
ms.openlocfilehash: 7f2d79f5a9e6798fafcf64e8b1bb680390800992
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757372"
---
# <a name="archiveitem"></a>ArchiveItem

Das **ArchiveItem** -Element enthält die Id des Quellordners und ein Array der Element-Ids für das Archivelement zugeordnete. 
  
```XML
<ArchiveItem>
   <ArchiveSourceFolderId/>
   <ItemIds/>
</ArchiveItem>
```

 **ArchiveItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[ArchiveSourceFolderId](archivesourcefolderid.md) | [Artikelnummern ein.](itemids.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

