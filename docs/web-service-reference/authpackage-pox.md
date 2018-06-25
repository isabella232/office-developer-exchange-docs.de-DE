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
description: Das AuthPackage-Element gibt das Authentifizierungsschema, das verwendet wird, wenn der Exchange-Server authentifiziert, die die Postfach-Serverrolle installiert ist.
ms.openlocfilehash: 120ec00ac82166ae2002a8fbac0edf9a1e23afc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757410"
---
# <a name="authpackage-pox"></a>AuthPackage (POX)

Das **AuthPackage** -Element gibt das Authentifizierungsschema, das verwendet wird, wenn der Exchange-Server authentifiziert, die die Postfach-Serverrolle installiert ist. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Clientzugriffsserver an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert gibt das Authentifizierungsschema, das verwendet wird, wenn auf dem Postfachserver zu authentifizieren. Im Folgenden sind die möglichen Werte aufgeführt:
  
- grundlegende
- Kerbtray
- kerbntlm
- NTLM
- certificate
- Verhandeln
- nego2
    
## <a name="remarks"></a>Hinweise

Das **AuthPackage** -Element wird nur verwendet, wenn das Element [Typ (POX)](type-pox.md) ein Textwerts EXCH oder AUSDR vorhanden ist. 
  
### <a name="version-differences"></a>Versionsunterschiede

Office 365, Exchange Online und lokale Versionen von Exchange beginnend mit erstellen 15.00.0995.014 zurück Wert "aushandeln" nur, wenn der Server so konfiguriert ist, dass aushandeln-Authentifizierung verwenden und der Client einen [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) -Header enthält, "Aushandeln" enthält. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

