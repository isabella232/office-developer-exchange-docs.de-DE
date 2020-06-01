---
title: ServerDN (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: 2ef73d13-e8bb-43f6-96c7-3ee157fed739
description: Das ServerDN-Element gibt den DN (Distinguished Name) des Computers an, auf dem Microsoft Exchange Server 2007 ausführt.
ms.openlocfilehash: 16c6e7368e221b7e54c8d7d63532bb29464a7e54
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461996"
---
# <a name="serverdn-pox"></a>ServerDN (POX)

Das **ServerDN** -Element gibt den DN (Distinguished Name) des Computers an, auf dem Microsoft Exchange Server 2007 ausführt. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[ServerDN (POX)](serverdn-pox.md)
  
```xml
<ServerDN/>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt den Distinguished Name des Exchange-Servers dar.
  
## <a name="remarks"></a>Bemerkungen

Der **ServerDN** -Wert wird nur verwendet, wenn [Type (POX)](type-pox.md) gleich dem-Typ ist. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

