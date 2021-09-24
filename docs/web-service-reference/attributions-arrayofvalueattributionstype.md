---
title: Attributions (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: Das Attributions-Element gibt ein Array von Zuschreibungen für das zugeordnete Value-Element an.
ms.openlocfilehash: e5483e8e7ef4745e8025106ae1f1c52e91987183
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59529328"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Attributions (ArrayOfValueAttributionsType)

Das **Attributions-Element** gibt ein Array von Zuschreibungen für das zugeordnete **Value-Element** an. 
  
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
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Gibt den Textkörperinhalt eines Elements an.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von E-Mail-Adressen und deren zugeordneten Zuschreibungen an.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Gibt erweiterte Eigenschaften für eine Persona an.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Telefonnummern und deren zugeordneten Zuschreibungen an.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Postadressen und deren zugeordneten Zuschreibungen an.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Zeichenfolgendaten für ein Persona-Element an.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Gibt eine Instanz in einem Array von Attributen an, die einem Persona-Element zugeordnet sind.  <br/> |
   
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

