---
title: SyncState
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SyncState
api_type:
- schema
ms.assetid: e5ebaae3-0f07-481d-ac67-d9687a3c7ac3
description: Das SyncState-Element enthält eine base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.
ms.openlocfilehash: 72a0e347b5732cbe397956f8cc50b3266fba9156
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543905"
---
# <a name="syncstate"></a>SyncState

Das **SyncState-Element** enthält eine base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren. 
  
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
|[SyncFolderHierarchy](syncfolderhierarchy.md) <br/> |Definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.  <br/> |
|[SyncFolderHierarchyResponseMessage](syncfolderhierarchyresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderHierarchy-Anforderung.  <br/> |
|[SyncFolderItems](syncfolderitems.md) <br/> |Definiert eine Anforderung zum Synchronisieren von Elementen in einem Exchange Speicherordner.  <br/> |
|[SyncFolderItemsResponseMessage](syncfolderitemsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SyncFolderItems-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderItems-Vorgang](syncfolderitems-operation.md)
  
[SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

