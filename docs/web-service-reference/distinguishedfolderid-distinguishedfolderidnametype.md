---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: Das DistinguishedFolderId-Element identifiziert Ordner, auf die anhand des Namens verwiesen werden kann.
ms.openlocfilehash: 23d1dead5a97fe8b2ceb29235f4b784f667d2ee1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526440"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

Das **DistinguishedFolderId-Element** identifiziert Ordner, auf die anhand des Namens verwiesen werden kann. 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keines
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Gibt einen generischen Ordner an.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Gibt einen Kalenderordner an.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Gibt einen Kontaktordner an.  <br/> |
   
## <a name="text-value"></a>Textwert

**DistinguishedFolderId-Elementtextwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Gibt die URL des Kalenderordners an.  <br/> |
|contacts  <br/> |Gibt die URL des Kontaktordners an.  <br/> |
|deleteditems  <br/> |Gibt die URL des Ordners für gelöschte Elemente an.  <br/> |
|Entwürfe  <br/> |Gibt die URL des Ordners "Entwürfe" an.  <br/> |
|Posteingang  <br/> |Gibt die URL des Posteingangsordners an.  <br/> |
|Journal  <br/> |Gibt die URL des Journalordners an.  <br/> |
|notes  <br/> |Gibt die URL des Notizenordners an.  <br/> |
|Postausgang  <br/> |Gibt die URL des Postausgangsordners an.  <br/> |
|SentItems  <br/> |Gibt die URL des Ordners "Gesendete Elemente" an.  <br/> |
|tasks  <br/> |Gibt die URL des Aufgabenordners an.  <br/> |
|msgfolderroot  <br/> |Gibt die URL des Nachrichtenstammordners an.  <br/> |
|publicfoldersroot  <br/> |Gibt die URL des Stammordners für öffentliche Ordner an.  <br/> |
|root  <br/> |Gibt die URL des Stammordners an.  <br/> |
|JunkEmail  <br/> |Gibt die URL des Junk-E-Mail-Ordners an.  <br/> |
|searchfolders  <br/> |Gibt die URL der Suchordner an.  <br/> |
|voicemail  <br/> |Gibt die URL des Voicemailordners an.  <br/> |
|recoverableitemsroot  <br/> |Gibt die URL des Stammordners für wiederherstellbare Elemente an.  <br/> |
|recoverableitemsdeletions  <br/> |Gibt die URL des Ordners für gelöschte wiederherstellbare Elemente an.  <br/> |
|recoverableitemsversions  <br/> |Gibt die URL des Ordners "Versionen des wiederherstellbaren Elements" an.  <br/> |
|recoverableitemspurges  <br/> |Gibt die URL des Ordners für gelöschte wiederherstellbare Elemente an.  <br/> |
|archiveroot  <br/> |Gibt die URL des Archivstammordners an.  <br/> |
|archivemsgfolderroot  <br/> |Gibt die URL des Stammordners des archivierten Nachrichtenordners an.  <br/> |
|archivedeleteditems  <br/> |Gibt die URL des archivierten Ordners für gelöschte Elemente an.  <br/> |
|archiverecoverableitemsroot  <br/> |Gibt die URL des archivierten Stammordners für wiederherstellbare Elemente an.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Gibt die URL des archivierten Ordners für wiederherstellbare gelöschte Elemente an.  <br/> |
|archiverecoverableitemsversions  <br/> |Gibt die URL des Ordners für archivierte Versionen von Wiederherstellbaren Elementen an.  <br/> |
|archiverecoverableitemspurges  <br/> |Gibt die URL des archivierten Ordners für gelöschte wiederherstellbare Elemente an.  <br/> |
|SyncIssues  <br/> |Gibt die URL des Ordners für Synchronisierungsprobleme an.  <br/> |
|Konflikte  <br/> |Gibt die URL des Konfliktordners an.  <br/> |
|LocalFailures  <br/> |Gibt die URL des Ordners für lokale Fehler an.  <br/> |
|ServerFailures  <br/> |Gibt die URL des Ordners "Serverfehler" an.  <br/> |
|recipientcache  <br/> |Gibt die URL des Empfängercacheordners an.  <br/> |
|Quickcontacts  <br/> |Gibt die URL des Schnellkontaktordners an.  <br/> |
|conversationhistory  <br/> |Gibt die URL des Unterhaltungsverlaufsordners an.  <br/> |
|adminauditlogs  <br/> |Gibt die URL des administrativen Überwachungsprotokollordners an.  <br/> |
|todosearch  <br/> |Gibt die URL des Aufgabenordners für die Suche an.  <br/> |
|mycontacts  <br/> |Gibt die URL des Ordners "Meine Kontakte" an.  <br/> |
|Verzeichnis  <br/> |Gibt eine URL des Verzeichnisordners an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

