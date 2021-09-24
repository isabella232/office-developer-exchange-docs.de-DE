---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: Das TTL-Element gibt die Zeit bis Zum Live in Stunden an, während der die Einstellungen gültig bleiben.
ms.openlocfilehash: 6850f104fe90ae941f9d1d522fa3d3641e433c5f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515103"
---
# <a name="ttl-pox"></a>TTL (POX)

Das **TTL-Element** gibt die Zeit bis Zum Live in Stunden an, während der die Einstellungen gültig bleiben. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[TTL (POX)](ttl-pox.md)
  
```xml
<TTL/>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem computer Exchange Server 2007, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die Zeit zu Live in Stunden dar, in denen die Einstellungen gültig bleiben. Der Wert Null gibt an, dass keine Verweigerung erforderlich ist. Wenn kein Wert angegeben ist, ist der Standardwert für dieses Element 1 Stunde.
  
## <a name="remarks"></a>HinwBemerkungeneise

Nachdem die durch das **TTL-Element** dargestellte Zeit abgelaufen ist, sollten die Einstellungen mithilfe einer AutoErmittlungsanforderung aufgehoben werden. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

