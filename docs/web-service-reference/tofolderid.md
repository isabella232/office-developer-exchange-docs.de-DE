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
ms.openlocfilehash: a48309f0b7f5c9bf667fc2eb653a0502832bc996
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839222"
---
# <a name="tofolderid"></a>ToFolderId

Das **ToFolderId** -Element darstellt, den Zielordner für eine kopierte oder verschobene Element oder einen Ordner. 
  
```xml
<ToFolderId>
   <FolderId/>
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
|[MoveFolder](movefolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu kopieren.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung an ein Element im Exchange-Speicher zu kopieren.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/>  `/CopyItem` <br/> |
   
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



[MoveFolder-Vorgang](movefolder-operation.md)
  
[CopyFolder-Vorgang](copyfolder-operation.md)
  
[MoveItem Operation](moveitem-operation.md)
  
[CopyItem Operation](copyitem-operation.md)

