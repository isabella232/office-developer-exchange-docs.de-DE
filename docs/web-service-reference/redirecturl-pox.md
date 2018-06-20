---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: Das RedirectUrl-Element enthält die URL der Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist, die zum Abrufen der für die AutoErmittlung verwendet werden soll.
ms.openlocfilehash: 3b634f1a3a3d44b6aae1a826a005149200641dcb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831027"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

Das **RedirectUrl** -Element enthält die URL der Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, dem die Clientzugriffs-Serverrolle installiert ist, die zum Abrufen der für die AutoErmittlung verwendet werden soll. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[RedirectUrl (POX)](redirecturl-pox.md)
  
```xml
<RedirectUrl/>
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
|[Konto (POX)](account-pox.md) <br/> |Gibt die kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die URL des Clientzugriffsservers, die zum Abrufen der für die AutoErmittlung verwendet werden soll.
  
## <a name="remarks"></a>Hinweise

Die Clientanwendung sollte beenden umleiten nach 10 umleitungen zulässig.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

