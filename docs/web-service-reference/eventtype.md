---
title: EventType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EventType
api_type:
- schema
ms.assetid: 04b70f9e-c226-4130-958e-0db0275cf58b
description: Das EventType-Element wird zum Erstellen eines Abonnements und zum Identifizieren eines Ereignistyps verwendet, der in einer Benachrichtigung gemeldet werden soll.
ms.openlocfilehash: 58c7ce571434b6fb8ac0b1dc2a3f8cd4fd56ff17
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526172"
---
# <a name="eventtype"></a>EventType

Das **eventType** -Element wird zum Erstellen eines Abonnements und zum Identifizieren eines Ereignistyps verwendet, der in einer Benachrichtigung gemeldet werden soll. 
  
```xml
<EventType/>
```

 **NotificationEventTypeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EventTypes](eventtypes.md) <br/> |Enthält eine Auflistung von Ereignis Benachrichtigungsereignis Typen, die zum Erstellen eines Abonnements verwendet werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Im Folgenden sind die möglichen Werte aufgeführt:
  
- CopiedEvent
    
- CreatedEvent
    
- DeletedEvent
    
- ModifiedEvent
    
- MovedEvent
    
- NewMailEvent
    
- FreeBusyChangedEvent
    
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

