---
title: DeploymentId (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_type:
- schema
ms.assetid: b879c134-307e-4645-bb53-55d8ba4fad9c
description: Das DeploymentId-Element identifiziert die Microsoft Exchange Server 2007-Gesamtstruktur eindeutig.
ms.openlocfilehash: 37d66eadb38f02e75a35d0516b36aff07dfdafa6
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545356"
---
# <a name="deploymentid-pox"></a>DeploymentId (POX)

Das **DeploymentId-Element** identifiziert die Microsoft Exchange Server 2007-Gesamtstruktur eindeutig. 
  
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
|[Benutzer (POX)](user-pox.md) <br/> |Stellt benutzerspezifische Informationen bereit.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert identifiziert die Exchange 2007-Gesamtstruktur eindeutig im GUID-Format.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn Sie Exchange 2007 deinstallieren und dann neu installieren und denselben Servernamen verwenden, ändert sich der **DeploymentId-Wert.** 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

