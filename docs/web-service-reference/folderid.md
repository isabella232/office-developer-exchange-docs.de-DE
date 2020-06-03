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
description: Das Folder-ID-Element enthält den Bezeichner und den Änderungsschlüssel eines Ordners.
ms.openlocfilehash: 7aa5070fa7a2c51303c7159de04fe277f909a874
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461387"
---
# <a name="folderid"></a>FolderId

Das **Folder** -ID-Element enthält den Bezeichner und den Änderungsschlüssel eines Ordners. 
  
```XML
<FolderId Id="" ChangeKey="" />
```

 **FolderIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Enthält eine Zeichenfolge, die einen Ordner im Exchange-Informationsspeicher identifiziert. Dieses Attribut ist erforderlich.  <br/> |
|ChangeKey  <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das ID-Attribut identifiziert wird. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner an, der für Aktionen vorgesehen ist, die Ordner verwenden.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für die Aktionen kopieren und verlegen an.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Gibt den Ordner an, in dem ein neuer Ordner oder Element erstellt wird.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/>  <br/> `/CreateItem/ParentFolderId` <br/><br/>  `/CreateFolder/ParentFolderId` <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Stellt die Auflistung von Ordnern dar, die abgebaut werden, um den Inhalt eines Suchordners zu bestimmen.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.  <br/> |
|[Ordner](folder.md) <br/> |Stellt einen Ordner in einem Postfach dar.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Kalenderordner in einem Postfach dar.  <br/> |
|[FolderChange](folderchange.md) <br/> |Stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/UpdateFolder/FolderChanges/FolderChange` <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einen Kontaktordner in einem Postfach dar.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach dar.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner in einem Postfach dar.  <br/> |
|[Tofolder-Datei](tofolderid.md) <br/> | Stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner dar. <br/> <br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/MoveFolder/ToFolderId` <br/> <br/> `/CopyFolder/ToFolderId` <br/> <br/> `/MoveItem/ToFolderId`<br/> <br/>  `/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/CreateItem/SavedItemFolderId` <br/><br/>  `/UpdateItem/SavedItemFolderId` <br/><br/>  `/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Stellt den Namen eines Benutzer Konfigurationsobjekts dar. Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Gibt die ID des Ordners an, in den e-Mail-Elemente kopiert werden.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Gibt die ID des Ordners an, in den e-Mail-Elemente verschoben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Alle **folderl** -Elemente haben den **FolderIdType** -Typ. Das **folderl** -Element ist in jedem Fall erforderlich, außer in Elementen, deren Typ das **BaseFolderType** -Element erweitert oder in dem das **Folder** -Element ein Teil einer Auswahl ist. Lesen Sie das Schema, um weitere Informationen zu erhalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Erstellen von Ordnern (Exchange Webdienste)](https://msdn.microsoft.com/library/3b15b0ec-8691-45ed-9a24-a91ff732d6cf%28Office.15%29.aspx)

