---
title: EmwsUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: cad0fa91-8d75-4dde-a484-518c837ae063
description: Das EmwsUrl-Element gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an.
ms.openlocfilehash: d46438f600e226bce95c5e479aca91bfa942535e
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59538175"
---
# <a name="emwsurl-pox"></a>EmwsUrl (POX)

Das **EmwsUrl-Element** gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt die URL des EWS-Endpunkts für den Benutzer dar. Es entspricht dem [POX-Element (EwsUrl).](ewsurl-pox.md) 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **EmwsUrl-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

