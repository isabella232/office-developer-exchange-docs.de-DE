---
title: EcpUrl-tmHiding (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 9b9ae15b-3ac1-45ac-85ba-38c7231fe508
description: Das EcpUrl-tmHiding-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl (POX)-Elements kombiniert werden kann, um eine URL zu generieren, die zum Aufheben des Abonnements des Benutzers von einem websitepostfach verwendet werden kann.
ms.openlocfilehash: 68b949db8b8d98caddbac3b9f96c5d5e55b104b7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463531"
---
# <a name="ecpurl-tmhiding-pox"></a>EcpUrl-tmHiding (POX)

Das **EcpUrl-tmHiding-** Element gibt eine partielle URL an, die mit dem Wert des [EcpUrl (POX)](ecpurl-pox.md) -Elements kombiniert werden kann, um eine URL zu generieren, die zum Aufheben des Abonnements des Benutzers von einem websitepostfach verwendet werden kann. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Exchange Server ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine partielle URL dar, die mit dem [EcpUrl (POX)](ecpurl-pox.md) -Elementwert kombiniert werden kann, um eine URL zu generieren, die zum Aufheben des Abonnements des Benutzers von einem websitepostfach verwendet werden kann. Der Wert des **EcpUrl-tmHiding-** Elements enthält Parameter, die in "<"-und ">"-Zeichen enthalten sind, die durch den Client ersetzt werden, wie in der folgenden Tabelle dargestellt. 
  
|**Parameter**|**Ersetzen durch**|
|:-----|:-----|
| _Id_ <br/> |Die SMTP-e-Mail-Adresse oder der Distinguished Name x500 des websitepostfachs.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das **EcpUrl-tmHiding-** Element ist ein optionales untergeordnetes Element des **Protocol** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

