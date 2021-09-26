---
title: SizeRequested
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e86f98b6-83b5-4530-80eb-dc5df42e2c62
description: Das SizeRequested-Element enthält die angeforderte Fotogröße für einen GetUserPhoto-Vorgang.
ms.openlocfilehash: 799869a85d7f72e79753a73f9c259388a2702bf5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545916"
---
# <a name="sizerequested"></a>SizeRequested

Das **SizeRequested-Element** enthält die angeforderte Fotogröße für einen **GetUserPhoto-Vorgang.** 
  
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

Der Textwert des **SizeRequested-Elements** ist die angeforderte Fotogröße eines vom Server zurückgegebenen digitalen Bilds. In der folgenden Tabelle sind die Textwerte für das **SizeRequested-Element aufgeführt.** 
  
|**Value**|**Bedeutung**|
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
   

