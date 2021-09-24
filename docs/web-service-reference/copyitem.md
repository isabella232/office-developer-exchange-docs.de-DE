---
title: CopyItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- CopyItem
api_type:
- schema
ms.assetid: ffb4c13e-e7ea-4e6b-87a0-509ce5371100
description: Das CopyItem-Element definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange Speicher.
ms.openlocfilehash: 7f083f09a587b4788180711039e1cfdbbe6a10cd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529176"
---
# <a name="copyitem"></a>CopyItem

Das **CopyItem-Element** definiert eine Anforderung zum Kopieren eines Elements in einem Postfach im Exchange Speicher. 
  
```XML
<CopyItem>
   <ToFolderId/>
   <ItemIds/>
   <ReturnNewItemIds/>
</CopyItem>
```

 **CopyItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ToFolderId](tofolderid.md) <br/> |Stellt den Zielordner für ein kopiertes Element dar.  <br/> |
|[ItemIds](itemids.md) <br/> |Enthält ein Array identifizierter Elemente, die in den durch das [ToFolderId-Element dargestellten](tofolderid.md) Ordner kopiert werden sollen.  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |Gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

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



[CopyItem-Vorgang](copyitem-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

