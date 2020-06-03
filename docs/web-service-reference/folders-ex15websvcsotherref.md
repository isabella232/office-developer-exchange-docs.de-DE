---
title: Ordner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folders
api_type:
- schema
ms.assetid: 8e71cb44-1df6-444a-add7-0c1363863f65
description: Das Folders-Element enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.
ms.openlocfilehash: b087be0501f04390b80458458e7e7ccc24bf27bd
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530979"
---
# <a name="folders"></a>Ordner

Das **Folders** -Element enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden. 
  
```xml
<Folders>
   <Folder/>
</Folders>
```

```xml
<Folders>
   <ContactsFolder/> 
</Folders>
```

```xml
<Folders>
   <TasksFolder/>
</Folders>
```

```xml
<Folders>
   <CalendarFolder/>
</Folders>
```

```xml
<Folders>
   <SearchFolder/> 
</Folders>
```

**ArrayOfFoldersType** oder **NonEmptyArrayOfFoldersType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Gibt einen Ordner zum Erstellen, abrufen, suchen, synchronisieren oder aktualisieren an.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner dar, der in erster Linie Kalenderelemente enthält.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Ordner Kontakte in einem Postfach dar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen in einem Postfach enthaltenen Suchordner dar.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner in einem Postfach dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [CopyFolder-Vorgangs](copyfolder-operation.md) Anforderung.  <br/> |
|[CreateFolder](createfolder.md) <br/> |Definiert eine Anforderung zum Erstellen eines Ordners im Exchange-Informationsspeicher.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [CreateFolder-Vorgangs](createfolder-operation.md) Anforderung.  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [CreateManagedFolder-Vorgangs](createmanagedfolder-operation.md) Anforderung.  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [GetFolder-Vorgangs](getfolder-operation.md) Anforderung.  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [MoveFolder-Vorgangs](movefolder-operation.md) Anforderung.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Gibt den Ordner an, in dem ein neuer Ordner erstellt wird.  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |Enthält die Ergebnisse der Suche eines einzelnen Stammordners während eines [FindFolder-Vorgangs](findfolder-operation.md).  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen [UpdateFolder-Vorgangs](updatefolder-operation.md) Anforderung.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist ein erforderliches untergeordnetes Element des [parentfolderid-Elements (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) . 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

