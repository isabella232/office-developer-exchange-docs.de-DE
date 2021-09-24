---
title: IsHidden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 2377b584-bd1e-49fc-b80a-a6634721a297
description: Das IsHidden-Element enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Persona angezeigt werden soll.
ms.openlocfilehash: 7ff24eaa5e8e7b25c87af0bf299fcca0d88dc0b6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532788"
---
# <a name="ishidden"></a>IsHidden

Das **IsHidden-Element** enthält einen booleschen Wert, der angibt, ob der zugrunde liegende Kontakt ausgeblendet oder als Teil der Persona angezeigt werden soll. 
  
```XML
<IsHidden>true | false</IsHidden>
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
|[Attribution (PersonaAttributionType)](attribution-personaattributiontype.md) <br/> |Gibt eine Instanz in einem Array von Attributen für ein **Persona-Element** an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IsHidden-Element** gibt an, dass der zugrunde liegende Kontakt ausgeblendet oder als Teil der Persona angezeigt werden soll. Der Wert **"false"** gibt an, dass der zugrunde liegende Kontakt nicht ausgeblendet oder als Teil der Persona angezeigt werden soll. 
  
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

