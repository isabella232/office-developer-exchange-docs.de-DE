---
title: ToFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ToFolderId
api_type:
- schema
ms.assetid: bd6a4265-ad40-43f6-bcc4-0bf5df4e984c
description: Das ToFolderId-Element stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen ordner dar.
ms.openlocfilehash: b58192aa4d1ffe609da78dfdf1b5c86522fc45c8
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515166"
---
# <a name="tofolderid"></a>ToFolderId

Das **ToFolderId-Element** stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen ordner dar. 
  
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
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner eines Zielordners für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert einen benannten Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MoveFolder](movefolder.md) <br/> |Definiert eine Anforderung zum Verschieben eines Ordners im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Definiert eine Anforderung zum Kopieren eines Ordners im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CopyFolder` <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung zum Verschieben eines Elements im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/MoveItem` <br/> |
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung zum Kopieren eines Elements im Exchange Speicher.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [MoveFolder-Vorgang](movefolder-operation.md)  
- [CopyFolder-Vorgang](copyfolder-operation.md) 
- [MoveItem-Vorgang](moveitem-operation.md) 
- [CopyItem-Vorgang](copyitem-operation.md)

