---
title: Ismembershipgroup
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0dc3e285-8f49-48ad-b844-37041c0d782b
description: Das ismembershipgroup-Element gibt einen booleschen Wert an, der angibt, ob es sich bei der Entität um eine Verteilergruppe oder ein Postfach handelt.
ms.openlocfilehash: ed79961c6d13ab226c0b489103ef3d2c4a08668d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459286"
---
# <a name="ismembershipgroup"></a>Ismembershipgroup

Das **ismembershipgroup** -Element gibt einen booleschen Wert an, der angibt, ob es sich bei der Entität um eine Verteilergruppe oder ein Postfach handelt. 
  
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
|[SearchableMailbox](searchablemailbox.md) <br/> |Gibt ein Postfach an, das von einer **GetSearchableMailboxes** -Anforderung zurückgegeben wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert **true** für das **ismembershipgroup** -Element gibt an, dass es sich bei der Entität um eine Verteilergruppe oder um ein Postfach handelt. Der Wert false gibt an, dass es sich bei der Entität nicht um eine Verteilergruppe oder um ein Postfach handelt. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

