---
title: ReferralPort (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: cd693f1e-fed4-4eb9-8297-178906f47050
description: Das ReferralPort-Element gibt den Port an, der verwendet wird, um einen Verweis auf ein Verzeichnis abzurufen.
ms.openlocfilehash: a2cafd0c634d48b1d4393ef69c31620036d8ad3b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513535"
---
# <a name="referralport-pox"></a>ReferralPort (POX)

Das **ReferralPort-Element** gibt den Port an, der verwendet wird, um einen Verweis auf ein Verzeichnis abzurufen. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[ReferralPort (POX)](referralport-pox.md)
  
```xml
<ReferralPort/>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Port dar, der für den Zugriff auf den Exchange Server verwendet wird.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **ReferralPort-Element** wird nur verwendet, wenn das [Type (POX)-Element](type-pox.md) exch oder EXPR entspricht. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

