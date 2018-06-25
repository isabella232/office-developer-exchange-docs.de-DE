---
title: Ordner
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Folder
api_type:
- schema
ms.assetid: 812948d8-c7db-45ce-bb3a-77233a53a974
description: Das Folder-Element definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren.
ms.openlocfilehash: ecfea52d2105599372a22b78778ac0d0d066bc60
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758506"
---
# <a name="folder"></a>Ordner

Das **Folder** -Element definiert einen Ordner erstellen, abrufen, suchen, synchronisieren oder zu aktualisieren. 
  
```xml
<Folder>
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
</Folder>
```

 **FolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, der den Ordner enthält.  <br/> |
|[FolderClass](folderclass.md) <br/> |Stellt die Ordner-Klasse für einen bestimmten Ordner.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Enthält den Anzeigenamen eines Ordners.  <br/> |
|[TotalCount](totalcount.md) <br/> |Stellt die gesamte Anzahl von Elementen in einem bestimmten Ordner an.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Stellt die Anzahl der untergeordneten Ordner, die in einem Ordner enthalten sind. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner identifiziert.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält die konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Erstellen (FolderSync)](create-foldersync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.  <br/> |
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

