---
title: RedirectUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: c54f310f-8c99-4c37-8e73-ac87722b6229
description: Das RedirectUrl-Element enthält die URL des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist, die zum Abrufen von AutoErmittlungseinstellungen verwendet werden soll.
ms.openlocfilehash: d515f3f79f2370dc496614bab0a3f77300ad4e30
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513528"
---
# <a name="redirecturl-pox"></a>RedirectUrl (POX)

Das **RedirectUrl-Element** enthält die URL des Computers, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist, die zum Abrufen von AutoErmittlungseinstellungen verwendet werden soll. 
  
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
|[Konto (POX)](account-pox.md) <br/> |Gibt die Kontoeinstellungen für den Benutzer an.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die URL des Clientzugriffsservers dar, der zum Abrufen von AutoErmittlungseinstellungen verwendet werden soll.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die Clientanwendung sollte die Umleitung nach 10 Umleitungen beenden.
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

