---
title: NetworkRequirements (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 1555fd2e-05b6-4b94-907b-dae9174049d9
description: Das NetworkRequirements-Element enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters (ISP) für die Verbindung mit dem Server erfüllt.
ms.openlocfilehash: 07a258ad48b74c614ce367db0f893ed884cf3f75
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59509514"
---
# <a name="networkrequirements-pox"></a>NetworkRequirements (POX)

Das **NetworkRequirements-Element** enthält die Kriterien, die verwendet werden, um zu bestimmen, ob sich der Clientcomputer in einem Netzwerk befindet, das die Anforderungen des Internetdienstanbieters (ISP) für die Verbindung mit dem Server erfüllt. 
  
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
|[IPv4Start (POX)](ipv4start-pox.md) <br/> |Gibt den Anfang eines Bereichs von IP-Adressen der Version 4 (IPv4) an, die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.  <br/> |
|[IPv4End (POX)](ipv4end-pox.md) <br/> |Identifiziert das Ende eines Bereichs von IP-Adressen der Version 4 (IPv4), die zum Identifizieren eines Computers im Netzwerk verwendet werden.  <br/> |
|[IPv6Start (POX)](ipv6start-pox.md) <br/> |Gibt den Anfang eines Bereichs von IPv6-Adressen (IP Version 6) an, die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.  <br/> |
|[IPv6End (POX)](ipv6end-pox.md) <br/> |Identifiziert das Ende eines Bereichs von IP-Adressen der Version 6 (IPv6), die zum Identifizieren eines Computers in einem Netzwerk verwendet werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Wenn der E-Mail-Client nicht den Netzwerkanforderungen entspricht, sollte er andere Protokolltypen testen. ISPs stellen möglicherweise eine Gruppe von Servern mit [POX-Tags (Protocol)](protocol-pox.md) bereit, die keine Authentifizierung erfordern, sich jedoch im ISP-Netzwerk befinden müssen. ISPs können eine andere Gruppe von Servern auflisten, die eine Authentifizierung erfordern, sich jedoch nicht in einem bestimmten Netzwerk befinden müssen. 
  
Das **NetworkRequirements-Element** ist optional. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

