---
title: BlockExternalImages
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5c754dfc-a9e9-4272-9b5f-5fe3db537e62
description: Das BlockExternalImages-Element gibt an, ob externe Bilder in HTML-Textkörpern blockiert werden.
ms.openlocfilehash: 73342316024ebe476a0e35f14157befc80edcf83
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44527404"
---
# <a name="blockexternalimages"></a>BlockExternalImages

Das **BlockExternalImages** -Element gibt an, ob externe Bilder in HTML-Textkörpern blockiert werden. 
  
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
|[FolderShape](foldershape.md) <br/> |Identifiziert die Ordner Eigenschaften, die in die GetFolder-, FindFolder-oder SyncFolderHierarchy-Antwort eingeschlossen werden sollen.  <br/> |
|[ItemShape](itemshape.md) <br/> |Identifiziert die Elementeigenschaften und Inhalte, die in einer GetItem-, FindItem-oder SyncFolderItems-Antwort enthalten sein sollen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für **BlockExternalImages** -Element gibt an, dass externe Bilder in HTML-Textkörpern blockiert werden. Der Wert **false** gibt an, dass externe Bilder zulässig sind. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

