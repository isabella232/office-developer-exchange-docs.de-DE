---
title: GroupingInformation (POX)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 2d8a007f-d79c-43c8-90e3-2c6d883f3a7c
description: Das GroupingInformation-Element enthält einen Wert, der verwendet wird, um das Postfach des Benutzers zu gruppieren, um die Affinität beizubehalten, wenn Benachrichtigungen über mehrere Postfächer abonniert werden.
ms.openlocfilehash: 7cab5d68f7dd5ec1f6caded5b9da6cfee03f3a67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530078"
---
# <a name="groupinginformation-pox"></a>GroupingInformation (POX)

Das **GroupingInformation** -Element enthält einen Wert, der verwendet wird, um das Postfach des Benutzers zu gruppieren, um die [Affinität beizubehalten](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx) , wenn Benachrichtigungen über mehrere Postfächer abonniert werden. 
  
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
|[Protokoll (POX)](protocol-pox.md) <br/> |Enthält die Spezifikationen für die Verbindung eines Clients mit dem Exchange-Server.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert wird mit dem Wert des **GroupingInformation** -Elements für andere Postfächer verglichen. Postfächer, die denselben Wert aufweisen und denselben Exchange-Webdienste-Endpunkt verwenden, können zusammen gruppiert werden, um die Affinität beizubehalten. Weitere Informationen finden Sie unter [MAINTAIN Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx).
  
## <a name="remarks"></a>Bemerkungen

Das **GroupingInformation** -Element gilt nur für **Protokoll** Elemente, die über ein untergeordnetes [Type (POX)-](type-pox.md) Element mit dem Wert "expr" verfügen. 
  
## <a name="see-also"></a>Siehe auch

- [POX Autodiscover XML-Elemente für Exchange](pox-autodiscover-xml-elements-for-exchange.md)
- [Verwalten von Affinität zwischen einer Gruppe von Abonnements und dem Postfachserver in Exchange](https://msdn.microsoft.com/library/1bda4094-88c3-4f61-9219-6ee70f6e81cf%28Office.15%29.aspx)

