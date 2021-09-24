---
title: RelativeFolderPath
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 54e3ba52-08a6-4d48-8a44-6fd5fdbffb25
description: Das RelativeFolderPath-Element enthält ein Array von Ordnern, die den relativen Ordnerpfad des zu erstellenden Ordnerpfads angeben.
ms.openlocfilehash: f9a1f193678e9dbd7686376c630ab2fbd0eaf1bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513458"
---
# <a name="relativefolderpath"></a>RelativeFolderPath

Das **RelativeFolderPath-Element** enthält ein Array von Ordnern, die den relativen Ordnerpfad des zu erstellenden Ordnerpfads angeben. 
  
```XML
<RelativeFolderPath>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</RelativeFolderPath>
```

 **NonEmptyArrayOfFoldersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Ordner](folder.md)  |  [CalendarFolder](calendarfolder.md)  |  [ContactsFolder](contactsfolder.md)  |  [SearchFolder](searchfolder.md)  |  [TasksFolder](tasksfolder.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[CreateFolderPath](createfolderpath.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

