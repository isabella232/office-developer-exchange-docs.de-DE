---
title: Änderungen (Elemente)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Changes
api_type:
- schema
ms.assetid: d3139fef-0455-4b89-babd-5d6783b50a58
description: Das Changes-Element enthält ein Sequenzarray von Änderungstypen, die die Arten von Unterschieden zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen.
ms.openlocfilehash: ede81d8ecae9751c477ae05cbd13f914fedf8e0f
ms.sourcegitcommit: 357b882a02e37b380a23b8a45b15f9c006a40b02
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 08/31/2021
ms.locfileid: "58764630"
---
# <a name="changes-items"></a>Änderungen (Elemente)

Das **Changes-Element** enthält ein Sequenzarray von Änderungstypen, die die Typen der Unterschiede zwischen den Elementen auf dem Client und den Elementen auf dem Exchange-Server darstellen. 
  
[SyncFolderItemsResponse](syncfolderitemsresponse.md)
  
[ResponseMessages](responsemessages.md)
  
[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md)
  
[Änderungen (Elemente)](changes-items.md)
  
```xml
<Changes>
   <Create/>
   <Update/>
   <Delete/>
   <ReadFlagChange/>
</Changes>
```

 **SyncFolderItemsChangesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
|[Delete (ItemSync)](delete-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher gelöscht werden soll.  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |Wird in [SyncFolderItems-Vorgangsantworten](syncfolderitems-operation.md) zurückgegeben, wenn ein Element gelesen wurde. Diese Eigenschaft ist schreibgeschützt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer [SyncFolderItems-Vorgangsanforderung.](syncfolderitems-operation.md)  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

