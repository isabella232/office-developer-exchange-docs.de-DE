---
title: Synchronisierungsstatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: Das Synchronisierungsstatus-Element enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.
ms.openlocfilehash: 3c600dde09fd813dcfb1f6e74671ebe9004701a1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839155"
---
# <a name="syncstate"></a>Synchronisierungsstatus

Das **Synchronisierungsstatus** -Element enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren. 
  
```xml
<SyncState/>
```

 **String**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung SyncFolderHierarchy.  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Definiert eine Anforderung zum Synchronisieren von Elementen in einem Ordner von Exchange-Speicher.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Anforderung SyncFolderItems.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)
  
[SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

