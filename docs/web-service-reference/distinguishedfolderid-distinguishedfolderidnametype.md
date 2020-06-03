---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: Das DistinguishedFolderId-Element identifiziert Ordner, auf die über den Namen verwiesen werden kann.
ms.openlocfilehash: ac239ec63f78322f6c82ab4be269d6fe4380dd8d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456192"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

Das **DistinguishedFolderId** -Element identifiziert Ordner, auf die über den Namen verwiesen werden kann. 
  
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
|[ContactsFolder](contactsfolder.md) <br/> |Gibt einen Kontakteordner an.  <br/> |
   
## <a name="text-value"></a>Textwert

**DistinguishedFolderId-Element Text Werte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Gibt die URL des Kalenderordners an.  <br/> |
|contacts  <br/> |Gibt die URL des Ordners Kontakte an.  <br/> |
|deleteditems  <br/> |Gibt die URL des Ordners "Gelöschte Elemente" an.  <br/> |
|Entwürfe  <br/> |Gibt die URL des Ordners Entwürfe an.  <br/> |
|Posteingang  <br/> |Gibt die URL des Posteingangsordners an.  <br/> |
|Journal  <br/> |Gibt die URL des Journal Ordners an.  <br/> |
|notes  <br/> |Gibt die URL des Ordners Notizen an.  <br/> |
|Postausgang  <br/> |Gibt die URL des Postausgangs Ordners an.  <br/> |
|SentItems  <br/> |Gibt die URL des Ordners "Gesendete Elemente" an.  <br/> |
|tasks  <br/> |Gibt die URL des Aufgabenordners an.  <br/> |
|msgfolderroot  <br/> |Gibt die URL des Nachrichten Stammordners an.  <br/> |
|publicfoldersroot  <br/> |Gibt die URL des Stammordners für Öffentliche Ordner an.  <br/> |
|root  <br/> |Gibt die URL des Stammordners an.  <br/> |
|JunkEmail  <br/> |Gibt die URL des Junk-e-Mail-Ordners an.  <br/> |
|searchfolders  <br/> |Gibt die URL der Suchordner an.  <br/> |
|voicemail  <br/> |Gibt die URL des Voice-Mail-Ordners an.  <br/> |
|recoverableitemsroot  <br/> |Gibt die URL des Stammordners "refundable Items" an.  <br/> |
|recoverableitemsdeletions  <br/> |Gibt die URL des Ordners Gelöschte Wiederherstellungselemente an.  <br/> |
|recoverableitemsversions  <br/> |Gibt die URL des Ordners "refundable Item Version" an.  <br/> |
|recoverableitemspurges  <br/> |Gibt die URL des Ordners "bereinigte Ordner für gelöschte Elemente" an.  <br/> |
|archiveroot  <br/> |Gibt die URL des Archivstamm Ordners an.  <br/> |
|archivemsgfolderroot  <br/> |Gibt die URL des Stammordners des archivierten Nachrichtenordners an.  <br/> |
|archivedeleteditems  <br/> |Gibt die URL des archivierten Ordners "Gelöschte Elemente" an.  <br/> |
|archiverecoverableitemsroot  <br/> |Gibt die URL des Stammordners für archivierte Wiederherstellungselemente an.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Gibt die URL des Ordners Archivierte Ordner für gelöschte Elemente an.  <br/> |
|archiverecoverableitemsversions  <br/> |Gibt die URL des Ordners "Archivierte Versionen der zurückstellbaren Elemente" an.  <br/> |
|archiverecoverableitemspurges  <br/> |Gibt die URL des archivierten Ordners "bereinigte gelöschte Elemente" an.  <br/> |
|SyncIssues  <br/> |Gibt die URL des Ordners Synchronisierungsprobleme an.  <br/> |
|Konflikte  <br/> |Gibt die URL des Ordners "Konflikte" an.  <br/> |
|LocalFailures  <br/> |Gibt die URL des lokalen Fehler Ordners an.  <br/> |
|ServerFailures  <br/> |Gibt die URL des Ordners "Serverfehler" an.  <br/> |
|recipientcache  <br/> |Gibt die URL des Empfängercache Ordners an.  <br/> |
|QuickContacts  <br/> |Gibt die URL des Ordners für schnell Kontakte an.  <br/> |
|conversationhistory  <br/> |Gibt die URL des Ordners unter Haltungs Verlauf an.  <br/> |
|adminauditlogs  <br/> |Gibt die URL des administrativen Überwachungsprotokoll Ordners an.  <br/> |
|todosearch  <br/> |Gibt die URL des Suchaufgaben Ordners an.  <br/> |
|MyContacts  <br/> |Gibt die URL des Ordners meine Kontakte an.  <br/> |
|Directory  <br/> |Gibt eine URL des Verzeichnisordners an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

