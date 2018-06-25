---
title: "\"SearchFolder\""
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: Das Element "SearchFolder" stellt einen Suchordner, der in einem Postfach enthalten ist.
ms.openlocfilehash: d842c54dab7950c68e26804b676834c2d95debad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831302"
---
# <a name="searchfolder"></a>"SearchFolder"

Das Element **"SearchFolder"** stellt einen Suchordner, der in einem Postfach enthalten ist. 
  
```xml
<SearchFolder>
   <FolderId/>
   <ParentFolderId/>
   <FolderClass/>
   <DisplayName/>
   <TotalCount/>
   <ChildFolderCount/>
   <ExtendedProperty/>
   <ManagedFolderInformation/>
   <UnreadCount/>
   <SearchParameters/>
   <PermissionSet/>
      <EffectiveRights/>
</SearchFolder>
```

 **SearchFolderType**
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
|[ChildFolderCount](childfoldercount.md) <br/> |Die Anzahl der in einem Ordner enthaltenen untergeordneten Ordner darstellt. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner identifiziert.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Die Anzahl der ungelesenen Elemente innerhalb eines bestimmten Ordners darstellt.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Enthält die Parameter, die einen Suchordner definieren.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält die konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Erstellen (FolderSync)](create-foldersync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Gibt einen einzelnen Ordner, in den lokalen Client-Speicher zu aktualisieren.  <br/> |
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern im Ordner Vorgänge verwendet.  <br/> |
   
## <a name="remarks"></a>Hinweise

 **"SearchFolder"** wird für die regulären Suchordner und MicrosoftOfficeOutlook und Outlook Web Access sichtbar Suchordner. Für ein Suchordner für Outlook und Outlook Web Access sichtbar sein soll muss der Ordner unter dem definierten SearchFolders-Ordner erstellt werden. 
  
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

