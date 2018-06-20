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
description: Das DeleteFolder-Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Speicher.
ms.openlocfilehash: d31f98f26f537104e40b303de4199f45c65f49c7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757920"
---
# <a name="deletefolder"></a>DeleteFolder

Das **DeleteFolder** -Element definiert eine Anforderung zum Löschen von Ordnern aus einem Postfach im Exchange-Speicher. 
  
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
|**DeleteType** <br/> |Beschreibt, wie ein Ordner gelöscht wird. Dieses Attribut ist erforderlich.  <br/> |
   
#### <a name="deletetype-attribute"></a>DeleteType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|HardDelete  <br/> |Ein Ordner wird dauerhaft aus dem Speicher entfernt.  <br/> |
|SoftDelete  <br/> |In ein Ordner verschoben die Dumpster Wenn die Dumpster ist aktiviert.  <br/> |
|MoveToDeletedItems  <br/> |Ein Ordner wird in den Ordner Gelöschte Objekte verschoben.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der zu löschenden Ordner verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Die Optionen **MoveToDeletedItems** und **HardDelete** sind transaktional, was bedeutet, dass jeweils ein Webdienstaufruf abgeschlossen ist, die Datenbank hat das Element in den Ordner Gelöschte Objekte verschoben oder dauerhaft entfernt das Element aus der Exchange-Datenbank. Dieses Verhalten gilt für MicrosoftExchange Server 2007 und Exchange Server 2010. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [DeleteFolder-Vorgang](deletefolder-operation.md)

