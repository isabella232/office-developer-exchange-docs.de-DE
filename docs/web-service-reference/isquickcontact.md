---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: Das IsQuickContact-Element gibt einen booleschen Wert an, der angibt, ob der zugrunde liegende Kontakt ein Schneller Kontakt ist.
ms.openlocfilehash: 7821332e685b44983787ce05cc6b6ef4250ee01d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509686"
---
# <a name="isquickcontact"></a>IsQuickContact

Das **IsQuickContact-Element** gibt einen booleschen Wert an, der angibt, ob der zugrunde liegende Kontakt ein Schneller Kontakt ist. 
  
```XML
<IsQuickContact>true | false</IsQuickContact>
```

 **boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Gibt eine Instanz in einem Array von Attributen für ein **Persona-Element** an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IsQuickContact-Element** gibt an, dass der Kontakt ein Schnellkontakt ist. Der Wert **"false"** gibt an, dass es sich bei dem Kontakt nicht um einen schnellen Kontakt handelt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

