---
title: SearchQueries
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 67328dab-321b-45ad-929e-cd83e65ad87e
description: Das SearchQueries-Element enthält eine Liste der Postfächer und zugeordneten Abfragen für Discovery-Suche.
ms.openlocfilehash: 182f1ba63b4226ea4ff6445ae9f039197dec38a5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831316"
---
# <a name="searchqueries"></a>SearchQueries

Das **SearchQueries** -Element enthält eine Liste der Postfächer und zugeordneten Abfragen für Discovery-Suche. 
  
```XML
<SearchQueries>
   <MailboxQuery/>
</SearchQueries>
```

 ****
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[MailboxQuery](mailboxquery.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxes](searchmailboxes.md) | [SearchMailboxesResult](searchmailboxesresult.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

