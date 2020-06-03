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
description: Das Benachrichtigungs Element enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.
ms.openlocfilehash: c4a5206c14985ec46cf40162a9ce4eaec68242ff
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530387"
---
# <a name="notification"></a>Benachrichtigung

Das **Benachrichtigungs** Element enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind. 
  
```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CopiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <CreatedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <DeletedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <ModifiedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <MovedEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <NewMailEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <StatusEvent/>
</Notification>
```

```xml
<Notification>
   <SubscriptionId/>
   <PreviousWatermark/>
   <MoreEvents/>
   <FreeBusyChangedEvent/>
</Notification>
```

**NOTIFICATIONTYPE**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Abonnement-Nr (GetEvents)](subscriptionid-getevents.md) <br/> |Stellt den Bezeichner für ein Abonnement dar.  <br/> |
|[PreviousWatermark](previouswatermark.md) <br/> |Stellt das Wasserzeichen des letzten Ereignisses dar, das erfolgreich an den Client für das Abonnement kommuniziert wurde.  <br/> |
|[MoreEvents](moreevents.md) <br/> |Gibt an, ob weitere Ereignisse in der Warteschlange an den Client übermittelt werden sollen.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner gelöscht wird.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.  <br/> |
|[FreeBusyChangedEvent](freebusychangedevent.md) <br/> |Stellt ein Ereignis dar, in dem die Frei/Gebucht-Zeit eines Elements geändert wurde.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetEventsResponseMessage](geteventsresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen GetEvents-Anforderung.  <br/> |
|[Sendnotificationresponsemessage zurück](sendnotificationresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen SendNotification-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [Vorgang abonnieren](subscribe-operation.md) 
- [GetEvents-Vorgang](getevents-operation.md) 
- [GetStreamingEvents-Vorgang](getstreamingevents-operation.md) 
- [Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

