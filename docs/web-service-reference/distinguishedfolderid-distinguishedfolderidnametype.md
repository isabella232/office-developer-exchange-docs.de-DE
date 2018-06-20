---
title: DistinguishedFolderId (DistinguishedFolderIdNameType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 915b2ee9-8284-4bf6-8995-1fd0785e9e48
description: Das DistinguishedFolderId-Element identifiziert, Ordner, die nach Namen verwiesen werden können.
ms.openlocfilehash: 1f5b97fc7ee7b93989762c26e4b979a8dfb884be
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758074"
---
# <a name="distinguishedfolderid-distinguishedfolderidnametype"></a>DistinguishedFolderId (DistinguishedFolderIdNameType)

Das **DistinguishedFolderId** -Element identifiziert, Ordner, die nach Namen verwiesen werden können. 
  
```XML
<DistinguishedFolderId> calendar | contacts | deleteditems | drafts | inbox | journal | notes | outbox | sentitems | tasks | msgfolderroot | publicfoldersroot | root | junkemail | searchfolders | voicemail | recoverableitemsroot | recoverableitemsdeletions | recoverableitemsversions | recoverableitemspurges | archiveroot | archivemsgfolderroot | archivedeleteditems | archiverecoverableitemsroot | archiverecoverableitemsdeletions | archiverecoverableitemsversions | archiverecoverableitemspurges | syncissues | conflicts | localfailures | serverfailures | recipientcache | quickcontacts | conversationhistory | adminauditlogs | todosearch | mycontacts | directory | imcontactlist | peopleconnect</DistinguishedFolderId>
```

 **DistinguishedFolderIdNameType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Gibt einen generischen Ordner.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Gibt einen Kalenderordner.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Gibt einen Kontakteordner.  <br/> |
   
## <a name="text-value"></a>Textwert

**Text-Elementwerte DistinguishedFolderId**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|Kalender  <br/> |Gibt die URL des Kalenderordners an.  <br/> |
|contacts  <br/> |Gibt die URL des Kontaktordners.  <br/> |
|deleteditems  <br/> |Gibt die URL des Ordners "Gelöschte Elemente" an.  <br/> |
|Entwürfe  <br/> |Gibt die URL der Ordner "Entwürfe" an.  <br/> |
|Posteingang  <br/> |Gibt die URL des Ordners Posteingang an.  <br/> |
|Journal  <br/> |Gibt die URL des Ordners Journal an.  <br/> |
|notes  <br/> |Gibt die URL der Ordner "Notizen" an.  <br/> |
|Postausgang  <br/> |Gibt die URL des Ordners Postausgang.  <br/> |
|Gesendete Elemente  <br/> |Gibt die URL der Ordner "Gesendete Elemente" an.  <br/> |
|tasks  <br/> |Gibt die URL des Aufgabenordners an.  <br/> |
|msgfolderroot  <br/> |Gibt die URL des Stammordners Nachricht an.  <br/> |
|publicfoldersroot  <br/> |Gibt die URL des Stammordners Öffentliche Ordner an.  <br/> |
|root  <br/> |Gibt die URL des Stammordners an.  <br/> |
|junkemail  <br/> |Gibt die URL des junk-e-Mail-Ordners an.  <br/> |
|SearchFolders  <br/> |Gibt die URL der Suchordner an.  <br/> |
|Voicemail  <br/> |Gibt die URL des Voicemail Ordners an.  <br/> |
|recoverableitemsroot  <br/> |Gibt die URL des Stammordners wiederherstellbare Elemente an.  <br/> |
|recoverableitemsdeletions  <br/> |Gibt die URL des Ordners "Gelöschte wiederherstellbare Elemente" an.  <br/> |
|recoverableitemsversions  <br/> |Gibt die URL des Versionsordners Wiederherstellbares Element an.  <br/> |
|recoverableitemspurges  <br/> |Gibt die URL des Ordners wiederherstellbare Elemente endgültig gelöscht.  <br/> |
|archiveroot  <br/> |Gibt die URL des Stammordners Archiv an.  <br/> |
|archivemsgfolderroot  <br/> |Gibt die URL des Stammordners archivierte Nachricht Ordner an.  <br/> |
|archivedeleteditems  <br/> |Gibt die URL des Ordners archivierten gelöschte Elemente an.  <br/> |
|archiverecoverableitemsroot  <br/> |Gibt die URL des Stammordners archivierten wiederherstellbare Elemente an.  <br/> |
|archiverecoverableitemsdeletions  <br/> |Gibt die URL des Ordners archivierten wiederherstellbare gelöschte Elemente an.  <br/> |
|archiverecoverableitemsversions  <br/> |Gibt die URL des Ordners wiederherstellbare Elemente archivierten Versionen an.  <br/> |
|archiverecoverableitemspurges  <br/> |Gibt die URL des Ordners archivierten Zeitfenster wiederherstellbare Elemente an.  <br/> |
|syncissues  <br/> |Gibt die URL des Ordners Synchronisierung Probleme an.  <br/> |
|Konflikte  <br/> |Gibt die URL des Ordners Konflikte an.  <br/> |
|localfailures  <br/> |Gibt die URL des Ordners lokale Fehler an.  <br/> |
|serverfailures  <br/> |Gibt die URL des Ordners mit Fehlern Server an.  <br/> |
|recipientcache  <br/> |Gibt die URL des Ordners Empfängercache an.  <br/> |
|QuickContacts  <br/> |Gibt die URL des Ordners Schnellkontakte an.  <br/> |
|conversationhistory  <br/> |Gibt die URL der dem Verlaufsordner Unterhaltung an.  <br/> |
|adminauditlogs  <br/> |Gibt die URL des Ordners administrative Audit Log an.  <br/> |
|todosearch  <br/> |Gibt die URL des Suchordners Aufgabe an.  <br/> |
|mycontacts  <br/> |Gibt die URL der an den Kontakteordner.  <br/> |
|Verzeichnis  <br/> |Gibt eine URL des Verzeichnisses an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

