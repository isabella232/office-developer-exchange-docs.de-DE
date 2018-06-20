---
title: LegacyDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9fb9529f-52c5-4907-a84b-935b78de16c3
description: Das Element LegacyDN identifiziert Postfach eines Benutzers von legacy-DN.
ms.openlocfilehash: f7ec1dea29a7d3ad6d470ef7812390d179fe1d2a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830243"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

Das Element **LegacyDN** identifiziert Postfach eines Benutzers von legacy-DN. 
  
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
|[Benutzer (POX)](user-pox.md) <br/> |Benutzerspezifische Informationen enthält.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die ältere e-Mail-Adresse eines Benutzers.
  
## <a name="remarks"></a>Hinweise

Das Element ["EmailAddress" (NonEmptyStringType)](emailaddress-nonemptystringtype.md) ist ein alternativer Element für eine Anforderung der AutoErmittlung. Es wird verwendet, wenn ein Postfach auf einem Computer vorhanden ist, auf dem Microsoft Exchange Server 2007 ausgeführt wird. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

