---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: Das ReadFlag-Element gibt den Lesestatus an, der für Elemente in einem Ordner festgelegt werden soll.
ms.openlocfilehash: ac079f6adbdb2686221dd52d748b05ac4141d6c6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523650"
---
# <a name="readflag"></a>ReadFlag

Das **ReadFlag-Element** gibt den Lesestatus an, der für Elemente in einem Ordner festgelegt werden soll. 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MarkAllItemsAsRead](markallitemsasread.md)
  
## <a name="text-value"></a>Textwert

Der Textwert  true für das **ReadFlag-Element** gibt an, dass die Elemente im Ordner als gelesen markiert werden. Der Wert **"false"** gibt an, dass die Elemente im Ordner als ungelesen markiert werden. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

