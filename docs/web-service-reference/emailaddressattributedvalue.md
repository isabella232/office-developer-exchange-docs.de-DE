---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: Das EmailAddressAttributedValue-Element gibt eine Instanz des ein Array von e-Mail-Adressen und deren zugeordneten Hinweise.
ms.openlocfilehash: 3bcbb5c0a2bc9a2dc24516b5fc62e6e3363a360b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758175"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

Das **EmailAddressAttributedValue** -Element gibt eine Instanz des ein Array von e-Mail-Adressen und deren zugeordneten Hinweise. 
  
```XML
<EmailAddressAttributedValue>
    <Value></Value>
    <Attributions></Attributions>
<EmailAddressAttributedValue>
```

 **EmailAddressAttributedValueType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Wert (EmailAddressType)](value-emailaddresstype.md) <br/> |Gibt an, dass ein Array Marken der Wert der ein **EmailAddress** zugeordnet.  <br/> |
|[Hinweise (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Gibt ein Array von Marken für zugeordneten **Wert** Elements an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Gibt ein Array von Werten für e-Mail und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.  <br/> |
|[Emails2](emails2.md) <br/> |Gibt ein Array von Werten für e-Mail und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.  <br/> |
|[Emails3](emails3.md) <br/> |Gibt ein Array von Werten für e-Mail und die Bezeichner der ihre Marken Quelle für die zugeordneten Rolle.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

