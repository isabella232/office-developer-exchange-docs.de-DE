---
title: Server (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 0ce51644-7f3a-408c-a398-814439b658dc
description: Das Server-Element gibt den Namen des e-Mail-Servers.
ms.openlocfilehash: fafd6684d0857bd8b7e1bac0aae0ed162a6a938a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831369"
---
# <a name="server-pox"></a>Server (POX)

Das **Server** -Element gibt den Namen des e-Mail-Servers. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Server (POX)](server-pox.md)
  
```xml
<Server/>
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

Der Textwert identifiziert der Server. Für die Protokolle wie POP3, SMTP, IMAP oder NNTP wird dieser Wert einen Hostnamen oder eine IP-Adresse sein. Für die Protokolle wie DAV oder WEB wird dies eine URL sein.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

