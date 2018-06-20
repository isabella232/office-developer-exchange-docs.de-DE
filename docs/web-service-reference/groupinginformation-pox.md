---
title: Werten "groupinginformation" (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: Das Werten "groupinginformation"-Element enthält einen Wert, der das Postfach des Benutzers zum Affinität verwalten, wenn Sie über mehrere Postfächer auf Benachrichtigungen abonnieren gruppiert verwendet wird.
ms.openlocfilehash: bcde002c794ac79d9515befc0755c1f954ee8706
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829781"
---
# <a name="groupinginformation-pox"></a>Werten "groupinginformation" (POX)

Das **Werten "groupinginformation"** -Element enthält einen Wert, der verwendet wird, um das Postfach des Benutzers zum [Aufrechterhalten der Affinität](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) beim Abonnieren von Benachrichtigungen über mehrere Postfächer zu gruppieren. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[Werten "groupinginformation" (POX)](groupinginformation-pox.md)
  
```XML
<GroupingInformation/>
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert wird auf den Wert des Elements für andere Postfächer **Werten "groupinginformation"** verglichen. Postfächer, die den gleichen Wert und verwenden den gleichen Exchange-Webdienste (EWS) Endpunkt können gruppiert werden, um die Affinität verwalten. Weitere Informationen finden Sie unter [Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange verwalten](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).
  
## <a name="remarks"></a>Hinweise

Das Element **Werten "groupinginformation"** gilt nur für **Protokoll** -Elemente, die ein untergeordnetes Element [Typ (POX)](type-pox.md) , mit dem Wert "AUSDR" aufweisen. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](http://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

