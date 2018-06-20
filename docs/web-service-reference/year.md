---
title: Jahr
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Year
api_type:
- schema
ms.assetid: 93bf2847-53fa-496c-9a1e-dc9a9ffd0b9f
description: Das Jahr-Element wird verwendet, um eine Zeitzone definiert, die sich je nach dem Jahr ändern. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.
ms.openlocfilehash: 95d75f9c6166fc26e86534346fb07292a7fb3dcd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839565"
---
# <a name="year"></a>Jahr

Das **Jahr** -Element wird verwendet, um eine Zeitzone definiert, die sich je nach dem Jahr ändern. Dieses Element ist optional. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt. 
  
```xml
<Year/>
```

**string**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StandardTime](standardtime.md) <br/> |Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird.  <br/> |
|[DaylightTime](daylighttime.md) <br/> |Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element Regionen dargestellt wird, in dem Sommerzeit beobachtet wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Das Jahr-Element akzeptiert eine Zeichenfolge, die ein Jahr darstellt. Das Jahresformat ist YYYY.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

