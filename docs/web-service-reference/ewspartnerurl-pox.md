---
title: EwsPartnerUrl (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2ebae21c-3efa-4239-9b49-4a3a8871449b
description: Das EwsPartnerUrl-Element gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an.
ms.openlocfilehash: a67eb17bb3db67a922c53ba5e37900ee0a9b956b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526109"
---
# <a name="ewspartnerurl-pox"></a>EwsPartnerUrl (POX)

Das **EwsPartnerUrl** -Element gibt die URL der besten Endpunkt Instanz für Exchange-Webdienste für einen e-Mail-aktivierten Benutzer an. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt die URL des EWS-Endpunkts für den Benutzer dar.
  
## <a name="remarks"></a>Bemerkungen

Das **EwsPartnerUrl** -Element ist ein optionales untergeordnetes Element des **Protocol** -Elements. Es entspricht dem [EwsUrl (POX)-](ewsurl-pox.md) Element. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

