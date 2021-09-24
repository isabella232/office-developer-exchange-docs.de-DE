---
title: GetStreamingEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetStreamingEvents
api_type:
- schema
ms.assetid: dbe83857-c4f8-4d98-813f-e03c289697a1
description: Das GetStreamingEvents-Element stellt den Vorgang dar, der von Clients zum Anfordern von Streamingbenachrichtigungen vom Server verwendet wird.
ms.openlocfilehash: 8a68b3edbb53b623e4dc709e0128c5b3ebc94f91
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59523052"
---
# <a name="getstreamingevents"></a>GetStreamingEvents

Das **GetStreamingEvents-Element** stellt den Vorgang dar, der von Clients zum Anfordern von Streamingbenachrichtigungen vom Server verwendet wird. 
  
[GetStreamingEvents](getstreamingevents.md)
  
```XML
<GetStreamingEvents>
   <SubscriptionId/>
   <ConnectionTimeout/>
</GetStreamingEvents>
```

 **GetStreamingEventsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SubscriptionId (GetStreamingEvents)](subscriptionid-getstreamingevents.md) <br/> |Stellt den Bezeichner für ein Abonnement dar, das nach Ereignissen abgefragt wird.  <br/> |
|[ConnectionTimeout](connectiontimeout.md) <br/> |Stellt die Anzahl der Minuten dar, um eine Verbindung geöffnet zu lassen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

