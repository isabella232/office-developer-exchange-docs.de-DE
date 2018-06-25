---
title: SyncScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncScope
api_type:
- schema
ms.assetid: e0ca231f-0374-4844-8d4c-ada8da167920
description: Das SyncScope-Element gibt an, ob nur Elemente oder Elemente und verknüpften Ordnerinformationen in eine Synchronisierung Antwort zurückgegeben werden.
ms.openlocfilehash: 847c0244a8847364e29ea584b0c0b721f00d3064
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839154"
---
# <a name="syncscope"></a>SyncScope

Das **SyncScope** -Element gibt an, ob nur Elemente oder Elemente und verknüpften Ordnerinformationen in eine Synchronisierung Antwort zurückgegeben werden. 
  
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
|[SyncFolderItems](syncfolderitems.md) <br/> |Das Element, das eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher definiert.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:  <br/> / SyncFolderItems  <br/> |
   
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Werte für das **SyncScope** -Element. 
  
**SyncScope-Elementwerte**

|**Wert**|**Beschreibung**|
|:-----|:-----|
|NormalItems  <br/> |Gibt an, dass nur die Elemente im Ordner in einer Synchronisierung Antwort zurückgegeben werden.  <br/> |
|NormalAndAssociatedItems  <br/> |Gibt an, dass beide Elemente in den Ordner und die Informationen des Ordners, in eine Synchronisierung Antwort zurückgegeben werden.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

