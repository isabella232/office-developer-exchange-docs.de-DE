---
title: Benachrichtigung
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Notification
api_type:
- schema
ms.assetid: c9070936-0930-438e-839c-91127256a6c8
description: Das Element Benachrichtigung enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.
ms.openlocfilehash: a769d8988eb68d0fa0b02f3838cd891e714571b6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830547"
---
# <a name="notification"></a>Benachrichtigung

Das Element **Benachrichtigung** enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind. 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

 **NotificationType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SubscriptionId (GetEvents)](subscriptionid-getevents.md) <br/> |Stellt den Bezeichner für ein Abonnement.  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |Stellt das Wasserzeichen des letzten Ereignisses, die erfolgreich übermittelt wurde an den Client für das Abonnement.  <br/> |
|[MoreEvents](moreevents.md) <br/> |Gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners gelöscht wird.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis in der eines Elements oder Ordners von einem übergeordneten Ordner in einer anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis, das durch eine neue e-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |Stellt ein Ereignis in der Frei/Gebucht-Zeit eines Elements geändert hat.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetEvents Anforderung.  <br/> |
|[SendNotificationResponseMessage](sendnotificationresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer SendNotification Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[GetStreamingEvents-Vorgang](getstreamingevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

