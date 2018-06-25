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
description: FolderChange-Element stellt eine Auflistung von Änderungen in einem gemeinsamen Ordner ausgeführt werden.
ms.openlocfilehash: 3f8b42ff4ac88eaef53d1d4ec1d61212bc14b8c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758505"
---
# <a name="folderchange"></a>FolderChange

**FolderChange** -Element stellt eine Auflistung von Änderungen in einem gemeinsamen Ordner ausgeführt werden. 
  
[UpdateFolder](updatefolder.md)
  
[FolderChanges](folderchanges.md)
  
[FolderChange](folderchange.md)
  
```xml
<FolderChange>
   <FolderId/>
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
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners zu aktualisieren.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert MicrosoftExchange Server 2007-Ordner, die nach Namen verwiesen werden können.  <br/> |
|[Updates (Ordner)](updates-folder.md) <br/> |Definiert den Typ des Updates, die für einen Ordner ausgeführt wird, die durch die [FolderId](folderid.md) oder [DistinguishedFolderId](distinguishedfolderid.md) -Element identifiziert wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderChanges](folderchanges.md) <br/> |Stellt eine Auflistung von Änderungen für einen Ordner.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/UpdateFolder/FolderChanges` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateFolder-Vorgang](updatefolder-operation.md)

