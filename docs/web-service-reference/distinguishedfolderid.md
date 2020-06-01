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
description: Das DistinguishedFolderId-Element identifiziert Ordner, auf die über den Namen verwiesen werden kann. Wenn Sie dieses Element nicht verwenden, müssen Sie das foldercode-Element verwenden, um einen Ordner zu identifizieren.
ms.openlocfilehash: be883cbca00910b24e4c45ba047803e5a5024566
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462696"
---
# <a name="distinguishedfolderid"></a>DistinguishedFolderId

Das **DistinguishedFolderId** -Element identifiziert Ordner, auf die über den Namen verwiesen werden kann. Wenn Sie dieses Element nicht verwenden, müssen Sie das [foldercode](folderid.md) -Element verwenden, um einen Ordner zu identifizieren. 
  
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
|**ChangeKey** <br/> |Enthält eine Zeichenfolge, die eine Version eines Ordners identifiziert, die durch das **ID-** Attribut identifiziert wird. Dieses Attribut ist optional. Verwenden Sie dieses Attribut, um sicherzustellen, dass die richtige Version eines Ordners verwendet wird.  <br/> |
   
#### <a name="id-attribute-values"></a>ID-Attributwerte

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Stellt den Ordner Kalender dar.  <br/> |
|contacts  <br/> |Stellt den Ordner Kontakte dar.  <br/> |
|deleteditems  <br/> |Stellt den Ordner Gelöschte Elemente dar.  <br/> |
|Entwürfe  <br/> |Stellt den Ordner Entwürfe dar.  <br/> |
|Posteingang  <br/> |Stellt den Ordner Posteingang dar.  <br/> |
|Journal  <br/> |Stellt den Ordner Journal dar.  <br/> |
|notes  <br/> |Stellt den Ordner Notizen dar.  <br/> |
|Postausgang  <br/> |Stellt den Ordner Postausgang dar.  <br/> |
|SentItems  <br/> |Stellt den Ordner "Gesendete Elemente" dar.  <br/> |
|tasks  <br/> |Stellt den Ordner Aufgaben dar.  <br/> |
|msgfolderroot  <br/> |Stellt den Nachrichten Ordner Stamm dar.  <br/> |
|root  <br/> |Stellt den Stamm des Postfachs dar.  <br/> |
|JunkEmail  <br/> |Stellt den Junk-e-Mail-Ordner dar.  <br/> |
|searchfolders  <br/> |Stellt den Ordner Suchordner dar.  <br/> |
|voicemail  <br/> |Stellt den Ordner Voicemail dar.  <br/> |
|recoverableitemsroot  <br/> |Stellt den Ordner "Papierkorb Stamm" dar.  <br/> |
|recoverableitemsdeletions  <br/> |Stellt den Ordner Papierkorb Löschungen dar.  <br/> |
|recoverableitemsversions  <br/> |Stellt den Ordner Papierkorb Versionen dar.  <br/> |
|recoverableitemspurges  <br/> |Stellt den Ordner Papierkorb-Löschvorgänge dar.  <br/> |
|archiveroot  <br/> |Stellt den Stamm Archivordner dar.  <br/> |
|archivemsgfolderroot  <br/> |Stellt den Nachrichten Ordner des Stamm Archivs dar.  <br/> |
|archivedeleteditems  <br/> |Stellt den Ordner Gelöschte Elemente archivieren dar.  <br/> |
|archiveinbox  <br/> |Stellt den Archiv Posteingangsordner dar. Versionen von Exchange, beginnend mit Buildnummer 15.00.0913.09, enthalten diesen Wert.  <br/> |
|archiverecoverableitemsroot  <br/> |Stellt den Stammordner für den Archiv Wiederherstellungselemente dar.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Stellt den Ordner "gelöschte Archive für gelöschte Elemente" dar.  <br/> |
|archiverecoverableitemsversions  <br/> |Stellt den Ordner "Archive refundable Items-Versionen" dar.  <br/> |
|archiverecoverableitemspurges  <br/> |Stellt den Ordner "Wiederherstellungs fähige Elemente archivieren" dar.  <br/> |
|SyncIssues  <br/> |Stellt den Ordner Synchronisierungsprobleme dar.  <br/> |
|Konflikte  <br/> |Stellt den Ordner Konflikte dar.  <br/> |
|LocalFailures  <br/> |Stellt den Ordner Lokale Fehler dar.  <br/> |
|ServerFailures  <br/> |Stellt den Ordner Serverfehler dar.  <br/> |
|recipientcache  <br/> |Stellt den Empfängercache Ordner dar.  <br/> |
|QuickContacts  <br/> |Stellt den Ordner "Quick Contacts" dar.  <br/> |
|conversationhistory  <br/> |Stellt den Ordner Unterhaltungsverlauf dar.  <br/> |
|adminauditlogs  <br/> |Stellt den Ordner Administrator-Überwachungsprotokolle dar.  <br/> |
|todosearch  <br/> |Stellt den TODO-Suchordner dar.  <br/> |
|MyContacts  <br/> |Stellt den Ordner Meine Kontakte dar.  <br/> |
|Directory  <br/> |Stellt den Verzeichnis Ordner dar.  <br/> |
|imcontactlist  <br/> |Stellt den Ordner "im Contact List" dar.  <br/> |
|peopleconnect  <br/> |Stellt den Ordner Personen Verbindung dar.  <br/> |
|Favoriten  <br/> |Stellt den Ordner Favoriten dar.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Postfach](mailbox.md) <br/> |Identifiziert eine primäre SMTP-Adresse. Proxy Adressen sind nicht zulässig.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ContextFolderId](contextfolderid.md) <br/> |Gibt den Ordner an, der für Unterhaltungs Aktionen vorgesehen ist, die Ordner verwenden.  <br/> |
|[DestinationFolderId](destinationfolderid.md) <br/> |Gibt den Zielordner für die Aktionen zum Kopieren und verlegen von Unterhaltungen an.  <br/> |
|[ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) <br/> | Gibt den Ordner an, in dem ein neuer Ordner oder Element erstellt wird.  <br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/CreateItem/ParentFolderId` <br/><br/>`/CreateFolder/ParentFolderId` <br/> |
|[ParentFolderIds](parentfolderids.md) <br/> |Identifiziert Ordner für die Suche nach dem [FindItem-Vorgang](finditem-operation.md) und dem FindFolder- [Vorgang](findfolder-operation.md).  <br/> |
|[BaseFolderIds](basefolderids.md) <br/> |Stellt die Auflistung von Ordnern dar, die durchsucht werden, um den Inhalt eines Suchordners zu bestimmen.  <br/> |
|[FolderIds](folderids.md) <br/> |Enthält ein Array von Ordner Bezeichnern, die zum Identifizieren von Ordnern zum Kopieren, migrieren, abrufen, löschen oder Überwachen von Ereignisbenachrichtigungen verwendet werden.  <br/> |
|[FolderChange](folderchange.md) <br/> |Stellt eine Auflistung von Änderungen dar, die für einen einzelnen Ordner ausgeführt werden sollen.  <br/> <br/>Für dieses Element wird folgender XPath-Ausdruck verwendet: <br/><br/>`/UpdateFolder/FolderChanges/FolderChange`<br/> |
|[Tofolder-Datei](tofolderid.md) <br/> | Stellt den Zielordner für ein kopiertes oder verschobenes Element oder einen verschobenen Ordner dar.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/MoveFolder/ToFolderId`<br/><br/>`/CopyFolder/ToFolderId`<br/><br/>`/MoveItem/ToFolderId`<br/><br/>`/CopyItem/ToFolderId` <br/> |
|[SavedItemFolderId](saveditemfolderid.md) <br/> | Identifiziert den Zielordner für Vorgänge, die Elemente im Exchange-Informationsspeicher aktualisieren, senden und erstellen.<br/><br/>Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>`/CreateItem/SavedItemFolderId`<br/><br/>`/UpdateItem/SavedItemFolderId`<br/><br/>`/SendItem/SavedItemFolderId` <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält.  <br/> |
|[UserConfigurationName](userconfigurationname.md) <br/> |Stellt den Namen eines Benutzer Konfigurationsobjekts dar. Der Benutzer Konfigurationsobjekt Name ist der Bezeichner für ein Benutzer Konfigurationsobjekt.  <br/> |
|[CopyToFolder](copytofolder.md) <br/> |Stellt die ID des Ordners dar, in den e-Mail-Elemente kopiert werden.  <br/> |
|[MoveToFolder](movetofolder.md) <br/> |Stellt die ID des Ordners dar, in den e-Mail-Elemente verschoben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Ein **DistinguishedFolderId** wird in eine **Ordner**-Nr aufgelöst. 
  
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

