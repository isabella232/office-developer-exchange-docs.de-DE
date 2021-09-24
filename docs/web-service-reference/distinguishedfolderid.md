---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: Das DistinguishedFolderId-Element identifiziert Ordner, auf die anhand des Namens verwiesen werden kann. Wenn Sie dieses Element nicht verwenden, müssen Sie das FolderId-Element verwenden, um einen Ordner zu identifizieren.
ms.openlocfilehash: 309db925bb783c435320aeb283915ece39da2271
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521996"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

Das **DistinguishedFolderId-Element** identifiziert Ordner, auf die anhand des Namens verwiesen werden kann. Wenn Sie dieses Element nicht verwenden, müssen Sie das [FolderId-Element](folderid.md) verwenden, um einen Ordner zu identifizieren. 
  
```XML
<DistinguishedFolderId Id="" ChangeKey="">
   <Mailbox/>
</DistinguishedFolderId>
```

 **DistinguishedFolderIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Enthält eine Zeichenfolge, die einen Standardordner identifiziert. Dieses Attribut ist erforderlich.  <br/> |
|**ChangeKey** <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, der durch das **Id-Attribut** identifiziert wird. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
#### <a name="id-attribute-values"></a>Id-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Stellt den Ordner "Kalender" dar.  <br/> |
|contacts  <br/> |Stellt den Ordner Kontakte dar.  <br/> |
|deleteditems  <br/> |Stellt den Ordner "Gelöschte Elemente" dar.  <br/> |
|Entwürfe  <br/> |Stellt den Ordner Entwürfe dar.  <br/> |
|Posteingang  <br/> |Stellt den Ordner Posteingang dar.  <br/> |
|Journal  <br/> |Stellt den Ordner Journal dar.  <br/> |
|notes  <br/> |Stellt den Ordner Notizen dar.  <br/> |
|Postausgang  <br/> |Stellt den Ordner Postausgang dar.  <br/> |
|SentItems  <br/> |Stellt den Ordner "Gesendete Elemente" dar.  <br/> |
|tasks  <br/> |Stellt den Ordner "Aufgaben" dar.  <br/> |
|msgfolderroot  <br/> |Stellt den Stamm des Nachrichtenordners dar.  <br/> |
|root  <br/> |Stellt den Stamm des Postfachs dar.  <br/> |
|JunkEmail  <br/> |Stellt den Junk-E-Mail-Ordner dar.  <br/> |
|searchfolders  <br/> |Stellt den Ordner "Suchordner" dar.  <br/> |
|voicemail  <br/> |Stellt den Voicemailordner dar.  <br/> |
|recoverableitemsroot  <br/> |Stellt den Dumpsterstammordner dar.  <br/> |
|recoverableitemsdeletions  <br/> |Stellt den Ordner "Dumpsterlöschungen" dar.  <br/> |
|recoverableitemsversions  <br/> |Stellt den Ordner "Dumpsterversionen" dar.  <br/> |
|recoverableitemspurges  <br/> |Represents the dumpster purster purges folder.  <br/> |
|archiveroot  <br/> |Stellt den Stammarchivordner dar.  <br/> |
|archivemsgfolderroot  <br/> |Stellt den Stammarchiv-Nachrichtenordner dar.  <br/> |
|archivedeleteditems  <br/> |Stellt den Ordner "Gelöschte Elemente im Archiv" dar.  <br/> |
|archiveinbox  <br/> |Stellt den Ordner "Posteingang archivieren" dar. Versionen von Exchange ab Buildnummer 15.00.0913.09 enthalten diesen Wert.  <br/> |
|archiverecoverableitemsroot  <br/> |Stellt den Stammordner für wiederherstellbare Elemente des Archivs dar.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Stellt den Ordner zum Löschen von wiederherstellbaren Elementen dar.  <br/> |
|archiverecoverableitemsversions  <br/> |Stellt den Ordner "Versionsordner für wiederherstellbare Elemente" dar.  <br/> |
|archiverecoverableitemspurges  <br/> |Represents the archive recoverable items purges folder.  <br/> |
|SyncIssues  <br/> |Stellt den Ordner für Synchronisierungsprobleme dar.  <br/> |
|Konflikte  <br/> |Stellt den Ordner "Konflikte" dar.  <br/> |
|LocalFailures  <br/> |Stellt den Ordner "Lokale Fehler" dar.  <br/> |
|ServerFailures  <br/> |Stellt den Ordner "Serverfehler" dar.  <br/> |
|recipientcache  <br/> |Stellt den Empfängercacheordner dar.  <br/> |
|Quickcontacts  <br/> |Stellt den Schnellkontaktordner dar.  <br/> |
|conversationhistory  <br/> |Stellt den Unterhaltungsverlaufsordner dar.  <br/> |
|adminauditlogs  <br/> |Stellt den Ordner "Administratorüberwachungsprotokolle" dar.  <br/> |
|todosearch  <br/> |Stellt den Todo-Suchordner dar.  <br/> |
|mycontacts  <br/> |Stellt den Ordner "Meine Kontakte" dar.  <br/> |
|Verzeichnis  <br/> |Stellt den Verzeichnisordner dar.  <br/> |
|Imcontactlist  <br/> |Stellt den Kontaktlistenordner für Chatnachrichten dar.  <br/> |
|peopleconnect  <br/> |Stellt den Ordner "Personen verbinden" dar.  <br/> |
|Favoriten  <br/> |Stellt den Ordner "Favoriten" dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert eine primäre SMTP-Adresse. Proxyadressen sind nicht zulässig.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner an, der für Unterhaltungsaktionen bestimmt ist, die Ordner verwenden.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für Aktionen zum Kopieren und Verschieben von Unterhaltungen an.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Gibt den Ordner an, in dem ein neuer Ordner oder ein neues Element erstellt wird.  <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifies folders to search for the [FindItem operation](finditem-operation.md) and the [FindFolder operation](findfolder-operation.md).  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Stellt die Auflistung von Ordnern dar, die durchsucht werden, um den Inhalt eines Suchordners zu ermitteln.  <br/> |
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von Ordnern verwendet werden, die kopiert, verschoben, abgerufen, gelöscht oder auf Ereignisbenachrichtigungen überwacht werden sollen.  <br/> |
|[FolderChange](folderchange.md) <br/> |Stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.  <br/> <br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | Stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner dar.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange Speicher aktualisieren, senden und erstellen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Stellt den Namen eines Benutzerkonfigurationsobjekts dar. Der Name des Benutzerkonfigurationsobjekts ist der Bezeichner für ein Benutzerkonfigurationsobjekt.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Stellt die ID des Ordners dar, in den E-Mail-Elemente kopiert werden.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Stellt die ID des Ordners dar, in den E-Mail-Elemente verschoben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Eine **DistinguishedFolderId** wird in eine **FolderId** aufgelöst. 
  
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

