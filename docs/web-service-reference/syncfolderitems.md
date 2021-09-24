---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: Das SyncFolderItems-Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange Speicherordner.
ms.openlocfilehash: a3e5aa83335a6bc29b832021e227e6adad4092bf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513283"
---
# <a name="syncfolderitems"></a>SyncFolderItems

Das **SyncFolderItems-Element** definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange Speicherordner. 
  
```xml
<SyncFolderItems>
   <ItemShape/>
   <SyncFolderId/>
   <SyncState/>
   <Ignore/>
   <MaxChangesReturned/>   <SyncScope/>
</SyncFolderItems>
```

 **SyncFolderItemsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und -inhalte, die in eine SyncFolderItems-Antwort eingeschlossen werden sollen. Dieses Element ist erforderlich.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält. Dieses Element ist erforderlich.  <br/> |
|[SyncState](syncstate-ex15websvcsotherref.md) <br/> |Enthält eine base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren. Dieses Element ist optional.  <br/> |
|[Ignore](ignore.md) <br/> |Identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen. Dieses Element ist optional.  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |Beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierungsantwort zurückgegeben werden können. Dieses Element ist erforderlich.  <br/> |
|[SyncScope](syncscope.md) <br/> |Gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

