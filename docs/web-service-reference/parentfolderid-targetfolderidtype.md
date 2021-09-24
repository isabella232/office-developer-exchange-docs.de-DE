---
title: ParentFolderId (TargetFolderIdType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ParentFolderId
api_type:
- schema
ms.assetid: 0e3e6e5f-06d0-499b-8ca4-d36036521658
description: Das ParentFolderId-Element identifiziert den Ordner, in dem ein neuer Ordner erstellt wird, oder den Ordner, in dem nach dem FindConversation-Vorgang gesucht werden soll.
ms.openlocfilehash: 53a5721b2c20c211a61b7e71b2e4f636700456b4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524623"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

Das **ParentFolderId-Element** identifiziert den Ordner, in dem ein neuer Ordner erstellt wird, oder den Ordner, in dem nach dem [FindConversation-Vorgang](findconversation-operation.md)gesucht werden soll.
  
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

Das **ParentFolderId-Element** enthält zwei untergeordnete Elemente. Die untergeordneten Elemente schließen sich im Schema gegenseitig aus. 
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den erforderlichen Bezeichner und den optionalen Änderungsschlüssel eines Ordners, in dem ein neuer Ordner erstellt wird, oder des Ordners, der nach dem [FindConversation-Vorgang](findconversation-operation.md)durchsucht wird. Die Verwendung dieses Elements schließt die Verwendung des [DistinguishedFolderId-Elements](distinguishedfolderid.md) aus.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner. Die Verwendung dieses Elements schließt die Verwendung des [FolderId-Elements](folderid.md) aus.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |Definiert eine Anforderung zum Erstellen eines Ordners in der Exchange Datenbank.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die beiden untergeordneten Elemente werden verwendet, um den Ordner zu definieren, der den neuen Ordner enthalten soll. Sie müssen entweder die [FolderId](folderid.md) oder das [DistinguishedFolderId-Element](distinguishedfolderid.md) auswählen, um den übergeordneten Ordner des neuen Ordners zu identifizieren. Sie können nicht beide Elemente gleichzeitig verwenden. Dieses Element ist erforderlich, um Ordner zu erstellen. 
  
Das [ParentFolderId-Element](parentfolderid.md) beschreibt den Speicherort vorhandener Elemente und Ordner. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateFolder-Vorgang](createfolder-operation.md)
- [FindConversation-Vorgang](findconversation-operation.md)
- [Erstellen von Ordnern (Exchange Webdienste)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

