---
title: FolderChanges
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderChanges
api_type:
- schema
ms.assetid: d3f611ed-56a4-43f8-aa65-cbd7844b827f
description: Das FolderChanges-Element stellt eine Auflistung von Änderungen für einen Ordner dar.
ms.openlocfilehash: 2c3bfc3081e323771e9d909138f7ed03e3d50a84
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541287"
---
# <a name="folderchanges"></a>FolderChanges

Das **FolderChanges-Element** stellt eine Auflistung von Änderungen für einen Ordner dar. 
  
[UpdateFolder](updatefolder.md)
  
[FolderChanges](folderchanges.md)
  
```xml
<FolderChanges>
   <FolderChange/>
</FolderChanges>
```

 **NonEmptyArrayOfFolderChangesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderChange](folderchange.md) <br/> |Stellt eine einzelne Änderung dar, die für einen einzelnen Ordner ausgeführt werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[UpdateFolder](updatefolder.md) <br/> |Stellt den Vorgang dar, der zum Aktualisieren von Eigenschaften für einen Ordner verwendet wird.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/>  `/UpdateFolder` <br/> |
   
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



[UpdateFolder-Vorgang](updatefolder-operation.md)

