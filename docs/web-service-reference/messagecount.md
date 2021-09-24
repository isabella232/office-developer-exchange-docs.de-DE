---
title: MessageCount
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MessageCount
api_type:
- schema
ms.assetid: 5efc5903-fcb3-44cf-aabb-b6912268df8e
description: Das MessageCount-Element enthält die Gesamtanzahl der Unterhaltungselemente im aktuellen Ordner.
ms.openlocfilehash: ef02d4e03136a4dead0be7e1d0fe95ff32a21e4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523958"
---
# <a name="messagecount"></a>MessageCount

Das **MessageCount-Element** enthält die Gesamtanzahl der Unterhaltungselemente im aktuellen Ordner. 
  
[FindConversationResponse](findconversationresponse.md)
  
[Conversations](conversations-ex15websvcsotherref.md)
  
[Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
[MessageCount](messagecount.md)
  
```XML
<MessageCount/>
```

 **xs:int**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Unterhaltung (ConversationType)](conversation-conversationtype.md) <br/> |Stellt eine einfache Unterhaltung dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert des **MessageCount-Elements** ist die Gesamtzahl der Unterhaltungselemente in einem Ordner. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[FindConversation Operation](findconversation-operation.md)
  
[ApplyConversationAction-Vorgang](applyconversationaction-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Conversations in EWS](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

