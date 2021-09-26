---
title: Bedingung (RestrictionType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: Das Condition-Element gibt die Bedingung an, die verwendet wird, um das Ende einer Suche nach einem FindItem- oder FindConversation-Vorgang zu identifizieren.
ms.openlocfilehash: f6292d2d25b9d236d0bb611c41a4cfcf490b6df4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543527"
---
# <a name="condition-restrictiontype"></a>Bedingung (RestrictionType)

Das **Condition-Element** gibt die Bedingung an, die verwendet wird, um das Ende einer Suche nach einem **FindItem-** oder **FindConversation-Vorgang** zu identifizieren. 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 **RestrictionType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> |Abstraktes Element, das das ersetzte Element innerhalb einer Einschränkung darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Gibt die Bedingung an, die verwendet wird, um das Ende einer Suche, den Startindex einer Suche, die maximal zurückzugebenden Einträge und die Suchanweisungen für ein **FindItem-** oder **einen FindConversation-Vorgang** zu identifizieren.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

