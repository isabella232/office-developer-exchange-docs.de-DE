---
title: FailedMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f34fb6f6-057e-4ae3-8e10-bc92112eafba
description: Das FailedMailboxes-Element gibt ein Array von Postfächern an, bei denen die Suche fehlgeschlagen ist.
ms.openlocfilehash: 10f10d3f2ac4379d7ddcb3a13019d17a17bb676a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461954"
---
# <a name="failedmailboxes"></a>FailedMailboxes

Das **FailedMailboxes** -Element gibt ein Array von Postfächern an, bei denen die Suche fehlgeschlagen ist. 
  
```XML
<FailedMailboxes>
    <FailedMailbox/>
<FailedMailboxes>
```

 **ArrayOfFailedSearchMailboxesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FailedMailbox](failedmailbox.md) <br/> |Gibt die Fehlermeldung für ein Postfach an, bei dem die Suche fehlgeschlagen ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchMailboxesResult](searchmailboxesresult.md) <br/> |Enthält das Ergebnis der **SearchMailboxes** -Anforderung.  <br/> |
   
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

