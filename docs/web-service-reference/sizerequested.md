---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: Das SizeRequested-Element enthält die Größe des angeforderten Fotos für einen Vorgang GetUserPhoto.
ms.openlocfilehash: 43e422512b1e8f06e410e533e9ae1dc49283d5f6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831504"
---
# <a name="sizerequested"></a>SizeRequested

Das **SizeRequested** -Element enthält die Größe des angeforderten Fotos für einen Vorgang **GetUserPhoto** . 
  
```XML
<SizeRequested>HR48x48 | HR64x64 | HR96X96 | HR120X120 | HR240X240 | HR360X360 | HR432X432 | HR504X504 | HR648X648</SizeRequested>
```

 **UserPhotoSizeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetUserPhoto](getuserphoto.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **SizeRequested** -Elements ist die Größe des angeforderten Fotos eines digitalen Bilds vom Server zurückgegeben. Die folgende Tabelle zeigt die Textwerte für das **SizeRequested** -Element. 
  
|**Wert**|**Bedeutung**|
|:-----|:-----|
|HR48x48  <br/> |Das Bild ist 48 Pixel hoch und 48 Pixel breit.  <br/> |
|HR64x64  <br/> |Das Bild ist 64 Pixel hoch und 64 Pixel breit.  <br/> |
|HR96x96  <br/> |Das Bild ist 96 Pixel hoch und 96 Pixel breit.  <br/> |
|HR120x120  <br/> |Das Bild ist 120 Pixel hoch und 120 Pixel breit.  <br/> |
|HR240x240  <br/> |Das Bild ist 240 Pixel hoch und 240 Pixel breit.  <br/> |
|HR360x360  <br/> |Das Bild ist 360 Pixel hoch und 360 Pixel breit.  <br/> |
|HR432x432  <br/> |Das Bild ist 432 Pixel hoch und 432 Pixel breit.  <br/> |
|HR504x504  <br/> |Das Bild ist 504 Pixel hoch und 504 Pixel breit.  <br/> |
|HR648x648  <br/> |Das Bild ist 648 Pixel hoch und 648 Pixel breit.  <br/> |
   
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
   

