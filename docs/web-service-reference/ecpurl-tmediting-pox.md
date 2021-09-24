---
title: EcpUrl-tmEditing (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 1fbc2ea9-3f94-441b-ab42-647326bf0021
description: Das EcpUrl-tmEditing-Element gibt eine partielle URL an, die mit dem PoX-Wert (EcpUrl) kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen Websitepostfachs verwendet werden kann.
ms.openlocfilehash: e615e8ae09c3a9422f753a71070917a41f40741b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531092"
---
# <a name="ecpurl-tmediting-pox"></a>EcpUrl-tmEditing (POX)

Das **EcpUrl-tmEditing-Element** gibt eine partielle URL an, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen Websitepostfachs verwendet werden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EcpUrl-tmEditing (POX)](ecpurl-tmediting-pox.md)
  
```XML
<EcpUrl-tmEditing/>
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

Der Textwert stellt eine partielle URL dar, die mit dem [PoX-Wert (EcpUrl)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die zum Bearbeiten eines vorhandenen Websitepostfachs verwendet werden kann. Der Wert des **EcpUrl-tmEditing-Elements** enthält Parameter, die in den Zeichen "<" und ">" enthalten sind, die durch den Client ersetzt werden, wie in der folgenden Tabelle dargestellt. 
  
|**Parameter**|**Ersetzen durch**|
|:-----|:-----|
| _ID_ <br/> |Die SMTP-E-Mail-Adresse oder der X500-Distinguished Name des Websitepostfachs.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **EcpUrl-tmEditing-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

