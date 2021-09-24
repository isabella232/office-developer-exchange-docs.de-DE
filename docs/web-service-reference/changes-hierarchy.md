---
title: Änderungen (Hierarchie)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Changes
api_type:
- schema
ms.assetid: 918a0d1f-90a5-4eef-9592-07e15bef94e6
description: The Changes element contains a sequenced array of change types that represent the type of differences between the folders on the client and the folders on the computer that is running Microsoft Exchange Server 2007.
ms.openlocfilehash: 1ecb43e37258ad5d8e12619436f14992cc2f788b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512121"
---
# <a name="changes-hierarchy"></a>Änderungen (Hierarchie)

Das **Changes-Element** enthält ein sequenziertes Array von Änderungstypen, die die Art der Unterschiede zwischen den Ordnern auf dem Client und den Ordnern auf dem Computer darstellen, auf dem Microsoft Exchange Server 2007 ausgeführt wird. 
  
[SyncFolderHierarchyResponse](syncfolderhierarchyresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md)
  
[Änderungen (Hierarchie)](changes-hierarchy.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
</Changes>
```

 **SyncFolderHierarchyChangesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Create (FolderSync)](create-foldersync.md) <br/> |Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[Update (FolderSync)](update-foldersync.md) <br/> |Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
|[Delete (FolderSync)](delete-foldersync.md) <br/> |Identifiziert einen einzelnen Ordner, der im lokalen Clientspeicher gelöscht werden soll.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderHierarchy-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des computers Exchange 2007, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)


[EWS-Referenz für Exchange](ews-reference-for-exchange.md)
  
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

