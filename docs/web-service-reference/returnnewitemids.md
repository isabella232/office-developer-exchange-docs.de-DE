---
title: ReturnNewItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aeef79e4-31e1-4213-b627-9bac676be018
description: Das ReturnNewItemIds-Element gibt an, ob die Element-IDs der neuen Elemente in der Antwort zurückgegeben werden.
ms.openlocfilehash: 6d3bc83c05a82d6e448041167676f41c2620dcd4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831232"
---
# <a name="returnnewitemids"></a>ReturnNewItemIds

Das **ReturnNewItemIds** -Element gibt an, ob die Element-IDs der neuen Elemente in der Antwort zurückgegeben werden. 
  
```XML
<ReturnNewItemIds/>
```

 **xs: Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopyItem](copyitem.md) <br/> |Definiert eine Anforderung an ein Element in einem Postfach im Exchange-Speicher zu kopieren.  <br/> |
|[MoveItem](moveitem.md) <br/> |Definiert eine Anforderung an ein Element im Exchange-Speicher zu verschieben.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **ReturnNewItemIds** -Element gibt an, dass das neue Element-IDs in der Antwort zurückgegeben werden. Der Wert **false** gibt an, dass das neue Element-IDs nicht in der Antwort zurückgegeben werden. 
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

