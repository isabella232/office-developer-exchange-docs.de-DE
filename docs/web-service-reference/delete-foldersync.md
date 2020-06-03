---
title: Delete (FolderSync)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Delete
api_type:
- schema
ms.assetid: c4397d91-43ef-40a9-a80e-d31501a33caa
description: Das delete-Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.
ms.openlocfilehash: 68f8687b8cf0723d7fd63a3d55da8ef7c2f98f8e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44454981"
---
# <a name="delete-foldersync"></a>Delete (FolderSync)

Das **Delete** -Element identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll. 
  
- [SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)  
- [ResponseMessages](responsemessages.md)  
- [SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)  
- [Änderungen (Hierarchie)](changes-hierarchy.md)  
- [Delete (FolderSync)](delete-foldersync.md)
  
```xml
<Delete>
   <FolderId/>
</Delete>
```

**SyncFolderHierarchyDeleteType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderId](folderid.md) <br/> |Enthält den Bezeichner und den Änderungsschlüssel eines Ordners.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Änderungen (Hierarchie)](changes-hierarchy.md) <br/> |Enthält ein sequenziertes Array von Änderungstypen, die die Art der Unterschiede zwischen den Ordnern auf dem Client und den Ordnern auf dem Computer mit Microsoft Exchange Server 2007 darstellen.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Exchange 2007 Computers, auf dem die Client Zugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)
- [EWS-Referenz für Exchange](ews-reference-for-exchange.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

