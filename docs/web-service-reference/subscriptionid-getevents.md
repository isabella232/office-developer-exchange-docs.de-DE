---
title: SubscriptionId (GetEvents)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- SubscriptionId
api_type:
- schema
ms.assetid: 77c0abab-69e8-428e-8c20-22258e4ef71b
description: Das SubscriptionId-Element stellt den Bezeichner für ein Abonnement dar.
ms.openlocfilehash: c24ae8dc61fa98716efc38d7a2500cab503760b2
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522586"
---
# <a name="subscriptionid-getevents"></a>SubscriptionId (GetEvents)

Das **SubscriptionId-Element** stellt den Bezeichner für ein Abonnement dar. 
  
```xml
<SubscriptionId/>
```

 **SubscriptionIdType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetEvents](getevents.md) <br/> |Stellt den Vorgang dar, der von Pullclients zum Anfordern von Benachrichtigungen vom Server verwendet wird.  <br/> |
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Subscribe-Anforderung.  <br/> |
|[Unsubscribe](unsubscribe.md) <br/> |Enthält die Eigenschaften, die zum Kündigen eines Abonnements verwendet werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert ist eine GUID.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die GUID, die den Abonnementbezeichner darstellt, wird vom Clientzugriffsserver generiert, wenn das Abonnement erstellt wird.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

