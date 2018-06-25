---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: Das FoldersToIgnore-Element gibt eine Liste der Ordner, die beim Abrufen von Elementen in einer Unterhaltung ignoriert werden. Alle Unterhaltungselemente in den Ordnern ignorierten werden nicht in einer Antwort GetConversationItems zurückgegeben.
ms.openlocfilehash: 96c094996c601e685dc1c7e6b869a790ce7d74a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758522"
---
# <a name="folderstoignore"></a>FoldersToIgnore

Das **FoldersToIgnore** -Element gibt eine Liste der Ordner, die beim Abrufen von Elementen in einer Unterhaltung ignoriert werden. Alle Unterhaltungselemente in den Ordnern ignorierten werden nicht in einer Antwort **GetConversationItems** zurückgegeben. 
  
```XML
<FoldersToIgnore>
   <FolderId/>
   <DistinguishedFolderId/>
</FoldersToIgnore>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[FolderId](folderid.md) | [DistinguishedFolderId](distinguishedfolderid.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetConversationItems](getconversationitems.md)
  
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
   

