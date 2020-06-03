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
description: Das Bereitstellungs-Kennungs Element identifiziert die Microsoft Exchange Server 2007 Gesamtstruktur eindeutig.
ms.openlocfilehash: 4986a3404763e88fb3e84d52a5d30d54c810f93a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467921"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

Das **Bereitstellungs** -Kennungs Element identifiziert die Microsoft Exchange Server 2007 Gesamtstruktur eindeutig. 
  
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
|[Benutzer (POX)](user-pox.md) <br/> |Enthält benutzerspezifische Informationen.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert identifiziert die Exchange 2007 Gesamtstruktur im GUID-Format eindeutig.
  
## <a name="remarks"></a>Bemerkungen

Wenn Sie Exchange 2007 deinstallieren und anschließend neu installieren und denselben Servernamen verwenden, ändert sich der Wert der **Bereitstellungs** -Nr. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

