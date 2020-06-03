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
description: Das SyncFolderItems-Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner.
ms.openlocfilehash: 0fa5b1544d5627d1423287369e72f97662c28d12
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465149"
---
# <a name="syncfolderitems"></a>SyncFolderItems

Das **SyncFolderItems** -Element definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange-Informationsspeicher Ordner. 
  
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
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und Inhalte, die in einer SyncFolderItems-Antwort enthalten sein sollen. Dieses Element ist erforderlich.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält. Dieses Element ist erforderlich.  <br/> |
|[Von "SyncState](syncstate-ex15websvcsotherref.md) <br/> |Enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren. Dieses Element ist optional.  <br/> |
|[Ignore](ignore.md) <br/> |Identifiziert Elemente, die während der Synchronisierung übersprungen werden sollen. Dieses Element ist optional.  <br/> |
|[MaxChangesReturned](maxchangesreturned.md) <br/> |Beschreibt die maximale Anzahl von Änderungen, die in einer Synchronisierungsantwort zurückgegeben werden können. Dieses Element ist erforderlich.  <br/> |
|[SyncScope](syncscope.md) <br/> |Gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

