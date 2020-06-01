---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: Das AuthPackage-Element gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Exchange-Server verwendet wird, auf dem die Postfachserverrolle installiert ist.
ms.openlocfilehash: 5317cf49d354a558417829e1d1b5b67cd6874309
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459104"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

Das **AuthPackage** -Element gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Exchange-Server verwendet wird, auf dem die Postfachserverrolle installiert ist. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Konto (POX)](account-pox.md)
  
- [Protokoll (POX)](protocol-pox.md)
  
- [AuthPackage (POX)](authpackage-pox.md)
  
```xml
<AuthPackage>basic or kerb or kerbntlm or ntlm or certificate or negotiate or nego2</AuthPackage>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text gibt das Authentifizierungsschema an, das bei der Authentifizierung mit dem Postfachserver verwendet wird. Im Folgenden sind die möglichen Werte aufgeführt:
  
- Basic
- Kerbtray
- kerbntlm
- NTLM
- certificate
- aushandeln
- nego2
    
## <a name="remarks"></a>Bemerkungen

Das **AuthPackage** -Element wird nur verwendet, wenn der [Typ (POX)-](type-pox.md) Element den Textwert von "$" oder "expr" aufweist. 
  
### <a name="version-differences"></a>Versionsunterschiede

Office 365, Exchange Online und lokale Versionen von Exchange, beginnend mit Build 15.00.0995.014, geben nur dann den Wert "Negotiate" zurück, wenn der Server für die Verwendung der Negotiate-Authentifizierung konfiguriert ist und der Client einen [X-ClientCanHandle-](pox-autodiscover-request-for-exchange.md) Header mit "Negotiate" enthält. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

