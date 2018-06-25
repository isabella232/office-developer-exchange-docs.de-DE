---
title: TasksFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TasksFolder
api_type:
- schema
ms.assetid: 5a9a4612-8064-4986-b467-c44f268c64df
description: Das TasksFolder-Element darstellt, einen Aufgabenordner, der in einem Postfach enthalten ist.
ms.openlocfilehash: b2151c68519a6ff15fbc74b48fc93a7e06af9e76
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839162"
---
# <a name="tasksfolder"></a>TasksFolder

Das **TasksFolder** -Element darstellt, einen Aufgabenordner, der in einem Postfach enthalten ist. 
  
```xml
<TasksFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <PermissionSet/>
      <EffectiveRights/>
</TasksFolder>
```

**TasksFolderType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Den Schlüssel-ID und Ändern des einem Aufgabenordner enthält.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, der den Ordner Aufgaben enthält.  <br/> |
|[FolderClass](folderclass.md) <br/> |Stellt die Ordner-Klasse für einen Aufgabenordner dar.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Enthält den Anzeigenamen der Aufgabenordner.  <br/> |
|[TotalCount](totalcount.md) <br/> |Stellt die gesamte Anzahl von Elementen in einem Aufgabenordner dar.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Stellt die Anzahl der untergeordneten Ordner, die in einem Aufgabenordner enthalten sind. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften auf einem Aufgabenordner identifiziert.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Stellt die Anzahl der ungelesenen Elemente in einem Aufgabenordner dar.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält die konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt. Dieses Element wurde in Microsoft Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Erstellen (FolderSync)](create-foldersync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.  <br/> |
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

