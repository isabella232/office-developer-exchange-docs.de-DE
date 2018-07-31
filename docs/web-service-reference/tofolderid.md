---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: Das ToFolderId-Element darstellt, den Zielordner für eine kopierte oder verschobene Element oder einen Ordner.
ms.openlocfilehash: 9d2fd6c177711cfe3a5d3415320440259e2f5289
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353658"
---
# <a name="tofolderid"></a>ToFolderId

Das **ToFolderId** -Element darstellt, den Zielordner für eine kopierte oder verschobene Element oder einen Ordner. 
  
```xml
<ToFolderId>
   <FolderId/>
</ToFolderId>
```

```xml
<ToFolderId>
   <DistinguishedFolderId/>
</ToFolderId>
```

**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner des Zielordners für eine kopierte oder verschobene Element oder einen Ordner.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Gibt einen benannten Zielordner für eine kopierte oder verschobene Element oder einen Ordner.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MoveFolder](movefolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu kopieren.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung an ein Element im Exchange-Speicher zu kopieren.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MoveFolder-Vorgang](movefolder-operation.md)  
- [CopyFolder-Vorgang](copyfolder-operation.md) 
- [MoveItem-Vorgang](moveitem-operation.md) 
- [CopyItem-Vorgang](copyitem-operation.md)

