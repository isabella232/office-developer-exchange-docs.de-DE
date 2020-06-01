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
description: Das Type-Element gibt den Typ des konfigurierten e-Mail-Kontos an.
ms.openlocfilehash: ad3570094ebe28498dfdc375cf7fc255434ba20d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465100"
---
# <a name="type-pox"></a>Typ (POX)

Das **Type** -Element gibt den Typ des konfigurierten e-Mail-Kontos an. 
  
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

Der Wert Text stellt den Typ des e-Mail-Kontos dar. In der folgenden Tabelle sind die möglichen Werte aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Exch  <br/> |Das Protokoll, das zum Herstellen einer Verbindung mit dem Server verwendet wird, ist Exchange RPC.  <br/> |
|Http  <br/> |Das Protokoll, das zum Herstellen einer Verbindung mit den Server-RPC/HTTP-Verbindungen verwendet wird.  <br/> |
|EXPR  <br/> |Das Protokoll, das zum Herstellen einer Verbindung mit dem Server verwendet wird, ist Exchange-RPC-über-HTTP mit einem RPC-Proxy Server.  <br/> Dies gilt nur, wenn das [POX-Element (AccountType)](accounttype-pox.md) auf e-Mail festgelegt ist.  <br/> |
|Web  <br/> |Der Zugriff auf E-Mail erfolgt über einen Webbrowser mithilfe der URL, die im [Server (POX)](server-pox.md) -Element angegeben ist.  <br/> Dies gilt nur, wenn das [POX-Element (AccountType)](accounttype-pox.md) auf e-Mail festgelegt ist.  <br/> |
   
### <a name="version-differences"></a>Versionsunterschiede

Office 365, Exchange Online und lokale Versionen von Exchange, die mit Build 15.00.0995.014 beginnen, geben nur dann den Wert "http" zurück, wenn der Server so konfiguriert ist, dass er RPC/HTTP-Verbindungen akzeptiert, und der Client einen [X-ClientCanHandle-](pox-autodiscover-request-for-exchange.md) Header enthält, der "ExHttpInfo" enthält. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

