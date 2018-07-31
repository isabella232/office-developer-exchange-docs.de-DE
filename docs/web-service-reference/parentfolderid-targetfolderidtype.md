---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: Das ParentFolderId-Element identifiziert den Ordner in der erstellt wird, eines neuen Ordners oder den Ordner für den Vorgang FindConversation suchen.
ms.openlocfilehash: 8e80b9b342274a8b2004838ebd16f8425a2d3fa3
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353826"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

Das **ParentFolderId** -Element identifiziert den Ordner in der erstellt wird, eines neuen Ordners oder den Ordner für den [Vorgang FindConversation](findconversation-operation.md)suchen.
  
```xml
<ParentFolderId>
   <DistinguishedFolderId/>
</ParentFolderId>
```

```xml
<ParentFolderId>
   <FolderId/> 
</ParentFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

Das **ParentFolderId** -Element enthält zwei untergeordnete Elemente. Die untergeordneten Elemente schließen sich gegenseitig aus im Schema. 
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält die erforderlichen Bezeichner und der Key optional Ändern eines Ordners in der erstellt wird, eines neuen Ordners oder den Ordner, der für den [Vorgang FindConversation](findconversation-operation.md)durchsucht wird. Die Verwendung dieses Elements schließt die Verwendung des [DistinguishedFolderId](distinguishedfolderid.md) -Elements.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner. Die Verwendung dieses Elements schließt die Verwendung des [FolderId](folderid.md) -Elements.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |Definiert eine Anforderung an einen Ordner in der Exchange-Datenbank zu erstellen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Die beiden untergeordneten Elemente werden verwendet, den Ordner zu definieren, der den neuen Ordner enthalten wird. Sie müssen entweder die [FolderId](folderid.md) oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element zum Identifizieren des übergeordneten Ordners des neuen Ordners auswählen. Sie können nicht beide Elemente gleichzeitig verwenden. Dieses Element ist erforderlich, um Ordner zu erstellen. 
  
Das Element [ParentFolderId](parentfolderid.md) beschreibt den Speicherort der vorhandenen Elemente und Ordner. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateFolder-Vorgang](createfolder-operation.md)
- [FindConversation-Vorgang](findconversation-operation.md)
- [Erstellen von Ordnern (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

