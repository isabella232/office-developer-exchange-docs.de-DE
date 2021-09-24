---
title: FolderIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- FolderIds
api_type:
- schema
ms.assetid: 3ff9d15a-7220-4785-ae6b-583a7eb82005
description: Das FolderIds-Element enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von Ordnern verwendet werden, die kopiert, verschoben, abgerufen, gelöscht oder auf Ereignisbenachrichtigungen überwacht werden sollen.
ms.openlocfilehash: 7c0cf46d5fdaf35ec72cf3b5750b51edc5a8bfe0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59518365"
---
# <a name="folderids"></a>FolderIds

Das **FolderIds-Element** enthält ein Array von Ordnerbezeichnern, die zum Identifizieren von Ordnern verwendet werden, die kopiert, verschoben, abgerufen, gelöscht oder auf Ereignisbenachrichtigungen überwacht werden sollen. 
  
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
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert Microsoft Exchange Server Ordner, auf die anhand des Namens verwiesen werden kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Definiert eine Anforderung zum Abrufen eines Ordners aus dem Exchange Speicher.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange Speicher.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange Speicher.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Definiert eine Anforderung zum Verschieben eines Ordners im Exchange Speicher.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Definiert eine Anforderung zum Kopieren eines Ordners im Exchange Speicher.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Push-basiertes Ereignisbenachrichtigungsabonnement dar.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein pullbasiertes Ereignisbenachrichtigungsabonnement dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages und https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema; Typenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd; Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFolder-Vorgang](getfolder-operation.md)
  
[DeleteFolder-Vorgang](deletefolder-operation.md)
  
[MoveFolder-Vorgang](movefolder-operation.md)
  
[CopyFolder-Vorgang](copyfolder-operation.md)
  
[Vorgang abonnieren](subscribe-operation.md)

