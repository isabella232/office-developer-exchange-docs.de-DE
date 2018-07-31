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
description: Das Ordner-Element enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.
ms.openlocfilehash: 34372f2480825c7a9977eeae8e730c201307f36b
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353588"
---
# <a name="folders"></a>Ordner

Das **Ordner** -Element enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden. 
  
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
|[Folder](folder.md) <br/> |Gibt einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontakteordner in einem Postfach an.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach enthalten.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner in einem Postfach an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopyFolderResponseMessage](copyfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [CopyFolder-Vorgang](copyfolder-operation.md) .  <br/> |
|[CreateFolder](createfolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu erstellen.  <br/> |
|[CreateFolderResponseMessage](createfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [CreateFolder-Vorgang](createfolder-operation.md) .  <br/> |
|[CreateManagedFolderResponseMessage](createmanagedfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [CreateManagedFolder Vorgang](createmanagedfolder-operation.md) .  <br/> |
|[GetFolderResponseMessage](getfolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [GetFolder-Vorgang](getfolder-operation.md) .  <br/> |
|[MoveFolderResponseMessage](movefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung [MoveFolder-Vorgang](movefolder-operation.md) .  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> |Identifiziert den Ordner, in dem ein neuer Ordner erstellt wird.  <br/> |
|[RootFolder (FindFolderResponseMessage)](rootfolder-findfolderresponsemessage.md) <br/> |Enthält die Ergebnisse einen einzelner Stammordner während eines [Vorgangs FindFolder](findfolder-operation.md)zu suchen.  <br/> |
|[UpdateFolderResponseMessage](updatefolderresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen Anforderung [UpdateFolder Vorgang](updatefolder-operation.md) .  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist ein erforderliches untergeordnetes Element des Elements [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) . 
  
Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md)

