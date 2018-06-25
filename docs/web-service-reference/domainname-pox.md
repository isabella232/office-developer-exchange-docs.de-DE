---
title: DomainName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2b4af2b2-58b5-4f28-9cb3-c07a11377747
description: Das DomainName-Element gibt die Domäne des Benutzers an.
ms.openlocfilehash: c38d2e470bd174ab6dd7e5e1dd3eee23daea5e69
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758092"
---
# <a name="domainname-pox"></a>DomainName (POX)

Das **DomainName** -Element gibt die Domäne des Benutzers an. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md)  
- [Konto (POX)](account-pox.md) 
- [Protokoll (POX)](protocol-pox.md) 
- [DomainName (POX)](domainname-pox.md)
  
```xml
<DomainName/>
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

Der Textwert gibt die Domäne des Benutzers an.
  
## <a name="remarks"></a>Hinweise

Wenn kein Wert angegeben ist, wird die Standardauthentifizierung die E-mail-Adresse als ein Benutzer Benutzerprinzipalnamens (UPN) Format verwenden. Beispiel: \<Username\>@\<Domäne\>.
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

