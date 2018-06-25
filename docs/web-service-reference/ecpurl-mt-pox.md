---
title: EcpUrl-Mt (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 5221745b-572c-44a5-afdb-41b58af44971
description: Das EcpUrl Mt-Element gibt eine partielle URL, die mit dem EcpUrl (POX) Elementwert generiert eine URL, die verwendet werden können, für den e-Mail-Nachricht Nachverfolgen der Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann.
ms.openlocfilehash: 13954a4dab8e81f4ba75b3578e6ba7f67f4b8b96
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758118"
---
# <a name="ecpurl-mt-pox"></a>EcpUrl-Mt (POX)

Das **EcpUrl Mt** -Element gibt eine partielle URL, die mit dem [EcpUrl (POX)](ecpurl-pox.md) Elementwert generiert eine URL, die verwendet werden können, für den e-Mail-Nachricht Nachverfolgen der Einstellungen für einen e-Mail-aktivierten Benutzer Zugriff auf kombiniert werden kann. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[EcpUrl-Mt (POX)](ecpurl-mt-pox.md)
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Computer, auf der Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt eine partielle URL, die kombiniert werden kann, mit der [EcpUrl (POX)](ecpurl-pox.md) Element Wert generiert eine URL, die Zugriff auf e-Mails Nachverfolgen der Einstellungen für den Benutzer verwendet werden können. Der Wert des Elements **EcpUrl Mt** enthält Parameter enthaltenen ' <' und ' >' Zeichen, die vom Client ersetzt werden, wie in der folgenden Tabelle dargestellt. 
  
|**Parameter**|**Ersetzen durch**|
|:-----|:-----|
| _IsOwa_ <br/> |n  <br/> |
| _MsgID_ <br/> |Internetnachricht-ID der Nachricht nachverfolgt werden durch die Kopfzeile Nachrichten-ID angegeben wird.  <br/> |
| _MBX_ <br/> |Die SMTP-Adresse des Postfachbesitzers.  <br/> |
| _Absender_ <br/> |Die SMTP-Adresse des Absenders der Nachricht.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **EcpUrl Mt** -Element ist ein optionales untergeordnetes Element des **Protokoll** -Elements. 
  
## <a name="see-also"></a>Siehe auch



[POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

