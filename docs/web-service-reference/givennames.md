---
title: GivenNames
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 64d86c24-07b8-448d-ad37-47f104777df3
description: Das GivenNames-Element gibt ein Array von Vornamenwerten und die Bezeichner ihrer Quellzuschreibungen für die zugeordnete Persona an.
ms.openlocfilehash: 7da46685ec9ec44a81e0aca813969bd00cb858df
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59539985"
---
# <a name="givennames"></a>GivenNames

Das **GivenNames-Element** gibt ein Array von Vornamenwerten und die Bezeichner ihrer Quellzuschreibungen für die zugeordnete Persona an. 
  
```xml
<GivenNames>
    <StringAttributedValue/>
</GivenNames>
```

 **ArrayOfStringAttributedValuesType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StringAttributedValue](stringattributedvalue.md) <br/> |Gibt eine Instanz in einem Array von Attributen an, die einem Persona-Element zugeordnet sind.  <br/> |
   
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

