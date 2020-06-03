---
title: ErrorCode (Int)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 65537d96-edf9-41ee-9ad5-91ffe37e2269
description: Das ErrorCode-Element gibt den Fehlercode einer fehlgeschlagenen Suche an, die für ein Postfach ausgeführt wird.
ms.openlocfilehash: 24170a56e5fa23c3811fcbd27f0240e6ba3c87b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460666"
---
# <a name="errorcode-int"></a>ErrorCode (Int)

Das **errorCode** -Element gibt den Fehlercode einer fehlgeschlagenen Suche an, die für ein Postfach ausgeführt wird. 
  
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
|[FailedMailbox](failedmailbox.md) <br/> |Gibt den Aufbewahrungs Status des Postfachs an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **errorCode** -Elements ist der Fehlercode, der für eine fehlerhafte Suche zurückgegeben wurde, die für ein Postfach ausgeführt wurde. 
  
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

