---
title: DomainRequired (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: Das DomainRequired-Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.
ms.openlocfilehash: 97d602c40b247f9a6650cc4440b53bf23c18482e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461324"
---
# <a name="domainrequired-pox"></a>DomainRequired (POX)

Das **DomainRequired** -Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text gibt an, ob die Domäne für die Authentifizierung erforderlich ist. Die möglichen Werte sind **ein** -und **ausgeschaltet**. Wenn der Wert **auf "on**" festgelegt ist, muss die nachfolgende Anforderung die Domäne des Benutzerkontos enthalten.
  
## <a name="remarks"></a>Bemerkungen

Wenn die Domäne nicht im [LoginName-](loginname-pox.md) Element angegeben ist oder das **LoginName** -Element nicht angegeben wurde, muss der Benutzer die Domäne eingeben, bevor die Authentifizierung erfolgreich ausgeführt wird. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

