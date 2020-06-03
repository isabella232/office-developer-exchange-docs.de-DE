---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: Das Wasserzeichen-Element stellt eine Ereignis Textmarke in der Post Fach Ereigniswarteschlange dar.
ms.openlocfilehash: a717196101fea698b0b8c66f92a3d420fda9a421
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459763"
---
# <a name="watermark"></a>Watermark

Das **Wasserzeichen** -Element stellt eine Ereignis Textmarke in der Post Fach Ereigniswarteschlange dar. 
  
```xml
<Watermark/>
```

 **Watermarktype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Pull-basiertes Ereignis Benachrichtigungsabonnement dar.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.  <br/> |
|[GetEvents](getevents.md) <br/> |Stellt den Vorgang dar, der von Pull-Clients zum Anfordern von Benachrichtigungen vom Server verwendet wird.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder ein Ordner gelöscht wird.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis dar, in dem ein Element oder ein Ordner geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder ein Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis dar, das durch ein neues e-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer subscribe-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Je nachdem, wie dieses Element verwendet wird, ist möglicherweise ein Textwert erforderlich oder optional.
  
## <a name="remarks"></a>Bemerkungen

Wenn eine subscribe-Anforderung ein Wasserzeichen enthält, wird das Abonnement aus dem Wasserzeichen vorwärts erstellt. Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, das in der Tabelle Post Fach Ereignisse nicht gefunden wird, `ErrorInvalidWatermark` wird ein Fehler an die Clientanwendung zurückgegeben. Dies kann vorkommen, wenn das Wasserzeichen zu alt ist und aus dem 30-Tage-Fenster der Ereignistabelle entfernt wurde oder wenn das Wasserzeichen in der Ereignistabelle nicht immer vorhanden war. Dies kann beispielsweise der Fall sein, wenn ein Wasserzeichen aus einem anderen Abonnement für ein Postfach in einer anderen Datenbank abgerufen wird. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

