---
title: DeleteFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DeleteFolder
api_type:
- schema
ms.assetid: e37963f4-af9e-4481-b389-16175711e66d
description: Das DeleteFolder-Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Informationsspeicher.
ms.openlocfilehash: eb705a47b78b19c79b2e87561ba3696ed40e09cd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458768"
---
# <a name="deletefolder"></a>DeleteFolder

Das **DeleteFolder** -Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Informationsspeicher. 
  
```XML
<DeleteFolder DeleteType="">
   <FolderIds/>
</DeleteFolder>
```

 **DeleteFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Deletetypeharddelete** <br/> |Beschreibt, wie ein Ordner gelöscht wird. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Ein Ordner wird dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |Wenn der Papierkorb aktiviert ist, wird ein Ordner in den Papierkorb verschoben.  <br/> |
|MoveToDeletedItems  <br/> |Ein Ordner wird in den Ordner "Gelöschte Elemente" verschoben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von zu löschenden Ordnern verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Die **MoveToDeletedItems** -und **HardDelete** -Optionen sind transaktional, was bedeutet, dass die Datenbank zum Zeitpunkt des Abschlusses eines Webdienstaufrufs das Element in den Ordner "Gelöschte Elemente" verschoben oder das Element endgültig aus der Exchange-Datenbank entfernt hat. Dieses Verhalten ist für Microsoft Exchange Server 2007 und Exchange Server 2010 identisch. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteFolder-Vorgang](deletefolder-operation.md)

