---
title: SearchFolder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SearchFolder
api_type:
- schema
ms.assetid: 1a7d408b-2e98-4391-8834-085ed6d5757c
description: Das SearchFolder-Element stellt einen Suchordner dar, der in einem Postfach enthalten ist.
ms.openlocfilehash: 44f19dad83e8cd18045901bc7e3e48e31508b3db
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544003"
---
# <a name="searchfolder"></a>SearchFolder

Das **SearchFolder-Element** stellt einen Suchordner dar, der in einem Postfach enthalten ist. 
  
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
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, der den Ordner enthält.  <br/> |
|[FolderClass](folderclass.md) <br/> |Stellt die Ordnerklasse für einen bestimmten Ordner dar.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Enthält den Anzeigenamen eines Ordners.  <br/> |
|[TotalCount](totalcount.md) <br/> |Stellt die Gesamtanzahl der Elemente in einem bestimmten Ordner dar.  <br/> |
|[ChildFolderCount](childfoldercount.md) <br/> |Stellt die Anzahl der untergeordneten Ordner dar, die in einem Ordner enthalten sind. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Identifiziert erweiterte Eigenschaften für Ordner.  <br/> |
|[ManagedFolderInformation](managedfolderinformation.md) <br/> |Enthält Informationen zu einem verwalteten Ordner.  <br/> |
|[UnreadCount](unreadcount.md) <br/> |Stellt die Anzahl der ungelesenen Elemente in einem bestimmten Ordner dar.  <br/> |
|[SearchParameters](searchparameters.md) <br/> |Enthält die Parameter, die einen Suchordner definieren.  <br/> |
|[PermissionSet (PermissionSetType)](permissionset-permissionsettype.md) <br/> |Enthält alle konfigurierten Berechtigungen für einen Ordner. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AppendToFolderField](appendtofolderfield.md) <br/> |Gibt Daten an, die während einer [UpdateFolder-Vorgang](updatefolder-operation.md) an eine Ordnereigenschaft angefügt werden sollen.  <br/> |
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[SetFolderField](setfolderfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft in einem Ordner in einer [UpdateFolder-Vorgang](updatefolder-operation.md)dar.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
|[Ordner](folders-ex15websvcsotherref.md) <br/> |Enthält ein Array von Ordnern, die in Ordnervorgängen verwendet werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

 **SearchFolder** wird sowohl für reguläre Suchordner als auch für MicrosoftOfficeOutlook und Outlook sichtbaren Web Access-Suchordner verwendet. Damit ein Suchordner für Outlook und Outlook Web Access sichtbar ist, muss der Ordner unter dem definierten Ordner "SearchFolders" erstellt werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

