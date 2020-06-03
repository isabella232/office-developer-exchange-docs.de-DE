---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: Das FolderChange-Element stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.
ms.openlocfilehash: e4a025bef100fdd478be545b6448b15886e47c60
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530239"
---
# <a name="folderchange"></a>FolderChange

Das **FolderChange** -Element stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen. 
  
- [UpdateFolder](updatefolder.md) 
- [FolderChanges](folderchanges.md) 
- [FolderChange](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
   <Updates/>
</FolderChange>
```

```xml
<FolderChange>
   <DistinguishedFolderId/>
   <Updates/>
</FolderChange>
```

**FolderChangeType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners, der aktualisiert werden soll.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert Microsoft Exchange Server 2007-Ordner, auf die über den Namen verwiesen werden kann.  <br/> |
|[Updates (Ordner)](updates-folder.md) <br/> |Definiert den Aktualisierungstyp, der für einen Ordner ausgeführt wird, der entweder durch das [Folder](folderid.md) -oder [DistinguishedFolderId](distinguishedfolderid.md) -Element identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |Stellt eine Auflistung von Änderungen für einen Ordner dar.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateFolder-Vorgang](updatefolder-operation.md)

