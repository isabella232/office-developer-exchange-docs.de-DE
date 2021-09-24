---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: Das LegacyDN-Element identifiziert das Postfach eines Benutzers anhand eines älteren Distinguished Name.
ms.openlocfilehash: bd65e18daf1b05f66ebd767635cbe6a3135f1abf
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540832"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

Das **LegacyDN-Element** identifiziert das Postfach eines Benutzers anhand eines älteren Distinguished Name. 
  
```xml
<LegacyDN/>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Anforderung (POX)](request-pox.md) <br/> |Enthält die Anforderung an den AutoErmittlungsdienst.  <br/> |
|[Benutzer (POX)](user-pox.md) <br/> |Stellt benutzerspezifische Informationen bereit.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die ältere E-Mail-Adresse eines Benutzers dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das [EmailAddress (NonEmptyStringType)-Element](emailaddress-nonemptystringtype.md) ist ein alternatives Element für eine AutoErmittlungsanforderung. Es wird verwendet, wenn ein Postfach auf einem Computer vorhanden ist, auf dem Microsoft Exchange Server 2007 ausgeführt wird. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

