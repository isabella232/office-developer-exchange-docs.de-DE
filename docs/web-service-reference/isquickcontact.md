---
title: IsQuickContact
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1c9542d6-ef72-4743-828a-bb671e783836
description: Das IsQuickContact-Element gibt einen booleschen Wert an, der angibt, ob der zugrunde liegende Kontakt ein schnell Kontakt ist.
ms.openlocfilehash: a8944be111a8dcbe914601ffc4e31794422d58aa
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44441576"
---
# <a name="isquickcontact"></a>IsQuickContact

Das **IsQuickContact** -Element gibt einen booleschen Wert an, der angibt, ob der zugrunde liegende Kontakt ein schnell Kontakt ist. 
  
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
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Gibt eine Instanz in einem Array von Attributen für ein **Persona** -Element an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **IsQuickContact** -Element gibt an, dass es sich bei dem Kontakt um einen schnell Kontakt handelt. Der Wert **false** gibt an, dass es sich bei dem Kontakt nicht um einen schnell Kontakt handelt. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

