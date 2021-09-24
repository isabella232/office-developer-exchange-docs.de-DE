---
title: MoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: Das MoveItem-Element definiert eine Anforderung zum Verschieben eines Elements im Exchange Speicher.
ms.openlocfilehash: 5df569722534b8a248da64b71f21219866173aab
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509602"
---
# <a name="moveitem"></a>MoveItem

Das **MoveItem-Element** definiert eine Anforderung zum Verschieben eines Elements im Exchange Speicher. 
  
```XML
<MoveItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</MoveItem>
```

 **MoveItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |Stellt den Zielordner für ein verschobenes Element dar.  <br/> |
|[ItemIds](itemids.md) <br/> |Enthält ein Array identifizierter Elemente, die in den ordner verschoben werden sollen, der durch das [ToFolderId-Element](tofolderid.md) dargestellt wird.  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |Gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MoveItem-Vorgang](moveitem-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

