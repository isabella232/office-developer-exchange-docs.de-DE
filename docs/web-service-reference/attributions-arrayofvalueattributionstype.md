---
title: Hinweise (ArrayOfValueAttributionsType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f36b6ee-8ecf-48c9-8cb6-dfb2da0ce2a2
description: Das Element Marken gibt ein Array von Marken für zugeordneten Wert Elements.
ms.openlocfilehash: a64510cacb9923682418ca8a9b203c765a129bdd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757413"
---
# <a name="attributions-arrayofvalueattributionstype"></a>Hinweise (ArrayOfValueAttributionsType)

Das Element **Marken** gibt ein Array von Marken für zugeordneten **Wert** Elements. 
  
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
|[Zuweisung (Zeichenfolge)](attribution-string.md) <br/> |Gibt eine Zeichenfolge zur Identifizierung eines Attributs verwendet.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[BodyContentAttributedValue](bodycontentattributedvalue.md) <br/> |Gibt den Textkörperinhalt eines Elements an.  <br/> |
|[EmailAddressAttributedValue](emailaddressattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von e-Mail-Adressen und deren zugeordneten Hinweise.  <br/> |
|[ExtendedPropertyAttributedValue](extendedpropertyattributedvalue.md) <br/> |Gibt die erweiterte Eigenschaften für eine Rolle.  <br/> |
|[PhoneNumberAttributedValue](phonenumberattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Telefonnummern und deren zugeordneten Hinweise.  <br/> |
|[PostalAddressAttributedValue](postaladdressattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Postanschriften und deren zugeordneten Hinweise.  <br/> |
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Zeichenfolgen-Daten für ein Element Persona.  <br/> |
|[StringAttributedValue](stringattributedvalue.md) <br/> |Gibt eine Instanz in ein Array von Attributen, die einer Rolle-Element zugeordnet ist.  <br/> |
   
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

