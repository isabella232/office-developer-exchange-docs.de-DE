---
title: MarkAsJunk
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f06bafc6-7ee3-4b2b-9fd1-7c51328f4729
description: Das MarkAsJunk-Element gibt die Anforderung an, ein Element in den Junk-E-Mail-Ordner zu verschieben und den Absender zur Liste der blockierten Absender hinzuzufügen.
ms.openlocfilehash: 252c36b8bb3662ffd6c0fe470a81b6f0b55acb69
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544087"
---
# <a name="markasjunk"></a>MarkAsJunk

Das **MarkAsJunk-Element** gibt die Anforderung an, ein Element in den Junk-E-Mail-Ordner zu verschieben und den Absender zur Liste der blockierten Absender hinzuzufügen. 
  
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
|IsJunk  <br/> |Der Textwert **"true"** für das **IsJunk-Attribut** gibt an, dass der E-Mail-Absender der Liste der blockierten Absender hinzugefügt wird. Der Wert **"false"** gibt an, dass der E-Mail-Absender aus der Liste der blockierten Absender entfernt wird, wenn sich der E-Mail-Absender bereits in der Liste befindet.  <br/> |
|MoveItem  <br/> |Der Textwert  true für das **MoveItem-Attribut** gibt an, dass das Element in den Standardmäßigen Junk-E-Mail-Ordner verschoben wird. Der Wert **"false"** gibt an, dass das Element nicht in den Standardmäßigen Junk-E-Mail-Ordner verschoben wird.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

[ItemIds](itemids.md)
  
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
   

