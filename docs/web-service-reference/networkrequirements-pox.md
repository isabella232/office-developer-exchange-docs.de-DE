---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: Das NetworkRequirements-Element enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters erfüllt, um eine Verbindung mit dem Server herzustellen.
ms.openlocfilehash: d588f7eb12a445fba9c997c4b9db0a6842105b4e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462724"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

Das **NetworkRequirements** -Element enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters erfüllt, um eine Verbindung mit dem Server herzustellen. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[NetworkRequirements (POX)](networkrequirements-pox.md)
  
```xml
<NetworkRequirements>
   <IPv4Start/>
   <IPv4End/>
   <IPv6Start/>
   <IPv6End/>
</NetworkRequirements>
```

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Gibt den Anfang eines Bereichs von IPv4-Adressen (IP Version 4) an, die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Identifiziert das Ende eines Bereichs von IPv4-Adressen (IP Version 4), die zum Identifizieren eines Computers im Netzwerk verwendet werden.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Gibt den Anfang eines Bereichs von IPv6-Adressen (IP Version 6) an, die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Identifiziert das Ende eines Bereichs von IPv6-Adressen (IP Version 6), die verwendet werden, um einen Computer in einem Netzwerk zu identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Wenn der e-Mail-Client nicht den Netzwerkanforderungen entspricht, sollte er andere Protokolltypen ausprobieren. ISPs können eine Gruppe von Servern mit [Protokoll-Tags (POX)](protocol-pox.md) bereitstellen, die keine Authentifizierung erfordern, aber sich im ISP-Netzwerk befinden müssen. ISPs können eine andere Gruppe von Servern auflisten, die eine Authentifizierung erfordern, sich jedoch nicht in einem bestimmten Netzwerk befinden müssen. 
  
Das **NetworkRequirements** -Element ist optional. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

