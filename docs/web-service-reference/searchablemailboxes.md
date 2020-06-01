---
title: SearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: eb0a7897-c642-4c93-a238-be03128af54e
description: Das SearchableMailboxes-Element enthält ein Array der Postfächer, die von einer GetSearchableMailboxes-Anforderung zurückgegeben werden.
ms.openlocfilehash: 5de15e1c2ae4a587052f836b189651450a1e7482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467445"
---
# <a name="searchablemailboxes"></a>SearchableMailboxes

Das **SearchableMailboxes** -Element enthält ein Array der Postfächer, die von einer **GetSearchableMailboxes** -Anforderung zurückgegeben werden. 
  
```XML
<SearchableMailboxes>
   <SearchableMailbox/>
</SearchableMailboxes>
```

 **ArrayOfSearchableMailboxesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[SearchableMailbox](searchablemailbox.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetSearchableMailboxesResponse](getsearchablemailboxesresponse.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> ||
   

