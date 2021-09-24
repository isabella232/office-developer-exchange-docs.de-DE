---
title: IsArchive
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: b89d8a78-5c18-4547-aaf4-4b16a93190a7
description: Das IsArchive-Element gibt einen booleschen Wert an, der angibt, ob das Postfach ein Archivpostfach ist.
ms.openlocfilehash: 269cb614ad9402a266b2ed521c4f485b3f43b1fb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514564"
---
# <a name="isarchive"></a>IsArchive

Das **IsArchive-Element** gibt einen booleschen Wert an, der angibt, ob das Postfach ein Archivpostfach ist. 
  
```XML
<IsArchive>true | false</IsArchive>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FailedMailbox](failedmailbox.md)  |  [RetentionPolicyTag](retentionpolicytag.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IsArchive-Element** gibt an, dass das Zielpostfach ein Archivpostfach ist. Der Wert **"false"** gibt an, dass das Zielpostfach kein Archivpostfach ist. 
  
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

