---
title: Untergeordnetes Element (ArrayOfStringArrayAttributedValuesType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: d37b3fd5-63f1-4003-a6ec-54adfce23d52
description: Das Children-Element gibt ein Array von untergeordneten Namen und Bezeichnern ihrer Quellzuschreibungen für die zugeordnete Persona an.
ms.openlocfilehash: 878f491af3047d313920cd0f3574de2daa8c21f0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59536974"
---
# <a name="children-arrayofstringarrayattributedvaluestype"></a>Untergeordnetes Element (ArrayOfStringArrayAttributedValuesType)

Das **Children-Element** gibt ein Array von untergeordneten Namen und Bezeichnern ihrer Quellzuschreibungen für die zugeordnete Persona an. 
  
```XML
<Children>
    <StringAttributedValue></StringAttributedValue>
</Children>
```

 **ArrayOfStringArrayAttributedValuesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StringArrayAttributedValue](stringarrayattributedvalue.md) <br/> |Gibt eine Instanz eines Arrays von Zeichenfolgendaten für ein Persona-Element an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Gibt eine Reihe von Persona-Daten an, die von einer **GetPersona-Anforderung** zurückgegeben werden.  <br/> |
   
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

