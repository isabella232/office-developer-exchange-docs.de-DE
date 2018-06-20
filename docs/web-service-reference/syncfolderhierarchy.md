---
title: SyncFolderHierarchy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SyncFolderHierarchy
api_type:
- schema
ms.assetid: 55df4d01-e48e-4263-a851-78a66ad1093a
description: Das SyncFolderHierarchy-Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an.
ms.openlocfilehash: f72640e5605dd83e92cd323cb00e4d2f64406245
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839146"
---
# <a name="syncfolderhierarchy"></a>SyncFolderHierarchy

Das **SyncFolderHierarchy** -Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client an. 
  
```xml
<SyncFolderHierarchy>
   <FolderShape/>   <SyncFolderId/>
   <SyncState/>
</SyncFolderHierarchy>
```

 **SyncFolderHierarchyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Gibt die Eigenschaften des Ordners in einer Antwort [SyncFolderHierarchy](syncfolderhierarchy.md) aufzunehmen.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner, der zu synchronisierenden Elemente enthält. Dieses Element ist optional.  <br/> |
|[Synchronisierungsstatus](syncstate-ex15websvcsotherref.md) <br/> |Enthält eine base64-codierten Format von der Synchronisierung von Daten, die nach jeder Anforderung erfolgreich aktualisiert werden. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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



[SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

