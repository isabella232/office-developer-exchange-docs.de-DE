---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: Das DeploymentId-Element wird die Microsoft Exchange Server 2007-Gesamtstruktur eindeutig identifiziert.
ms.openlocfilehash: 4f2548709753d8407d02218acecd9233f0ba764f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757953"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

Das **DeploymentId** -Element wird die Microsoft Exchange Server 2007-Gesamtstruktur eindeutig identifiziert. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)  
- [Response (POX)](response-pox.md) 
- [Benutzer (POX)](user-pox.md)  
- [DeploymentId (POX)](deploymentid-pox.md)
  
```xml
<DeploymentId/>
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
|[Benutzer (POX)](user-pox.md) <br/> |Benutzerspezifische Informationen enthält.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert identifiziert eindeutig die Exchange 2007-Gesamtstruktur im GUID-Format.
  
## <a name="remarks"></a>Hinweise

Wenn Sie deinstallieren und Neuinstallieren von Exchange 2007 und den gleichen Servernamen verwenden, ändert sich der **DeploymentId** -Wert. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

