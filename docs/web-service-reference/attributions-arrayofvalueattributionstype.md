---
title: Zuordnungen (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: Das Attributes-Element gibt ein Array von Attributes für das zugehörige Value-Element an.
ms.openlocfilehash: 9fd552670c529009838125063869f65e130c1e63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463993"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Zuordnungen (ArrayOfValueAttributionsType)

Das **Attributes** -Element gibt ein Array von Attributes für das zugehörige **value** -Element an. 
  
```XML
<Attributions>
    <Attribution></Attribution>
</Attribution>
```

 **ArrayOfValueAttributionsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Attribution (Zeichenfolge)](attribution-string.md) <br/> |Gibt eine Zeichenfolge an, die zum Identifizieren eines Attributs verwendet wird.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Gibt den Textkörper Inhalt eines Elements an.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Zuschreibungen an.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Gibt erweiterte Eigenschaften für eine Rolle an.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Telefonnummern und deren zugeordneten Zuschreibungen an.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Postadressen und deren zugeordneten Zuschreibungen an.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Zeichenfolgendaten für ein Persona-Element an.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Gibt eine Instanz in einem Array von Attributen an, die mit einem Persona-Element verknüpft sind.  <br/> |
   
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

