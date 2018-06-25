---
title: SortOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: Das SortOrder-Element definiert, wie Elemente in einer Anforderung FindItem oder FindConversation sortiert werden.
ms.openlocfilehash: e20e5eab7972616c90079786abd78a0f7fedfebe
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831519"
---
# <a name="sortorder"></a>SortOrder

Das **SortOrder** -Element definiert, wie Elemente in einer Anforderung **FindItem** oder **FindConversation** sortiert werden. 
  
```xml
<SortOrder>
   <FieldOrder/>
</SortOrder>
```

 **NonEmptyArrayOfFieldOrdersType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FieldOrder](fieldorder.md) <br/> |Stellt ein einzelnes Feld dar, nach dem die Ergebnisse durchsucht werden und gibt die Richtung für die Sortierung an. Eine oder mehrere der folgenden Elemente können enthalten sein. [FieldOrder](fieldorder.md) Elemente werden in der Reihenfolge angegeben, die für die Sortierung angewendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach an.  <br/> Es folgt der XPath-Ausdruck, der dieses Element:`/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung an Unterhaltungen in einem Postfach suchen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation Operation](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

