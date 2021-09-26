---
title: EcpUrl-extinstall (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: Das EcpUrl-extinstall-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl -Elements (POX) kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der derzeit im Postfach des Benutzers installierten Mail-Apps verwendet werden kann.
ms.openlocfilehash: bf91b12cbcff3b08b3b13569eac9c957dea12757
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59541420"
---
# <a name="ecpurl-extinstall-pox"></a>EcpUrl-extinstall (POX)

Das **EcpUrl-extinstall-Element** gibt eine partielle URL an, die mit dem Wert des [EcpUrl -Elements (POX)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der derzeit im Postfach des Benutzers installierten Mail-Apps verwendet werden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EcpUrl-extinstall (POX)](ecpurl-extinstall-pox.md)
  
```XML
<EcpUrl-extinstall/>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine partielle URL dar, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der derzeit im Postfach des Benutzers installierten Mail-Apps verwendet werden kann. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **EcpUrl-extinstall-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

