---
title: EcpUrl-mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: Das EcpUrl-mt-Element gibt eine partielle URL an, die mit dem Wert des EcpUrl -Elements (POX) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf E-Mail-Nachrichtenverfolgungseinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann.
ms.openlocfilehash: bb0a60f3b3a2d65421164e40537e7514df20e357
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520815"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl-mt (POX)

Das **EcpUrl-mt-Element** gibt eine partielle URL an, die mit dem Wert des [EcpUrl -Elements (POX)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf E-Mail-Nachrichtenverfolgungseinstellungen für einen E-Mail-aktivierten Benutzer verwendet werden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EcpUrl-mt (POX)](ecpurl-mt-pox.md)
  
```XML
<EcpUrl-mt/>
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

Der Textwert stellt eine partielle URL dar, die mit dem Wert des [EcpUrl -Elements (POX)](ecpurl-pox.md) kombiniert werden kann, um eine URL zu generieren, die für den Zugriff auf E-Mail-Tracking-Einstellungen für den Benutzer verwendet werden kann. Der Wert des **EcpUrl-mt-Elements** enthält Parameter, die in den Zeichen "<" und ">" enthalten sind, die durch den Client ersetzt werden, wie in der folgenden Tabelle dargestellt. 
  
|**Parameter**|**Ersetzen durch**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _Msgid_ <br/> |Internetnachrichtenbezeichner der Nachricht, die nachverfolgt werden soll, wie im Nachrichten-ID-Header angegeben.  <br/> |
| _Mbx_ <br/> |Die SMTP-Adresse des Postfachbesitzers.  <br/> |
| _Sender_ <br/> |Die SMTP-Adresse des Absenders der Nachricht.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **EcpUrl-mt-Element** ist ein optionales untergeordnetes Element des **Protocol-Elements.** 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

