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
description: Das CertPrincipalName-Element gibt den Secure Sockets Layer (SSL) zertifikatprinzipalnamen an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Server 2007 Organisation mithilfe von SSL erforderlich ist.
ms.openlocfilehash: fb2a1c8577bce41945b669be56f2a94a2c4dca26
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463342"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

Das **CertPrincipalName** -Element gibt den Secure Sockets Layer (SSL) zertifikatprinzipalnamen an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Server 2007 Organisation mithilfe von SSL erforderlich ist. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange 2007 ausgeführt wird, auf dem die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Text-Wert gibt den Namen des SSL-Zertifikat Prinzipals an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Organisation mithilfe von SSL erforderlich ist.
  
## <a name="remarks"></a>Bemerkungen

Wenn das **CertPrincipalName** -Element nicht angegeben ist, wird standardmäßig auf msstd: Server festgelegt, wobei Server der Wert ist, der im [Server (POX)-](server-pox.md) Element angegeben ist. Wenn beispielsweise Server als example.com angegeben ist und **CertPrincipalName** mit aktiviertem [SSL (POX)](ssl-pox.md) leer gelassen wird, lautet der Standardwert von **CertPrincipalName** msstd:example. com. 
  
Wenn **None** angegeben ist, überprüft Windows den zertifikatprinzipalnamen gemäß den Informationen, die im Thema [Principal Names](https://go.microsoft.com/fwlink/?LinkId=93417) auf MSDN gefunden werden. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

