---
title: Typ (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Das Type-Element identifiziert den Typ des konfigurierten e-Mail-Kontos.
ms.openlocfilehash: 6e1349769c6a5349304f576419e0c609d3edd9a0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839271"
---
# <a name="type-pox"></a>Typ (POX)

Das **Type** -Element identifiziert den Typ des konfigurierten e-Mail-Kontos. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Typ (POX)](type-pox.md)
  
```XML
<Type>WEB or EXCH or EXPR or EXHTTP</Type>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Typ des e-Mail-Konto. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|EXCH  <br/> |Das Protokoll, das für die Verbindung mit dem Server verwendet wird, ist Exchange RPC.  <br/> |
|EXHTTP  <br/> |Das Protokoll, das zum Herstellen einer Verbindung der Server RPC/HTTP-Verbindungen verwendet wird.  <br/> |
|AUSDR  <br/> |Das Protokoll, das verwendet wird, um mit dem Server herstellen ist Exchange – RPC über HTTP mit RPC-Proxyserver.  <br/> Dies gilt nur, wenn das Element [AccountType (POX)](accounttype-pox.md) auf e-Mails festgelegt ist.  <br/> |
|WEB  <br/> |E-Mail ist über einen Webbrowser zugegriffen, über die URL, die im [Server (POX)](server-pox.md) -Element angegeben ist.  <br/> Dies gilt nur, wenn das Element [AccountType (POX)](accounttype-pox.md) auf e-Mails festgelegt ist.  <br/> |
   
### <a name="version-differences"></a>Versionsunterschiede

Office 365, Exchange Online und lokale Versionen von Exchange beginnend mit erstellen 15.00.0995.014 return Wert "EXHTTP" nur, wenn der Server so konfiguriert ist, dass um RPC/HTTP-Verbindungen zu übernehmen und der Client eine [X-ClientCanHandle](pox-autodiscover-request-for-exchange.md) -Kopfzeile enthält, "ExHttpInfo" enthält. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

