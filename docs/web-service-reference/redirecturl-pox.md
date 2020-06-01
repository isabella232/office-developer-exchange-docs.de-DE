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
description: Das RedirectUrl-Element enthält die URL des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die zum Abrufen von AutoErmittlungseinstellungen verwendet werden sollte.
ms.openlocfilehash: 5400b1e7a4bb7ebebc58b6a0f1fc9bf37f5a2e22
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468089"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

Das **RedirectUrl** -Element enthält die URL des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist, die zum Abrufen von AutoErmittlungseinstellungen verwendet werden sollte. 
  
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
|[Konto (POX)](account-pox.md) <br/> |Gibt Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt die URL des Client Zugriffsservers dar, der zum Abrufen von AutoErmittlungseinstellungen verwendet werden soll.
  
## <a name="remarks"></a>Bemerkungen

Die Clientanwendung sollte die Umleitung nach 10 Umleitungen beenden.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

