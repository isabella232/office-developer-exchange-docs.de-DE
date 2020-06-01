---
title: FoldersToIgnore
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: b5d18516-a617-4daf-8baf-c7ce29c76f6b
description: Das FoldersToIgnore-Element identifiziert eine Liste von Ordnern, die ignoriert werden, wenn Elemente in einer Unterhaltung abgerufen werden. Alle Unterhaltungselemente in den ignorierten Ordnern werden nicht in einer GetConversationItems-Antwort zurückgegeben.
ms.openlocfilehash: 07813a54a9a3afa3de23ae94f1c9b191d1cb6fac
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44453357"
---
# <a name="folderstoignore"></a>FoldersToIgnore

Das **FoldersToIgnore** -Element identifiziert eine Liste von Ordnern, die ignoriert werden, wenn Elemente in einer Unterhaltung abgerufen werden. Alle Unterhaltungselemente in den ignorierten Ordnern werden nicht in einer **GetConversationItems** -Antwort zurückgegeben. 
  
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

[Ordner-Nr](folderid.md)  |  [DistinguishedFolderId](distinguishedfolderid.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetConversationItems](getconversationitems.md)
  
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
   

