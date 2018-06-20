---
title: Erforderlicher (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 1f26b691-7331-4c7f-a92b-dfcc66c26963
description: Erforderlicher-Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist.
ms.openlocfilehash: f314b9d27d1b4ee472d249ec49af1a785ff9ac25
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758088"
---
# <a name="domainrequired-pox"></a>Erforderlicher (POX)

**Erforderlicher** -Element gibt an, ob die Domäne für die Authentifizierung erforderlich ist. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md) 
- [Konto (POX)](account-pox.md)  
- [Protokoll (POX)](protocol-pox.md)  
- [Erforderlicher (POX)](domainrequired-pox.md)
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt an, ob die Domäne für die Authentifizierung erforderlich ist. Die möglichen Werte sind **aktiviert** und **deaktiviert**. Ist der Wert **auf**, muss die nachfolgende Anforderung die Domäne für das Konto des Benutzers enthalten.
  
## <a name="remarks"></a>Hinweise

Wenn die Domäne in die [LoginName (POX)](loginname-pox.md) Element nicht angegeben ist oder das **LoginName** -Element nicht angegeben wurde, muss der Benutzer die Domäne eingeben, bevor die Authentifizierung erfolgreich ausgeführt werden kann. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

