---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: Das DomainRequired-Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.
ms.openlocfilehash: 906c99ff7a8428404ee6045b749cdb0afed882b7
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540062"
---
# <a name="domainrequired-pox"></a>DomainRequired (POX)

Das **DomainRequired-Element** gibt an, ob die Domäne für die Authentifizierung erforderlich ist. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md) 
- [Konto (POX)](account-pox.md)  
- [Protokoll (POX)](protocol-pox.md)  
- [DomainRequired (POX)](domainrequired-pox.md)
  
```xml
<DomainRequired>on or off</DomainRequired>
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

Der Textwert gibt an, ob die Domäne für die Authentifizierung erforderlich ist. Die möglichen Werte sind **aktiviert** und **deaktiviert.** Wenn der Wert **aktiviert** ist, muss die nachfolgende Anforderung die Domäne des Benutzerkontos enthalten.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn die Domäne nicht im [POX-Element (LoginName)](loginname-pox.md) angegeben ist oder das **LoginName-Element** nicht angegeben wurde, muss der Benutzer die Domäne eingeben, bevor die Authentifizierung erfolgreich ist. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

