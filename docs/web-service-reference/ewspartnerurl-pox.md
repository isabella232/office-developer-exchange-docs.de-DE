---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: Das EwsPartnerUrl-Element gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an.
ms.openlocfilehash: 88ee0abdc5b8db09a938fc5fdba717a166b42399
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524322"
---
# <a name="ewspartnerurl-pox"></a>EwsPartnerUrl (POX)

Das **EwsPartnerUrl-Element** gibt die URL der besten Endpunktinstanz für Exchange Webdienste (EWS) für einen E-Mail-aktivierten Benutzer an. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EwsPartnerUrl (POX)](ewspartnerurl-pox.md)
  
```XML
<EwsPartnerUrl/>
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

Der Textwert stellt die URL des EWS-Endpunkts für den Benutzer dar.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **EwsPartnerUrl-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** Es entspricht dem [POX-Element (EwsUrl).](ewsurl-pox.md) 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

