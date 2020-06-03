---
title: ManagedFolderInformation
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ManagedFolderInformation
api_type:
- schema
ms.assetid: dea980eb-8303-47fe-a380-20a8efc9ead6
description: Das ManagedFolderInformation-Element enthält Informationen zu einem verwalteten benutzerdefinierten Ordner.
ms.openlocfilehash: ce15dcb15cccdce253494beefd2f4a2a7a0c0ad8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44450949"
---
# <a name="managedfolderinformation"></a>ManagedFolderInformation

Das **ManagedFolderInformation** -Element enthält Informationen zu einem verwalteten benutzerdefinierten Ordner. 
  
```xml
<ManagedFolderInformation>
   <CanDelete/>
   <CanRenameOrMove/>
   <MustDisplayComment/>
   <HasQuota/>
   <IsManagedFoldersRoot/>
   <ManagedFolderId/>
   <Comment/>
   <StorageQuota/>
   <FolderSize/>
   <HomePage/>
</ManagedFolderInformation>
```

 **ManagedFolderInformationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CanDelete](candelete.md) <br/> |Gibt an, ob ein verwalteter Ordner von einem Kunden gelöscht werden kann.  <br/> |
|[CanRenameOrMove](canrenameormove.md) <br/> |Gibt an, ob ein bestimmter verwalteter Ordner vom Kunden umbenannt oder verschoben werden kann.  <br/> |
|[MustDisplayComment](mustdisplaycomment.md) <br/> |Gibt an, ob der Kommentar des verwalteten Ordners angezeigt werden muss.  <br/> |
|[HasQuota](hasquota.md) <br/> |Gibt an, ob der verwaltete Ordner ein Kontingent aufweist.  <br/> |
|[IsManagedFoldersRoot](ismanagedfoldersroot.md) <br/> |Gibt an, ob der verwaltete Ordner der Stamm für alle verwalteten Ordner ist.  <br/> |
|[ManagedFolderId](managedfolderid.md) <br/> |Enthält die Ordner-ID des verwalteten Ordners.  <br/> |
|[Kommentar](comment.md) <br/> |Enthält den Kommentar, der einem verwalteten Ordner zugeordnet ist.  <br/> |
|[StorageQuota](storagequota.md) <br/> |Beschreibt das Speicherkontingent für den verwalteten Ordner.  <br/> |
|[FolderSize](foldersize.md) <br/> |Beschreibt die Gesamtgröße aller Inhalte eines verwalteten Ordners.  <br/> |
|[HomePage](homepage.md) <br/> |Gibt die URL an, die als Standardstartseite für den verwalteten Ordner verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Stellt einen Ordner im Exchange-Informationsspeicher dar. Verwaltete benutzerdefinierte Ordner können nur Unterordner des Ordners mit dem Namen " **verwaltete Ordner**" sein.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Nicht zutreffend.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Nicht zutreffend.  <br/> |
|[SearchFolder](searchfolder.md) <br/> |Nicht zutreffend.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Nicht zutreffend  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[CreateManagedFolder-Vorgang](createmanagedfolder-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Hinzufügen von verwalteten Ordnern](https://msdn.microsoft.com/library/846658c6-7043-40fb-8439-19f97c2a967f%28Office.15%29.aspx)

