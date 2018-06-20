---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: Das FolderIds-Element enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der Ordner kopieren, verschieben, abrufen, löschen oder Überwachen von Ereignissen verwendet werden.
ms.openlocfilehash: 911a74ca778ee988c270c16c67620a40656d82d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758507"
---
# <a name="folderids"></a>FolderIds

Das **FolderIds** -Element enthält ein Array von Bezeichnern für Ordner, die zum Identifizieren der Ordner kopieren, verschieben, abrufen, löschen oder Überwachen von Ereignissen verwendet werden. 
  
```xml
<FolderIds>
   <FolderId/>
   <DistinguishedFolderId/>
</FolderIds>
```

 **NonEmptyArrayOfBaseFolderIdsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert die Microsoft Exchange Server-Ordner, die nach Namen verwiesen werden können.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Definiert eine Anforderung an einen Ordner aus dem Exchange-Speicher abzurufen.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Speicher.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu verschieben.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Definiert eine Anforderung an einen Ordner im Exchange-Speicher zu kopieren.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages und http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichten-schema Typen-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd; Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFolder Operation](getfolder-operation.md)
  
[DeleteFolder-Vorgang](deletefolder-operation.md)
  
[MoveFolder-Vorgang](movefolder-operation.md)
  
[CopyFolder-Vorgang](copyfolder-operation.md)
  
[Vorgang abonnieren](subscribe-operation.md)

