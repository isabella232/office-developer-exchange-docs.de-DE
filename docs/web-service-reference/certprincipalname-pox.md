---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: Das Element CertPrincipalName gibt den Prinzipal Secure Sockets Layer (SSL) Zertifikat-Namen, der von der Microsoft Exchange Server 2007-Organisation Herstellen einer Verbindung mit SSL erforderlich ist.
ms.openlocfilehash: d2766b16a3e8a1bcd013de332d9c07f709fcf949
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757560"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

Das Element **CertPrincipalName** gibt den Prinzipal Secure Sockets Layer (SSL) Zertifikat-Namen, der von der Microsoft Exchange Server 2007-Organisation Herstellen einer Verbindung mit SSL erforderlich ist. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[CertPrincipalName (POX)](certprincipalname-pox.md)
  
```xml
<CertPrincipalName>none or servername</CertPrinicpalName>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer mit Exchange 2007, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt den SSL-Zertifikat principal Name, der von der Microsoft Exchange-Organisation Herstellen einer Verbindung mit SSL erforderlich ist.
  
## <a name="remarks"></a>Hinweise

Wenn das Element **CertPrincipalName** nicht angegeben wird, ist die Standardeinstellung auf Msstd:SERVER, festlegen SERVER ist, auf dem der Wert, der im [Server (POX)](server-pox.md) -Element angegeben ist. Angenommen, wenn der SERVER als example.com angegeben ist, und **CertPrincipalName** mit [SSL (POX)](ssl-pox.md) eingeschaltet ist leer, wäre der Standardwert der **CertPrincipalName** msstd:example.com. 
  
Wenn **keines** angegeben ist, wird Windows den Prinzipal Zertifikatnamen entsprechend den Informationen im Thema [Dienstprinzipalnamen](http://go.microsoft.com/fwlink/?LinkId=93417) auf MSDN überprüfen. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

