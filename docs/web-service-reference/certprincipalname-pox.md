---
title: CertPrincipalName (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: a24092c9-58be-4008-92c4-68ec5c6c0fa6
description: Das CertPrincipalName-Element gibt den SSL-Zertifikatprinzipalnamen (Secure Sockets Layer) an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Server 2007-Organisation mithilfe von SSL erforderlich ist.
ms.openlocfilehash: 69ee49cdad09032c269ffbbcc918044daf61cb9b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523251"
---
# <a name="certprincipalname-pox"></a>CertPrincipalName (POX)

Das **CertPrincipalName-Element** gibt den SSL-Zertifikatprinzipalnamen (Secure Sockets Layer) an, der zum Herstellen einer Verbindung mit der Microsoft Exchange Server 2007-Organisation mit ssl erforderlich ist. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Exchange 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt den SSL-Zertifikatprinzipalnamen an, der zum Herstellen einer Verbindung mit der Microsoft Exchange-Organisation mit ssl erforderlich ist.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn das **CertPrincipalName-Element** nicht angegeben ist, wird der Standardwert auf msstd:SERVER festgelegt, wobei SERVER der wert ist, der im [Server (POX)-Element](server-pox.md) angegeben ist. Wenn SERVER beispielsweise als example.com angegeben wird und **CertPrincipalName** leer bleibt und [SSL (POX)](ssl-pox.md) aktiviert ist, lautet der Standardwert von **CertPrincipalName** msstd:example.com. 
  
Wenn **keine** Angabe erfolgt, überprüft Windows den Zertifikatprinzipalnamen gemäß den Informationen im Thema ["Prinzipalnamen"](https://go.microsoft.com/fwlink/?LinkId=93417) auf MSDN. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

