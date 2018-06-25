---
title: EmptyFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 502b2841-103d-4340-97d5-51a1db813fb2
description: Das EmptyFolder-Element definiert eine Anforderung an einen Ordner in einem Postfach im Exchange-Speicher zu leeren. Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird.
ms.openlocfilehash: c72e11cea29e2e55c9c29754eec60e73bd1e4d9c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758211"
---
# <a name="emptyfolder"></a>EmptyFolder

Das **EmptyFolder** -Element definiert eine Anforderung an einen Ordner in einem Postfach im Exchange-Speicher zu leeren. Optional können Unterordner auch gelöscht werden, wenn der Ordner geleert wird. 
  
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
|**DeleteSubFolders** <br/> |Gibt an, ob Unterordner gelöscht werden. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Eine Nachrichten und Ordnern dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Eine Nachrichten und Ordnern werden verschoben und die Dumpster Wenn die Dumpster ist aktiviert.  <br/> |
|MoveToDeletedItems  <br/> |Eine Nachrichten und Ordnern in den Ordner Gelöschte Objekte verschoben werden.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der zu löschenden Ordner verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[EmptyFolder-Vorgang](emptyfolder-operation.md)

