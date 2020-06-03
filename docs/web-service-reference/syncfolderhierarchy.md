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
description: Das SyncFolderHierarchy-Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client.
ms.openlocfilehash: 68b607dbf603e955f74dfaccadd3ce6c4c9fb6ab
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44466647"
---
# <a name="syncfolderhierarchy"></a>SyncFolderHierarchy

Das **SyncFolderHierarchy** -Element definiert eine Anforderung zum Synchronisieren einer Ordnerhierarchie auf einem Client. 
  
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
|[FolderShape](foldershape.md) <br/> |Gibt die Ordner Eigenschaften an, die in eine [SyncFolderHierarchy](syncfolderhierarchy.md) -Antwort eingeschlossen werden sollen.  <br/> |
|[SyncFolderId](syncfolderid.md) <br/> |Stellt den Ordner dar, der die zu synchronisierenden Elemente enthält. Dieses Element ist optional.  <br/> |
|[Von "SyncState](syncstate-ex15websvcsotherref.md) <br/> |Enthält eine Base64-codierte Form der Synchronisierungsdaten, die nach jeder erfolgreichen Anforderung aktualisiert wird. Dies wird verwendet, um den Synchronisierungsstatus zu identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[SyncFolderHierarchy-Vorgang](syncfolderhierarchy-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

