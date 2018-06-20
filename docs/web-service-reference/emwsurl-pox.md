---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: Das EmwsUrl-Element gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer.
ms.openlocfilehash: d8905d098c9978c3413f67e9a1b2443a52fb0d1f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758212"
---
# <a name="emwsurl-pox"></a>EmwsUrl (POX)

Das **EmwsUrl** -Element gibt die URL der besten Endpunktinstanz für die Exchange-Webdienste (EWS) für einen e-Mail-aktivierten Benutzer. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die URL des EWS-Endpunkts für den Benutzer. Dies entspricht dem Element ["Ewsurl" (POX)](ewsurl-pox.md) . 
  
## <a name="remarks"></a>Hinweise

Das **EmwsUrl** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

