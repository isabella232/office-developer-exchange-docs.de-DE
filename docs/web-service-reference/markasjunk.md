---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: Das MarkAsJunk-Element gibt die Anforderung zum Verschieben eines Elements in den Junk-e-Mailordner und den Absender zur Liste blockierter Absender hinzufügen.
ms.openlocfilehash: fbb3eee7ce350954888931ca55b27f596656b161
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830350"
---
# <a name="markasjunk"></a>MarkAsJunk

Das **MarkAsJunk** -Element gibt die Anforderung zum Verschieben eines Elements in den Junk-e-Mailordner und den Absender zur Liste blockierter Absender hinzufügen. 
  
```XML
<MarkAsJunk IsJunk="true | false" MoveItem="true | false">
   <ItemIds/>
</MarkAsJunk>
```

 **MarkAsJunkType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|IsJunk  <br/> |Der Textwert **true** für das **IsJunk** -Attribut gibt an, dass der e-Mail-Absender zur Liste blockierter Absender hinzugefügt wird. Der Wert **false** gibt an, dass der e-Mail-Absender aus der Liste blockierter Absender entfernt wird, wenn der e-Mail-Absender bereits in der Liste ist.  <br/> |
|MoveItem  <br/> |Der Textwert **true** für das **MoveItem** -Attribut gibt an, dass das Element in der standardmäßigen Junk-e-Mail-Ordner verschoben wird. Der Wert **false** gibt an, dass das Element nicht in den Junk-e-Mail-Standardordner verschoben wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[Artikelnummern ein.](itemids.md)
  
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
   

