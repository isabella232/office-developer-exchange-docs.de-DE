---
title: Erstellen (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Create
api_type:
- schema
ms.assetid: 6b463d0a-70e9-40c5-ade4-c7d9a5f36bc1
description: Das Create-Element identifiziert einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.
ms.openlocfilehash: 867eecb89c115b008d4828e162b21d078eba695c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757734"
---
# <a name="create-foldersync"></a>Erstellen (FolderSync)

Das **Create** -Element identifiziert einen einzelnen Ordner im lokalen Client-Speicher zu erstellen. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Änderungen (Hierarchie)](changes-hierarchy.md)
  
[Erstellen (FolderSync)](create-foldersync.md)
  
```xml
<Create>
   <Folder/>
   <CalendarFolder/>
   <ContactsFolder/>
   <SearchFolder/>
   <TasksFolder/>
</Create>
```

 **SyncFolderHierarchyCreateOrUpdateType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Folder](folder.md) <br/> |Definiert den Ordner, um das Erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.  <br/> |
|[CalendarFolder](calendarfolder.md) <br/> |Stellt einen Ordner, der in erster Linie Kalenderelemente enthält.  <br/> |
|[ContactsFolder](contactsfolder.md) <br/> |Stellt einem Kontaktordner in einem Postfach an.  <br/> |
|["SearchFolder"](searchfolder.md) <br/> |Stellt einen Suchordner in einem Postfach enthalten.  <br/> |
|[TasksFolder](tasksfolder.md) <br/> |Stellt einen Aufgabenordner, die in einem Postfach enthalten sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Änderungen (Hierarchie)](changes-hierarchy.md) <br/> |Enthält ein Array Sequenz von Dateitypen ändern, die den Typ der Unterschiede zwischen den Elementen auf dem Client und der Elemente auf dem Exchange-Server darstellen.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

