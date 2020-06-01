---
title: EcpUrl-extinstall (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: f81807e6-93de-4e47-afee-1e1ae6a85054
description: Das EcpUrl-extinstall-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der aktuell im Postfach des Benutzers installierten e-Mail-Apps verwendet werden kann.
ms.openlocfilehash: 889e0ca3bdcdce4b557fe066db2918fde4abaa9b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461303"
---
# <a name="ecpurl-extinstall-pox"></a>EcpUrl-extinstall (POX)

Das **EcpUrl-extinstall-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der aktuell im Postfach des Benutzers installierten e-Mail-Apps verwendet werden kann. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Anzeigen oder Ändern der aktuell im Postfach des Benutzers installierten e-Mail-Apps verwendet werden kann. 
  
## <a name="remarks"></a>Bemerkungen

Das **EcpUrl-extinstall-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

