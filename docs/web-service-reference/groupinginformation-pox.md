---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: Das GroupingInformation-Element enthält einen Wert, der zum Gruppieren des Postfachs des Benutzers verwendet wird, um die Affinität beizubehalten, wenn Benachrichtigungen über mehrere Postfächer hinweg abonniert werden.
ms.openlocfilehash: 14e751adcd0b966907ce495a2753b2b26d812a86
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525884"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

Das **GroupingInformation-Element** enthält einen Wert, der zum Gruppieren des Postfachs des Benutzers verwendet wird, um die [Affinität](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) beizubehalten, wenn Benachrichtigungen über mehrere Postfächer hinweg abonniert werden. 
  
[AutoErmittlung (POX)](autodiscover-pox.md)
  
[Response (POX)](response-pox.md)
  
[Konto (POX)](account-pox.md)
  
[Protokoll (POX)](protocol-pox.md)
  
[GroupingInformation (POX)](groupinginformation-pox.md)
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen zum Verbinden eines Clients mit dem Exchange Server.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert wird mit dem Wert des **GroupingInformation-Elements** für andere Postfächer verglichen. Postfächer, die denselben Wert haben und den gleichen Exchange Webdienstendpunkt (EWS) verwenden, können gruppiert werden, um die Affinität aufrechtzuerhalten. Weitere Informationen finden Sie unter [Verwalten der Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange.](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **GroupingInformation-Element** gilt nur für **Protokollelemente,** die ein untergeordnetes [Type (POX)-Element](type-pox.md) mit dem Wert "EXPR" aufweisen. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

