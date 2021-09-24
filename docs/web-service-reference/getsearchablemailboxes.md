---
title: GetSearchableMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 949871f7-0d10-498e-84aa-f0652f1193be
description: Das GetSearchableMailboxes-Element enthält eine Anforderung zum Abrufen einer Liste von Postfächern, für die der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt.
ms.openlocfilehash: 7c5902af3e0aa88c77a8e13d7c4ec521aa444d6b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515845"
---
# <a name="getsearchablemailboxes"></a>GetSearchableMailboxes

Das **GetSearchableMailboxes-Element** enthält eine Anforderung zum Abrufen einer Liste von Postfächern, für die der Client über die Berechtigung zum Ausführen einer eDiscovery-Suche verfügt. 
  
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

[SearchFilter](searchfilter.md)  |  [ExpandGroupMembership](expandgroupmembership.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

