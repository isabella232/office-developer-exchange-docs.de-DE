---
title: EmailAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ebdf224d-3796-4179-aa0a-87942e7585ff
description: Das EmailAddressAttributedValue-Element gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an.
ms.openlocfilehash: 09fdd5921cef3d70a6da4b6d4d38f08834c5d482
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530691"
---
# <a name="emailaddressattributedvalue"></a>EmailAddressAttributedValue

Das **EmailAddressAttributedValue** -Element gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an. 
  
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
|[Wert (e-mailemailtype)](value-emailaddresstype.md) <br/> |Gibt den Wert einer e- **mailemail** an, die einem attributes-Array zugeordnet ist.  <br/> |
|[Zuordnungen (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md) <br/> |Gibt ein Array von Attributes für das zugehörige **value** -Element an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Emails1](emails1.md) <br/> |Gibt ein Array von e-Mail-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.  <br/> |
|[Emails2](emails2.md) <br/> |Gibt ein Array von e-Mail-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.  <br/> |
|[Emails3](emails3.md) <br/> |Gibt ein Array von e-Mail-Werten und die Bezeichner ihrer Quell Zuweisungen für die zugeordnete Rolle an.  <br/> |
   
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

