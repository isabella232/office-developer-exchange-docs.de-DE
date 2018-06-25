---
title: ItemClasses
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemClasses
api_type:
- schema
ms.assetid: f95430cc-2860-47c1-af2d-8c4156c9b281
description: Das ItemClasses-Element darstellt, die Element-Klassen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen.
ms.openlocfilehash: 70a4823f9017ba8c6f894394d5907f1adeb80167
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830148"
---
# <a name="itemclasses"></a>ItemClasses

Das **ItemClasses** -Element darstellt, die Element-Klassen, die auf eingehende Nachrichten in der Reihenfolge für die Bedingung oder Ausnahme anzuwendende gekennzeichnet sein müssen. 
  
```XML
<ItemClasses>
    <String/>
</ItemClasses>
```

 **ArrayOfStringsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[String](string.md) <br/> |Stellt eine einzelnes Element-Klasse.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Bedingungen](conditions.md) <br/> |Stellt die Bedingungen dar, bei deren Erfüllung die Regelaktionen für eine Regel ausgelöst werden.  <br/> |
|[Ausnahmen](exceptions.md) <br/> |Stellt die Ausnahmen, die alle verfügbaren Regel Ausnahmebedingungen für eine Posteingangsregel darstellen.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

