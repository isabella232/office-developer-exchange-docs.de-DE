---
title: DistinguishedFolderId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistinguishedFolderId
api_type:
- schema
ms.assetid: 50018162-2941-4227-8a5b-d6b4686bb32f
description: Das DistinguishedFolderId-Element identifiziert, Ordner, die nach Namen verwiesen werden können. Wenn Sie dieses Element nicht verwenden, müssen Sie das FolderId-Element verwenden, um einen Ordner zu identifizieren.
ms.openlocfilehash: 834166be3d882fa8c0533cfcc2999600430b82ce
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758076"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

Das **DistinguishedFolderId** -Element identifiziert, Ordner, die nach Namen verwiesen werden können. Wenn Sie dieses Element nicht verwenden, müssen Sie das [FolderId](folderid.md) -Element verwenden, um einen Ordner zu identifizieren. 
  
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
|**ChangeKey** <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die von dem **Id** -Attribut angegeben ist. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
#### <a name="id-attribute-values"></a>ID-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Stellt den Ordner Kalender.  <br/> |
|contacts  <br/> |Stellt den Ordner Kontakte dar.  <br/> |
|deleteditems  <br/> |Stellt den Ordner Gelöschte Objekte.  <br/> |
|Entwürfe  <br/> |Ordner "Entwürfe" darstellt.  <br/> |
|Posteingang  <br/> |Stellt den Ordner Posteingang dar.  <br/> |
|Journal  <br/> |Stellt den Ordner Journal dar.  <br/> |
|notes  <br/> |Stellt den Ordner Notizen dar.  <br/> |
|Postausgang  <br/> |Stellt den Ordner Postausgang.  <br/> |
|Gesendete Elemente  <br/> |Stellt den Ordner Gesendete Objekte.  <br/> |
|tasks  <br/> |Stellt den Ordner Aufgaben dar.  <br/> |
|msgfolderroot  <br/> |Stammverzeichnis der Nachricht darstellt.  <br/> |
|root  <br/> |Stellt den Stamm des Postfachs an.  <br/> |
|junkemail  <br/> |Stellt den Junk-e-Mail-Ordner dar.  <br/> |
|SearchFolders  <br/> |Ordner Suchordner darstellt.  <br/> |
|Voicemail  <br/> |Stellt den Voicemail-Ordner dar.  <br/> |
|recoverableitemsroot  <br/> |Stellt die Dumpster Stammordner.  <br/> |
|recoverableitemsdeletions  <br/> |Stellt die Dumpster Löschvorgänge Ordner.  <br/> |
|recoverableitemsversions  <br/> |Stellt die Dumpster Versionsordner.  <br/> |
|recoverableitemspurges  <br/> |Stellt die Dumpster Löscht ein Ordner.  <br/> |
|archiveroot  <br/> |Stellt den Stammordner Archiv.  <br/> |
|archivemsgfolderroot  <br/> |Stellt den Stammordner des Archivs Nachricht dar.  <br/> |
|archivedeleteditems  <br/> |Stellt den Archivordner für gelöschte Elemente.  <br/> |
|archiveinbox  <br/> |Stellt das Archiv Ordner Posteingang dar. Versionen von Exchange, beginnend mit Buildnummer 15.00.0913.09 enthalten dieser Wert.  <br/> |
|archiverecoverableitemsroot  <br/> |Stammordner Archiv wiederherstellbare Elemente darstellt.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Stellt den Archivordner wiederherstellbare Elemente löschen.  <br/> |
|archiverecoverableitemsversions  <br/> |Stellt den Archivordner wiederherstellbare Elemente Versionen.  <br/> |
|archiverecoverableitemspurges  <br/> |Stellt den Archivordner wiederherstellbare Elemente bereinigt.  <br/> |
|syncissues  <br/> |Stellt den Sync-Probleme-Ordner dar.  <br/> |
|Konflikte  <br/> |Stellt die Konfliktordner dar.  <br/> |
|localfailures  <br/> |Den Ordner Lokale Fehler darstellt.  <br/> |
|serverfailures  <br/> |Den Ordner Server Fehler darstellt.  <br/> |
|recipientcache  <br/> |Stellt den Ordner Empfängercache dar.  <br/> |
|QuickContacts  <br/> |Stellt den Ordner Schnellkontakte dar.  <br/> |
|conversationhistory  <br/> |Stellt den Ordner Unterhaltungsverlauf.  <br/> |
|adminauditlogs  <br/> |Stellt dem Administrator Audit Protokollordner.  <br/> |
|todosearch  <br/> |Stellt den Suchordner erledigen.  <br/> |
|mycontacts  <br/> |Stellt den Ordner Kontakte dar.  <br/> |
|Verzeichnis  <br/> |Stellt den Ordner Directory.  <br/> |
|imcontactlist  <br/> |Stellt den Instant Messaging-Kontaktliste-Ordner dar.  <br/> |
|peopleconnect  <br/> |Stellt die Personen verbinden Ordner.  <br/> |
|Favoriten  <br/> |Stellt den Ordner Favoriten.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Primäre SMTP-Adresse identifiziert. Proxyadressen sind nicht zulässig.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner, der für unterhaltungsaktionen gerichtet ist, die Ordner zu verwenden.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für die Kopie an, und verschieben Sie die unterhaltungsaktionen.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Identifiziert den Ordner, in dem ein neuer Ordner oder Element erstellt wird.  <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Ordner für die Suche für den [FindItem-Vorgang](finditem-operation.md) und den [FindFolder Vorgang](findfolder-operation.md)identifiziert.  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Stellt die Auflistung von Ordnern, die durchsucht werden, um den Inhalt eines Suchordners zu ermitteln.  <br/> |
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der Ordner kopieren, verschieben, abrufen, löschen oder Überwachen von Ereignissen verwendet werden.  <br/> |
|[FolderChange](folderchange.md) <br/> |Stellt eine Auflistung von Änderungen in einem gemeinsamen Ordner ausgeführt werden.  <br/> <br/>Es folgt der XPath-Ausdruck, der dieses Element:<br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[ToFolderId](tofolderid.md) <br/> | Stellt den Zielordner für eine kopierte oder verschobene Element oder einen Ordner.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[Des SavedItemFolderId](saveditemfolderid.md) <br/> | Identifiziert den Zielordner für Vorgänge, die zu aktualisieren, senden und Elemente im Exchange-Speicher zu erstellen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner, der zu synchronisierenden Elemente enthält.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Der Name eines Benutzers Configuration-Objekts darstellt. Der Benutzername des Configuration-Objekt ist der Bezeichner für eine Benutzer-Konfigurationsobjekt.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Stellt der ID des Ordners, e-Mail, um Elemente kopiert werden sollen.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Stellt der ID des Ordners die e-Mail, die Elemente in verschoben werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Eine **DistinguishedFolderId** in einer **FolderId**aufgelöst wird. 
  
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

