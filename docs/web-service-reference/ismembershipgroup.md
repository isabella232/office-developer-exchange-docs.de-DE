---
title: IsMembershipGroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: Das IsMembershipGroup-Element gibt einen booleschen Wert an, der angibt, ob die Entität eine Verteilergruppe oder ein Postfach ist.
ms.openlocfilehash: 111a517a5258a48aada1c7768c908d62f3a47b9e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540979"
---
# <a name="ismembershipgroup"></a>IsMembershipGroup

Das **IsMembershipGroup-Element** gibt einen booleschen Wert an, der angibt, ob die Entität eine Verteilergruppe oder ein Postfach ist. 
  
```XML
<IsMembershipGroup>true | false</IsMembershipGroup>
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
|[SearchableMailbox](searchablemailbox.md) <br/> |Gibt ein Postfach an, das von einer **GetSearchableMailboxes-Anforderung** zurückgegeben wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **"true"** für das **IsMembershipGroup-Element** gibt an, dass es sich bei der Entität um eine Verteilergruppe oder ein Postfach handelt. Der Wert "false" gibt an, dass es sich bei der Entität nicht um eine Verteilergruppe oder ein Postfach handelt. 
  
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

