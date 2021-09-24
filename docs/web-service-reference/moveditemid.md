---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: Das MovedItemId-Element gibt den Bezeichner des Elements an, das vom MarkAsJunk-Vorgang verschoben wurde.
ms.openlocfilehash: 0775aaed119242fc2a2057fb20807d5be30692e5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509595"
---
# <a name="moveditemid"></a>MovedItemId

Das **MovedItemId-Element** gibt den Bezeichner des Elements an, das vom **MarkAsJunk-Vorgang** verschoben wurde. 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 **ItemIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Der Wert des **Id-Attributs** ist der Elementbezeichner des Elements, das durch den **MarkAsJunk-Vorgang** verschoben wird. Der Elementbezeichner bleibt nach der Verschiebung gleich.  <br/> |
|ChangeKey  <br/> |Der Wert des **ChangeKey-Attributs** ist der Änderungsschlüssel des verschobenen Elements. Der Änderungsschlüssel ändert sich, nachdem das Element durch den **MarkAsJunk-Vorgang** verschoben wurde.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
  
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
   

