---
title: BodyContentAttributedValue
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: f99e9590-8388-4203-ac30-1ea394f351a6
description: Das BodyContentAttributedValue-Element gibt den Textkörperinhalt eines Elements an.
ms.openlocfilehash: 294bb0baf4915180a34701775a45e9dafbd99753
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520020"
---
# <a name="bodycontentattributedvalue"></a>BodyContentAttributedValue

Das **BodyContentAttributedValue-Element** gibt den Textkörperinhalt eines Elements an. 
  
```XML
<BodyContentAttributedValue>
   <Value></Value>
   <Attributions></Attributions>
</ BodyContentAttributedValue>
```

 **BodyContentAttributedValueType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Wert (BodyContentType)](value-bodycontenttype.md) <br/> |Gibt den Wert eines **BodyContentAttributedValue-Elements** an.  <br/> |
|[Attributions (ArrayOfPersonaAttributionsType)](attributions-arrayofpersonaattributionstype.md) <br/> |Gibt ein Array von Attributionsinformationen für einen oder mehrere der Kontakte oder Active Directory-Empfänger an, die in der zugeordneten Persona aggregiert sind.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Texte](bodies.md) <br/> |Gibt ein Array von **BodyContentAttributedValue-Elementen** an.  <br/> |
   
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

