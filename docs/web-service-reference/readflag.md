---
title: ReadFlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 9d91aa89-9f9f-4877-846d-aaf48bbeec7c
description: Das ReadFlag-Element gibt den Zustand "gelesen", um für Elemente in einem Ordner festzulegen.
ms.openlocfilehash: f3156a51fbdd3372dd28f2065499d26a50b3d497
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830954"
---
# <a name="readflag"></a>ReadFlag

Das **ReadFlag** -Element gibt den Zustand "gelesen", um für Elemente in einem Ordner festzulegen. 
  
```XML
<ReadFlag>true | false</ReadFlag>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MarkAllItemsAsRead](markallitemsasread.md)
  
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **ReadFlag** -Element gibt an, dass die Elemente im Ordner als gelesen markiert werden. Der Wert **"false"** gibt an, dass die Elemente im Ordner markiert werden als ungelesen. 
  
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
   

