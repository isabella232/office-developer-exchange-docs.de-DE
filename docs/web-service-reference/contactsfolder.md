---
title: ContactsFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ContactsFolder
api_type:
- schema
ms.assetid: 6c299de8-2087-4aeb-8e66-2bc7586509a6
description: Das ContactsFolder-Element stellt einen Kontakteordner, der in einem Postfach enthalten ist.
ms.openlocfilehash: 01302f00d84cfff9713e3b188b7799c537fc0629
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757623"
---
# <a name="contactsfolder"></a>ContactsFolder

Das **ContactsFolder** -Element stellt einen Kontakteordner, der in einem Postfach enthalten ist. 
  
```xml
<ContactsFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <EffectiveRights/>
   <SharingEffectiveRights/>
   <PermissionSet/>
</ContactsFolder>
```

 **ContactsFolderType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Schlüssel-ID und Ändern eines Ordners Kontakte.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, das den Kontakteordner enthält.  <br/> |
|[FolderClass](folderclass.md) <br/> |Stellt die Ordner-Klasse für einen Kontakteordner dar.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Enthält den Anzeigenamen eines Ordners Kontakte.  <br/> |
|[TotalCount](totalcount.md) <br/> |Stellt die gesamte Anzahl von Elementen in einem Kontakteordner dar.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Stellt die Anzahl der untergeordneten Ordner, die in einem Kontakteordner enthalten sind. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für den Kontakteordner identifiziert.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält.  <br/> |
|[SharingEffectiveRights (PermissionReadAccessType)](sharingeffectiverights-permissionreadaccesstype.md) <br/> |Gibt an, die Berechtigungen, die der Benutzer für die Kontaktdaten aufweist, die gemeinsam genutzt wird.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält die konfigurierten Berechtigungen für einen Ordner.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Erstellen (FolderSync)](create-foldersync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.  <br/> |
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern, die im Ordner Vorgänge verwendet werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

