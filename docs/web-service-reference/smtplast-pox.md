---
title: SMTPLast (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_type:
- schema
ms.assetid: f1aa8bd9-c6ac-41ac-8d2d-56fb20006005
description: Das SMTPLast-Element gibt an, ob für den Simple Mail Transfer Protocol (SMTP) Server die e-Mail-Nachrichten heruntergeladen werden müssen, bevor eine e-Mail mithilfe des SMTP-Servers gesendet wird.
ms.openlocfilehash: 7019da28ffa196a9abc8798aa75aff2756198da3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468432"
---
# <a name="smtplast-pox"></a>SMTPLast (POX)

Das **SMTPLast** -Element gibt an, ob für den Simple Mail Transfer Protocol (SMTP) Server die e-Mail-Nachrichten heruntergeladen werden müssen, bevor eine e-Mail mithilfe des SMTP-Servers gesendet wird. 
  
- [AutoErmittlung (POX)](autodiscover-pox.md)
  
- [Response (POX)](response-pox.md)
  
- [Konto (POX)](account-pox.md)
  
- [Protokoll (POX)](protocol-pox.md)
  
- [SMTPLast (POX)](smtplast-pox.md)
  
```xml
<SMTPLast>on or off</SMTPLast>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für das Verbinden eines Clients mit dem Computer, auf dem Microsoft Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffs-Server Rolle installiert ist.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Text-Wert gibt an, ob der SMTP-Server die e-Mail-Nachrichten heruntergeladen werden muss, bevor er e-Mails mithilfe des SMTP-Servers sendet. Die möglichen Werte sind **ein** -und **ausgeschaltet**. Der Standardwert ist **Off**.
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)

