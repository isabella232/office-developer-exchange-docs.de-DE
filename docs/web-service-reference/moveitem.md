---
title: MoveItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoveItem
api_type:
- schema
ms.assetid: a4593377-22dd-415f-b01d-387389ef650f
description: Das MoveItem-Element definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher.
ms.openlocfilehash: 61dbb91cc20a71f50999241b3daa21bf8ebfbcc8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530401"
---
# <a name="moveitem"></a>MoveItem

Das **MoveItem** -Element definiert eine Anforderung zum verlagern eines Elements in der Exchange-Informationsspeicher. 
  
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
|[Tofolder-Datei](tofolderid.md) <br/> |Stellt den Zielordner für ein verschobenes Element dar.  <br/> |
|[ItemIds](itemids.md) <br/> |Enthält ein Array von identifizierten Elementen, das in den durch das [tofolder](tofolderid.md) -Element dargestellten Ordner zu navigieren ist.  <br/> |
|[ReturnNewItemIds](returnnewitemids.md) <br/> |Gibt an, ob die Elementbezeichner neuer Elemente in der Antwort zurückgegeben werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[MoveItem-Vorgang](moveitem-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

