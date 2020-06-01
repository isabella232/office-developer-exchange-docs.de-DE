---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: Das MarkAsJunk-Element gibt die Anforderung an, ein Element in den Ordner Junk-e-Mail zu migrieren und den Absender der Liste blockierter Absender hinzuzufügen.
ms.openlocfilehash: 99adc423864f3096772394ef290df20e158e457d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467081"
---
# <a name="markasjunk"></a>MarkAsJunk

Das **MarkAsJunk** -Element gibt die Anforderung an, ein Element in den Ordner Junk-e-Mail zu migrieren und den Absender der Liste blockierter Absender hinzuzufügen. 
  
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
|Isjunk  <br/> |Der Textwert **true** für das **isjunk** -Attribut gibt an, dass der e-Mail-Absender der Liste blockierter Absender hinzugefügt wird. Der Wert **false** gibt an, dass der e-Mail-Absender aus der Liste blockierter Absender entfernt wird, wenn sich der e-Mail-Absender bereits in der Liste befindet.  <br/> |
|MoveItem  <br/> |Der Textwert **true** für das **MoveItem** -Attribut gibt an, dass das Element in den standardmäßigen Junk-e-Mail-Ordner verschoben wird. Der Wert **false** gibt an, dass das Element nicht in den standardmäßigen Junk-e-Mail-Ordner verschoben wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[ItemIds](itemids.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
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
   

