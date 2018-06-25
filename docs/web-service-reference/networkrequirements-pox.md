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
description: Das NetworkRequirements-Element enthält die Kriterien, die verwendet werden, um festzustellen, ob der Clientcomputer in einem Netzwerk, die erfüllt die Anforderungen des Internet-Dienstanbieters (ISP ist), um mit dem Server herstellen.
ms.openlocfilehash: f3abcff04cd4121b8dcc7ceff7658ad389e6d0b0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830529"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

Das **NetworkRequirements** -Element enthält die Kriterien, die verwendet werden, um festzustellen, ob der Clientcomputer in einem Netzwerk, die erfüllt die Anforderungen des Internet-Dienstanbieters (ISP ist), um mit dem Server herstellen. 
  
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
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Gibt den Beginn einer Reihe von IP-Version 4 (IPv4)-Adressen, die zur Identifizierung von eines Computers in einem Netzwerk verwendet werden.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Bezeichnet das Ende einer Reihe von IP-Version 4 (IPv4)-Adressen, die verwendet werden, um einen Computer im Netzwerk zu identifizieren.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Identifiziert den Anfang des einen Bereich von IP Version 6 (IPv6)-Adressen, die zur Identifizierung von eines Computers in einem Netzwerk verwendet werden.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Bezeichnet das Ende einer Reihe von IP-Version 6 (IPv6)-Adressen, die zur Identifizierung von eines Computers in einem Netzwerk verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="remarks"></a>Hinweise

Wenn der e-Mail-Client nicht die netzwerkanforderungen entspricht, sollte es anderen Protokolltypen versuchen. Internetdienstanbieter vorsehen eine Gruppe von Servern mit [Protocol (POX)](protocol-pox.md) Tags, die erforderlich sind, erfordern keine Authentifizierung ISP-Netzwerk befinden. Internetdienstanbieter können einen anderen Satz von Servern aufzulisten, die Authentifizierung erfordern, nicht aber ein bestimmtes Netzwerk befinden. 
  
Das **NetworkRequirements** -Element ist optional. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

