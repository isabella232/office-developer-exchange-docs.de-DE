---
title: AuthRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 241a23ee-d2a2-4724-b794-d0d523d480a2
description: Das AuthRequired-Element gibt an, ob eine Authentifizierung erforderlich ist.
ms.openlocfilehash: e40325f0327cec8dbd647e05cd18951aa991340b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59526872"
---
# <a name="authrequired-pox"></a>AuthRequired (POX)

Das **AuthRequired-Element** gibt an, ob eine Authentifizierung erforderlich ist. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Konto (POX)](account-pox.md)
  
- [Protokoll (POX)](protocol-pox.md)
  
- [AuthRequired (POX)](authrequired-pox.md)
  
```xml
<AuthRequired>on or off</AuthRequired>
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

Der Textwert gibt an, ob eine Authentifizierung erforderlich ist. Die möglichen Werte sind **aktiviert** und **deaktiviert.** Wenn kein Wert angegeben ist, ist der Standardwert **aktiviert.** 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

