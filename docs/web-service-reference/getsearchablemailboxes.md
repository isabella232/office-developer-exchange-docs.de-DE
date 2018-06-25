---
title: GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 949871f7-0d10-498e-84aa-f0652f1193be
description: Das GetSearchableMailboxes-Element enthält eine Anforderung an einer Liste der Postfächer erhalten möchten, dass der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt.
ms.openlocfilehash: 8cce18bb62d3840cb9883d20a380cc4f2193303e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758790"
---
# <a name="getsearchablemailboxes"></a>GetSearchableMailboxes

Das **GetSearchableMailboxes** -Element enthält eine Anforderung an einer Liste der Postfächer erhalten möchten, dass der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt. 
  
```XML
<GetSearchableMailboxes>
   <SearchFilter/>
   <ExpandGroupMembership/>
</GetSearchableMailboxes>
```

 **GetSearchableMailboxesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[SearchFilter](searchfilter.md) | [ExpandGroupMembership](expandgroupmembership.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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
   

