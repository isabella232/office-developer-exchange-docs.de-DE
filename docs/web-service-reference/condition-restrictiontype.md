---
title: Condition (restrictiontype)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4fdb373e-bf1b-4cb0-bbfb-444c6c6cec50
description: Das Condition-Element gibt die Bedingung an, die verwendet wird, um das Ende einer Suche nach einer FindItem oder einer FindConversation-Operation zu identifizieren.
ms.openlocfilehash: 00c5b5e615ed9b253c79dae9dc2b89c797853089
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463937"
---
# <a name="condition-restrictiontype"></a>Condition (restrictiontype)

Das **Condition** -Element gibt die Bedingung an, die verwendet wird, um das Ende einer Suche nach einer **FindItem** oder einer **FindConversation** -Operation zu identifizieren. 
  
```XML
<Condition>
    <SearchExpression></SearchExpression>
</Condition>
```

 **Restrictiontype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SearchExpression](searchexpression.md) <br/> |Abstract-Element, das das ersetzte Element innerhalb einer Einschränkung darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SeekToConditionPageItemView](seektoconditionpageitemview.md) <br/> |Gibt die Bedingung an, die verwendet wird, um das Ende einer Suche, den startIndex einer Suche, die maximal zurückzugebenden Einträge und die Suchanweisungen für eine **FindItem** oder einen **FindConversation** -Vorgang zu identifizieren.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

