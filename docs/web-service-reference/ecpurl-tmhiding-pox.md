---
title: EcpUrl-tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: Das EcpUrl-tmHiding-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl -Elements (POX) kombiniert werden kann, um eine URL zu generieren, die verwendet werden kann, um den Benutzer von einem Websitepostfach abzumelden.
ms.openlocfilehash: d8e8ced554b96f1a0cd554d3d601970d5f47019b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514733"
---
# <a name="ecpurl-tmhiding-pox"></a>EcpUrl-tmHiding (POX)

Das **EcpUrl-tmHiding-Element** gibt eine partielle URL an, die mit dem Wert des [EcpUrl -Elements (POX)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die verwendet werden kann, um den Benutzer von einem Websitepostfach abzumelden. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EcpUrl-tmHiding (POX)](ecpurl-tmhiding-pox.md)
  
```XML
<EcpUrl-tmHiding/>
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

Der Textwert stellt eine partielle URL dar, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die verwendet werden kann, um den Benutzer von einem Websitepostfach abzumelden. Der Wert des **EcpUrl-tmHiding-Elements** enthält Parameter, die in den Zeichen "<" und ">" enthalten sind, die vom Client ersetzt werden, wie in der folgenden Tabelle dargestellt. 
  
|**Parameter**|**Ersetzen durch**|
|:-----|:-----|
| _ID_ <br/> |Die SMTP-E-Mail-Adresse oder der X500-Distinguished Name des Websitepostfachs.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **EcpUrl-tmHiding-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

