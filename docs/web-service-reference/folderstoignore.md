---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: Das FoldersToIgnore-Element identifiziert eine Liste von Ordnern, die beim Abrufen von Elementen in einer Unterhaltung ignoriert werden. Alle Unterhaltungselemente in den ignorierten Ordnern werden in einer GetConversationItems-Antwort nicht zurückgegeben.
ms.openlocfilehash: c0102d12b24df2cadd5e307e80c5acda9a3c0589
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59528660"
---
# <a name="folderstoignore"></a>FoldersToIgnore

Das **FoldersToIgnore-Element** identifiziert eine Liste von Ordnern, die beim Abrufen von Elementen in einer Unterhaltung ignoriert werden. Alle Unterhaltungselemente in den ignorierten Ordnern werden in einer **GetConversationItems-Antwort** nicht zurückgegeben. 
  
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

[FolderId](folderid.md)  |  [DistinguishedFolderId](distinguishedfolderid.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetConversationItems](getconversationitems.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

