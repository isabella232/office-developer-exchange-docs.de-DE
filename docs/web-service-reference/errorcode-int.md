---
title: ErrorCode (int)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: Das ErrorCode-Element gibt den Fehlercode einer fehlgeschlagenen Suche an, die für ein Postfach ausgeführt wurde.
ms.openlocfilehash: 25a0b14ecefce76707a8dfa73f99d8b93b445af7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59530837"
---
# <a name="errorcode-int"></a>ErrorCode (int)

Das **ErrorCode-Element** gibt den Fehlercode einer fehlgeschlagenen Suche an, die für ein Postfach ausgeführt wurde. 
  
```XML
<ErrorCode></ErrorCode>
```

 **int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FailedMailbox](failedmailbox.md) <br/> |Gibt den Aufbewahrungsstatus des Postfachs an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **ErrorCode-Elements** ist der Fehlercode, der für eine fehlgeschlagene Suche in einem Postfach zurückgegeben wird. 
  
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

