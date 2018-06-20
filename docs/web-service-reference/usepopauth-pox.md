---
title: UsePOPAuth (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 28f552d8-6bb8-49b4-a45c-b2053670f1cc
description: Das UsePOPAuth-Element gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für Simple Mail Transfer Protocol (SMTP) verwendet wird.
ms.openlocfilehash: be03568d697b1f5461d49dba388a1d3f1008a67e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839428"
---
# <a name="usepopauth-pox"></a>UsePOPAuth (POX)

Das **UsePOPAuth** -Element gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für Simple Mail Transfer Protocol (SMTP) verwendet wird. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[UsePOPAuth (POX)](usepopauth-pox.md)
  
```xml
<UsePOPAuth>on or off</UsePOPAuth>
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

Der Textwert gibt an, ob die Authentifizierungsinformationen angeben, die für einen POP3-Konto bereitgestellt wird auch für SMTP verwendet wird. Die möglichen Werte sind **aktiviert** und **deaktiviert**.
  
## <a name="remarks"></a>Hinweise

Das **UsePOPAuth** -Element wird nur verwendet, wenn [Type (POX)](type-pox.md) SMTP ist. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

