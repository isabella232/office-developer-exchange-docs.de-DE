---
title: FolderChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderChange
api_type:
- schema
ms.assetid: 23279750-131b-4e1a-b7d1-be235c4e0891
description: Das FolderChange-Element stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.
ms.openlocfilehash: 3ea723e6bbfcfe048256715aa5a60da98076ccb8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541294"
---
# <a name="folderchange"></a>FolderChange

Das **FolderChange-Element** stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen. 
  
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
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines zu aktualisierenden Ordners.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifies MicrosoftExchange Server 2007 folders that can be referenced by name.  <br/> |
|[Updates (Ordner)](updates-folder.md) <br/> |Definiert den Aktualisierungstyp, der für einen Ordner ausgeführt wird, der durch das [FolderId-](folderid.md) oder [DistinguishedFolderId-Element](distinguishedfolderid.md) identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |Stellt eine Auflistung von Änderungen für einen Ordner dar.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [UpdateFolder-Vorgang](updatefolder-operation.md)

