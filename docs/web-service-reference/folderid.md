---
title: FolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderId
api_type:
- schema
ms.assetid: 00d14e3e-4365-4f21-8f88-eaeea73b9bf7
description: Das FolderId-Element enthält den Schlüssel-ID und Ändern eines Ordners.
ms.openlocfilehash: 5764a164d5af183b8f313955ace5274dc6023a6a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758509"
---
# <a name="folderid"></a>FolderId

Das **FolderId** -Element enthält den Schlüssel-ID und Ändern eines Ordners. 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Enthält eine Zeichenfolge, die einen Ordner im Exchange-Speicher identifiziert. Dieses Attribut ist erforderlich.  <br/> |
|ChangeKey  <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem Id-Attribut angegeben ist. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner, der für Aktionen gerichtet ist, die Ordner zu verwenden.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für die Kopie an, und verschieben Sie Aktionen.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifiziert den Ordner, in einen neuen Ordner oder Element erstellt wird.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Stellt die Auflistung von Ordnern, die durchsucht werden wird, um den Inhalt des ein Suchordner bestimmen.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu löschen.  <br/> |
|[Folder](folder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach an.  <br/> |
|[FolderChange](folderchange.md) <br/> |Stellt eine Auflistung von Änderungen in einem gemeinsamen Ordner ausgeführt werden.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einem Kontaktordner in einem Postfach an.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach an.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Ordner in einem Postfach an.  <br/> |
|[ToFolderId](tofolderid.md) <br/> | Stellt den Zielordner für eine kopierte oder verschobene Element oder einen Ordner. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[Des SavedItemFolderId](saveditemfolderid.md) <br/> | Identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner, der zu synchronisierenden Elemente enthält.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Der Name eines Benutzers Configuration-Objekts darstellt. Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Identifiziert die ID des Ordners, den e-Mail-Elemente kopiert werden.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Identifiziert die ID des Ordners, den e-Mail-Elemente in verschoben werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Alle **FolderId** Elemente sind vom Typ **FolderIdType** . **FolderId** -Element muss in jedem Fall außer in Elemente, deren Typ die **BaseFolderType erweitert,** oder, in dem das **FolderId** -Element ist Teil einer Auswahl. Überprüfen Sie das Schema für Weitere Informationen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Erstellen von Ordnern (Exchange Web Services)](http://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

