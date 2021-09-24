---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: Das EmptyFolder-Element definiert eine Anforderung zum Leeren eines Ordners in einem Postfach im Exchange Speicher. Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.
ms.openlocfilehash: c1b0e953f677c1fe5ae0958b35f85f3f5c4fb973
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519674"
---
# <a name="emptyfolder"></a>EmptyFolder

Das **EmptyFolder-Element** definiert eine Anforderung zum Leeren eines Ordners in einem Postfach im Exchange Speicher. Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird. 
  
```XML
<EmptyFolder>
   <FolderIds/>
</EmptyFolder>
```

 **EmptyFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**DeleteType** <br/> |Gibt an, wie ein Ordner geleert wird. Dieses Attribut ist erforderlich.  <br/> |
|**DeleteSubFolders** <br/> |Gibt an, ob Unterordner gelöscht werden sollen. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Nachrichten und Ordner werden dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Nachrichten und Ordner werden in den Dumpster verschoben, wenn der Dumpster aktiviert ist.  <br/> |
|MoveToDeletedItems  <br/> |Nachrichten und Ordner werden in den Ordner "Gelöschte Elemente" verschoben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von zu löschenden Ordnern verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[EmptyFolder-Vorgang](emptyfolder-operation.md)

