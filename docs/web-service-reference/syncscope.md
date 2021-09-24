---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: Das SyncScope-Element gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden.
ms.openlocfilehash: 5e5d19809cea1f8f244444c09615ee888fea05be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538898"
---
# <a name="syncscope"></a>SyncScope

Das **SyncScope-Element** gibt an, ob nur Elemente oder Elemente und Ordner zugeordnete Informationen in einer Synchronisierungsantwort zurückgegeben werden. 
  
```xml
<SyncScope>NormalItems or NormalAndAssociatedItems</SyncScope>
```

 **SyncFolderItemsScopeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SyncFolderItems](syncfolderitems.md) <br/> |Das Element, das eine Anforderung zum Synchronisieren von Elementen in einem Exchange Speicherordner definiert.  <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet:   <br/> /SyncFolderItems  <br/> |
   
## <a name="text-value"></a>Textwert

In der folgenden Tabelle sind die möglichen Werte für das **SyncScope-Element** aufgeführt. 
  
**SyncScope-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NormalItems  <br/> |Gibt an, dass nur Elemente im Ordner in einer Synchronisierungsantwort zurückgegeben werden.  <br/> |
|NormalAndAssociatedItems  <br/> |Gibt an, dass sowohl Elemente im Ordner als auch die mit dem Ordner verknüpften Informationen in einer Synchronisierungsantwort zurückgegeben werden.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

