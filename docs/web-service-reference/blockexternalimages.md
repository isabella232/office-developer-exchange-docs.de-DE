---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: Das BlockExternalImages-Element gibt an, ob externe Bilder in HTML-Textkörpern blockiert werden.
ms.openlocfilehash: 82ddb7e53f351324783fa39e3b76c9c0534b8193
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543583"
---
# <a name="blockexternalimages"></a>BlockExternalImages

Das **BlockExternalImages-Element** gibt an, ob externe Bilder in HTML-Textkörpern blockiert werden. 
  
```XML
<BlockExternalImages> true | false </BlockExternalImages>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FolderShape](foldershape.md) <br/> |Identifies the folder properties to include in the GetFolder, FindFolder, or SyncFolderHierarchy response.  <br/> |
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und -inhalte, die in eine GetItem-, FindItem- oder SyncFolderItems-Antwort eingeschlossen werden sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **BlockExternalImages-Element** gibt an, dass externe Bilder in HTML-Textkörpern blockiert werden. Der Wert **"false"** gibt an, dass externe Bilder zulässig sind. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

