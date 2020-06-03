---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: Das EmwsUrl-Element gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.
ms.openlocfilehash: 19e1078ae8d08513e85d75d87e960a910986f727
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530670"
---
# <a name="emwsurl-pox"></a>EmwsUrl (POX)

Das **EmwsUrl** -Element gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md) 
- [Response (POX)](response-pox.md) 
- [Konto (POX)](account-pox.md) 
- [Protokoll (POX)](protocol-pox.md) 
- [EmwsUrl (POX)](emwsurl-pox.md)
  
```XML
<EmwsUrl/>
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

Der Wert Text stellt die URL des EWS-Endpunkts für den Benutzer dar. Es entspricht dem [EwsUrl (POX)-](ewsurl-pox.md) Element. 
  
## <a name="remarks"></a>Bemerkungen

Das **EmwsUrl** -Element ist ein optionales untergeordnetes Element des **Protocol** -Elements. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

