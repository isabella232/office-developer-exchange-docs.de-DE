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
description: Das FolderIds-Element enthält ein Array von Ordner Bezeichnern, mit denen Ordner identifiziert werden, die zum Kopieren, verlegen, abrufen, löschen oder Überwachen von Ereignisbenachrichtigungen verwendet werden.
ms.openlocfilehash: ff0476f72c7da088bd2b39f58ab560dcc82197e4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530993"
---
# <a name="folderids"></a>FolderIds

Das **FolderIds** -Element enthält ein Array von Ordner Bezeichnern, mit denen Ordner identifiziert werden, die zum Kopieren, verlegen, abrufen, löschen oder Überwachen von Ereignisbenachrichtigungen verwendet werden. 
  
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
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> |Identifiziert Exchange Server Ordner, auf die über den Namen verwiesen werden kann.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetFolder](getfolder.md) <br/> |Definiert eine Anforderung zum Abrufen eines Ordners aus dem Exchange-Informationsspeicher.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/GetFolder` <br/> |
|[DeleteFolder](deletefolder.md) <br/> |Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Informationsspeicher.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/DeleteFolder` <br/> |
|[EmptyFolder](emptyfolder.md) <br/> |Definiert eine Anforderung zum Löschen von Ordnern aus dem Exchange-Informationsspeicher.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/EmptyFolder` <br/> |
|[MoveFolder](movefolder.md) <br/> |Definiert eine Anforderung zum Migrieren eines Ordners in der Exchange-Informationsspeicher.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/MoveFolder` <br/> |
|[CopyFolder](copyfolder.md) <br/> |Definiert eine Anforderung zum Kopieren eines Ordners in der Exchange-Informationsspeicher.  <br/> Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/CopyFolder` <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.  <br/> |
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages und https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema; Typenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd; Types. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetFolder-Vorgang](getfolder-operation.md)
  
[DeleteFolder-Vorgang](deletefolder-operation.md)
  
[MoveFolder-Vorgang](movefolder-operation.md)
  
[CopyFolder-Vorgang](copyfolder-operation.md)
  
[Vorgang abonnieren](subscribe-operation.md)

