---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: IsHidden-Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll.
ms.openlocfilehash: ee20bf0af287e3cddaedb5bc6d3c63ef9a7a7006
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830032"
---
# <a name="ishidden"></a>IsHidden

**IsHidden** -Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll. 
  
```XML
<IsHidden>true | false</IsHidden>
```

 **Boolean**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Zuweisung (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Gibt eine Instanz in ein Array von Attributen für eine **Rolle** -Element an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **IsHidden** -Element gibt an, dass der zugrunde liegenden Kontakt ausgeblendet oder als Teil der Rolle angezeigt werden soll. Der Wert **false** gibt an, dass der zugrunde liegenden Kontakt nicht ausgeblendet oder als Teil der Rolle angezeigt. 
  
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

