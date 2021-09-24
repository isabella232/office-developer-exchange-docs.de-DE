---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: Das EmailAddressAttributedValue-Element gibt eine Instanz eines Arrays von E-Mail-Adressen und deren zugeordneten Zuschreibungen an.
ms.openlocfilehash: 2b5e9b431b6a62c63e815bfee190c923f454c867
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519765"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

Das **EmailAddressAttributedValue-Element** gibt eine Instanz eines Arrays von E-Mail-Adressen und deren zugeordneten Zuschreibungen an. 
  
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
|[Wert (EmailAddressType)](value-emailaddresstype.md) <br/> |Gibt den Wert einer **EmailAddress** an, die einem Attributionsarray zugeordnet ist.  <br/> |
|[Attributions (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Gibt ein Array von Zuschreibungen für das zugeordnete **Value-Element** an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Gibt ein Array von E-Mail-Werten und die Bezeichner ihrer Quellzuschreibungen für die zugeordnete Persona an.  <br/> |
|[Emails2](emails2.md) <br/> |Gibt ein Array von E-Mail-Werten und die Bezeichner ihrer Quellzuschreibungen für die zugeordnete Persona an.  <br/> |
|[Emails3](emails3.md) <br/> |Gibt ein Array von E-Mail-Werten und die Bezeichner ihrer Quellzuschreibungen für die zugeordnete Persona an.  <br/> |
   
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

