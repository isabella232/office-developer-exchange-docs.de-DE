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
description: Das LegacyDN-Element identifiziert das Postfach eines Benutzers anhand des Legacy Distinguished Name.
ms.openlocfilehash: b9af4278a5421dc932573396c3563a64a78de41e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526382"
---
# <a name="legacydn-pox"></a>LegacyDN (POX)

Das **LegacyDN** -Element identifiziert das Postfach eines Benutzers anhand des Legacy Distinguished Name. 
  
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
|[Benutzer (POX)](user-pox.md) <br/> |Enthält benutzerspezifische Informationen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die ältere e-Mail-Adresse eines Benutzers dar.
  
## <a name="remarks"></a>Bemerkungen

Das [NonEmptyStringType-Element (Email)](emailaddress-nonemptystringtype.md) ist ein alternatives Element für eine Auto Ermittlungsanforderung. Sie wird verwendet, wenn ein Postfach auf einem Computer mit Microsoft Exchange Server 2007 vorhanden ist. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

