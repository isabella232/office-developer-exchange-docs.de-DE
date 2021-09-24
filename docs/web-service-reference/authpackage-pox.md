---
title: AuthPackage (POX)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 709dbe53-6141-41f8-a2b9-a399bae47991
description: Das AuthPackage-Element gibt das Authentifizierungsschema an, das bei der Authentifizierung bei dem Exchange Server verwendet wird, auf dem die Postfachserverrolle installiert ist.
ms.openlocfilehash: aff4e84cd44d76c2c5a913b6627e1b0c87bab4dc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513024"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

Das **AuthPackage-Element** gibt das Authentifizierungsschema an, das bei der Authentifizierung bei dem Exchange Server verwendet wird, auf dem die Postfachserverrolle installiert ist. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Clientzugriffsserver.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt das Authentifizierungsschema an, das bei der Authentifizierung beim Postfachserver verwendet wird. Im Folgenden sind die möglichen Werte aufgeführt:
  
- basic
- Kerb
- kerbntlm
- Ntlm
- certificate
- Verhandeln
- nego2
    
## <a name="remarks"></a>HinwBemerkungeneise

Das **AuthPackage-Element** wird nur verwendet, wenn das [Type (POX)-Element](type-pox.md) den Textwert EXCH oder EXPR aufweist. 
  
### <a name="version-differences"></a>Versionsunterschiede

Office 365-, Exchange Online- und lokale Versionen von Exchange ab Build 15.00.0995.014 geben nur dann den Wert "negotiate" zurück, wenn der Server für die Verwendung der Negotiate-Authentifizierung konfiguriert ist und der Client einen [X-ClientCanHandle-Header](pox-autodiscover-request-for-exchange.md) enthält, der "Negotiate" enthält. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

