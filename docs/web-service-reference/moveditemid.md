---
title: MovedItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7d5425ab-1e75-43d1-b801-802ff5139df6
description: Das MovedItemId-Element gibt den Bezeichner des Elements an, das von der MarkAsJunk-Operation verschoben wurde.
ms.openlocfilehash: 5cf8800ec672278691348bbcd8c6c8cc7a12905b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468614"
---
# <a name="moveditemid"></a>MovedItemId

Das **MovedItemId** -Element gibt den Bezeichner des Elements an, das von der **MarkAsJunk** -Operation verschoben wurde. 
  
```XML
<MovedItemId Id="" ChangeKey=""/>
```

 **Itemidtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|Id  <br/> |Der Wert des **ID-** Attributs ist der Elementbezeichner des Elements, das von der **MarkAsJunk** -Operation verschoben wird. Die Element-ID bleibt nach dem Wechsel unverändert.  <br/> |
|ChangeKey  <br/> |Der Wert des **ChangeKey** -Attributs ist der Änderungsschlüssel des verschobenen Elements. Der Änderungsschlüssel ändert sich, nachdem das Element vom **MarkAsJunk** -Vorgang verschoben wurde.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MarkAsJunkResponseMessage](markasjunkresponsemessage.md)
  
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
   

