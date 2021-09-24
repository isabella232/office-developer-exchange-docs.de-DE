---
title: ContextFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ContextFolderId
api_type:
- schema
ms.assetid: 48de92aa-e124-42b5-89bc-cdce5e93d78b
description: Das ContextFolderId-Element gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden. Dieses Element muss beim Kopieren, Löschen, Verschieben und Festlegen des Lesestatus von Unterhaltungselementen in einem Zielordner vorhanden sein.
ms.openlocfilehash: f9b1a5d140bbdaf91b2feee724101be3884f6c99
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518673"
---
# <a name="contextfolderid"></a>ContextFolderId

Das **ContextFolderId-Element** gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden. Dieses Element muss beim Kopieren, Löschen, Verschieben und Festlegen des Lesestatus von Unterhaltungselementen in einem Zielordner vorhanden sein. 
  
- [ApplyConversationAction](applyconversationaction.md) 
- [ConversationActions](conversationactions.md)
- [ConversationAction](conversationaction.md)
- [ContextFolderId](contextfolderid.md)
  
```XML
<ContextFolderId>
   <FolderId/>
</ContextFolderId>
```

```XML
<ContextFolderId>
   <DistinguishedFolderId/>
</ContextFolderId>
```


**TargetFolderIdType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel des Kontextordners.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert Ordner, auf die anhand des Namens verwiesen werden kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ConversationAction](conversationaction.md) <br/> |Enthält eine einzelne Aktion, die auf eine einzelne Unterhaltung angewendet werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ApplyConversationAction-Vorgang](applyconversationaction-operation.md)

