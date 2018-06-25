---
title: TTL (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 178eefa1-995c-4bea-930b-e51293961191
description: Das Element TTL gibt die Zeitspanne an Live, in Stunden, in denen die Einstellungen gültig.
ms.openlocfilehash: 5fecf3103553a82ed2aeeecfc1e4e1b9fe38583c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839269"
---
# <a name="ttl-pox"></a>TTL (POX)

Das Element **TTL** gibt die Zeitspanne an Live, in Stunden, in denen die Einstellungen gültig. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange Server 2007-Computer, auf dem die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt Gültigkeitsdauer, in Stunden, in denen die Einstellungen gültig. Der Wert 0 gibt an, dass diese neue Suche nicht erforderlich ist. Wenn kein Wert angegeben ist, ist der Standardwert für dieses Element 1 Stunde.
  
## <a name="remarks"></a>Hinweise

Nach Ablauf dieses Zeitraums, der durch das **TTL** -Element dargestellt wird, sollte die Einstellungen mithilfe einer Anforderung der AutoErmittlung erneut gefunden. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

