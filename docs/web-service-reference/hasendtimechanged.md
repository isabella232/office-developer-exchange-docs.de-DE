---
title: HasEndTimeChanged
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: a0eb444d-8e2e-478b-b785-2b9787ffb226
description: Das HasEndTimeChanged-Element gibt an, ob sich die Endzeit für eine Besprechung geändert hat.
ms.openlocfilehash: f5f0c54e210219566786980ca02f33d72307dcff
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59516776"
---
# <a name="hasendtimechanged"></a>HasEndTimeChanged

Das **HasEndTimeChanged-Element** gibt an, ob sich die Endzeit für eine Besprechung geändert hat. 
  
```XML
<HasEndTimeChanged>true | false</HasEndTimeChanged>
```

 **Boolescher Wert**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ChangeHighlights](changehighlights.md) <br/> |Gibt an, was sich zwischen zwei Versionen einer Besprechungsanfrage geändert hat.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **HasEndTimeChanged-Element** gibt an, dass sich die Endzeit einer Besprechung geändert hat. Der Wert **"false"** gibt an, dass sich die Endzeit einer Besprechung nicht geändert hat. 
  
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

