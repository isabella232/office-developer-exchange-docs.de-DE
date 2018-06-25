---
title: SyncFolderItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderItems
api_type:
- schema
ms.assetid: 463ed78c-bf82-4cd8-971a-d18425e9e7be
description: Das SyncFolderItems-Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.
ms.openlocfilehash: 368e19babfccaeab40380103495c63d30647905c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839150"
---
# <a name="syncfolderitems"></a>SyncFolderItems

Das **SyncFolderItems** -Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher. 
  
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
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und den Inhalt in einer Antwort SyncFolderItems aufzunehmen. Dieses Element ist erforderlich.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner, der zu synchronisierenden Elemente enthält. Dieses Element ist erforderlich.  <br/> |
|[Synchronisierungsstatus](syncstate-ex15websvcsotherref.md) <br/> |Enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren. Dieses Element ist optional.  <br/> |
|[Ignorieren](ignore.md) <br/> |Identifiziert Elemente, während der Synchronisierung zu überspringen. Dieses Element ist optional.  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |Beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierung Antwort zurückgegeben werden kann. Dieses Element ist erforderlich.  <br/> |
|[SyncScope](syncscope.md) <br/> |Gibt an, ob nur Elemente oder Elemente und verknüpften Ordnerinformationen in eine Synchronisierung Antwort zurückgegeben werden. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

