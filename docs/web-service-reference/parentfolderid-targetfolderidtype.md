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
description: Das parentfolderid-Element gibt den Ordner an, in dem ein neuer Ordner erstellt wird, oder den Ordner, der für den FindConversation-Vorgang gesucht werden soll.
ms.openlocfilehash: 36e63266d10603c4d453a37e2b0d22e02599e516
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467802"
---
# <a name="parentfolderid-targetfolderidtype"></a>ParentFolderId (TargetFolderIdType)

Das **parentfolderid** -Element gibt den Ordner an, in dem ein neuer Ordner erstellt wird, oder den Ordner, der für den [FindConversation-Vorgang](findconversation-operation.md)gesucht werden soll.
  
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

Das **parentfolderid** -Element enthält zwei untergeordnete Elemente. Die untergeordneten Elemente sind im Schema gegenseitig ausschliessend. 
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den erforderlichen Bezeichner und den optionalen Änderungsschlüssel eines Ordners, in dem ein neuer Ordner erstellt wird, oder der Ordner, der für den [FindConversation-Vorgang](findconversation-operation.md)durchsucht wird. Die Verwendung dieses Elements schließt die Verwendung des [DistinguishedFolderId](distinguishedfolderid.md) -Elements aus.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner. Die Verwendung dieses Elements schließt die Verwendung des [Folder](folderid.md) -Elements aus.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateFolder](createfolder.md) <br/> |Definiert eine Anforderung zum Erstellen eines Ordners in der Exchange-Datenbank.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/CreateFolder` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die beiden untergeordneten Elemente werden verwendet, um den Ordner zu definieren, der den neuen Ordner enthalten soll. Sie müssen entweder die [Ordner](folderid.md) -oder das [DistinguishedFolderId](distinguishedfolderid.md) -Element auswählen, um den übergeordneten Ordner des neuen Ordners zu identifizieren. Beide Elemente können nicht gleichzeitig verwendet werden. Dieses Element ist zum Erstellen von Ordnern erforderlich. 
  
Das [parentfolderid](parentfolderid.md) -Element beschreibt den Speicherort vorhandener Elemente und Ordner. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [CreateFolder-Vorgang](createfolder-operation.md)
- [FindConversation-Vorgang](findconversation-operation.md)
- [Erstellen von Ordnern (Exchange Webdienste)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

