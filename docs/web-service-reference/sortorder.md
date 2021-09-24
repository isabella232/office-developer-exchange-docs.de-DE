---
title: SortOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SortOrder
api_type:
- schema
ms.assetid: c2413f0b-8c03-46ae-9990-13338b3c53a6
description: Das SortOrder-Element definiert, wie Elemente in einer FindItem- oder FindConversation-Anforderung sortiert werden.
ms.openlocfilehash: eefa10c4af32d550414d83f8f524b5b088fcfa7c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531701"
---
# <a name="sortorder"></a>SortOrder

Das **SortOrder-Element** definiert, wie Elemente in einer **FindItem-** oder **FindConversation-Anforderung** sortiert werden. 
  
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
|[FieldOrder](fieldorder.md) <br/> |Stellt ein einzelnes Feld dar, nach dem die Ergebnisse durchsucht werden und gibt die Richtung für die Sortierung an. Eines oder mehrere dieser Elemente können eingeschlossen werden. [FieldOrder-Elemente](fieldorder.md) werden in der für die Sortierung angegebenen Reihenfolge angewendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[FindItem](finditem.md) <br/> |Definiert eine Anforderung zum Suchen von Elementen in einem Postfach.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  `/FindItem` <br/> |
|[FindConversation](findconversation.md) <br/> |Definiert eine Anforderung zum Suchen von Unterhaltungen in einem Postfach.  <br/> |
   
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



[FindItem-Vorgang](finditem-operation.md)
  
[FindConversation-Vorgang](findconversation-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

