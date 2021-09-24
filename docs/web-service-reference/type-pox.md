---
title: Typ (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: 9a627244-554f-4223-b9d8-a601b81a4a1a
description: Das Type-Element identifiziert den Typ des konfigurierten E-Mail-Kontos.
ms.openlocfilehash: bb92913071509fec46736341bce56b1a00730f6b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59517525"
---
# <a name="type-pox"></a>Typ (POX)

Das **Type-Element** identifiziert den Typ des konfigurierten E-Mail-Kontos. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Exchange Server.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt den Typ des E-Mail-Kontos dar. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|EXCH  <br/> |Das Protokoll, das zum Herstellen einer Verbindung mit dem Server verwendet wird, ist Exchange RPC.  <br/> |
|EXHTTP  <br/> |Das Protokoll, das zum Herstellen einer Verbindung mit den RPC/HTTP-Verbindungen des Servers verwendet wird.  <br/> |
|EXPR  <br/> |Das Protokoll, das zum Herstellen einer Verbindung mit dem Server verwendet wird, ist Exchange RPC über HTTP unter Verwendung eines RPC-Proxyservers.  <br/> Dies gilt nur, wenn das [POX-Element (AccountType)](accounttype-pox.md) auf E-Mail festgelegt ist.  <br/> |
|WEB  <br/> |Der Zugriff auf E-Mail erfolgt über einen Webbrowser mithilfe der URL, die im [Serverelement (POX)](server-pox.md) angegeben ist.  <br/> Dies gilt nur, wenn das [POX-Element (AccountType)](accounttype-pox.md) auf E-Mail festgelegt ist.  <br/> |
   
### <a name="version-differences"></a>Versionsunterschiede

Office 365, Exchange Online und lokale Versionen von Exchange ab Build 15.00.0995.014 geben nur dann den Wert "EXHTTP" zurück, wenn der Server so konfiguriert ist, dass RPC/HTTP-Verbindungen akzeptiert werden und der Client einen [X-ClientCanHandle-Header](pox-autodiscover-request-for-exchange.md) mit "ExHttpInfo" enthält. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

