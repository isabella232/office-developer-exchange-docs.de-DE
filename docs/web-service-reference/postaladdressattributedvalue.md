---
title: PostalAddressAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0f92aa41-1499-4d96-a973-24529ec64d24
description: Das PostalAddressAttributedValue-Element gibt eine Instanz des ein Array von Postadressen und deren zugeordneten Hinweise.
ms.openlocfilehash: f2b8b9818e39780b934522910d016875dbe5af2e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830854"
---
# <a name="postaladdressattributedvalue"></a>PostalAddressAttributedValue

Das **PostalAddressAttributedValue** -Element gibt eine Instanz des ein Array von Postadressen und deren zugeordneten Hinweise. 
  
```XML
<PostalAddressAttributedValue>
   <Value/>
   <Attributions/>
</PostalAddressAttributedValue>
```

 **PostalAddressAttributedValueType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Wert (PersonaPostalAddressType)](value-personapostaladdresstype.md) | [Marken (ArrayOfValueAttributionsType)](attributions-arrayofvalueattributionstype.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[BusinessAddresses](businessaddresses.md) | [HomeAddresses](homeaddresses.md) | [OtherAddresses](otheraddresses.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

