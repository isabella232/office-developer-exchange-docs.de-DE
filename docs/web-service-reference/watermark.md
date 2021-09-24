---
title: Watermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Watermark
api_type:
- schema
ms.assetid: e1545046-94f9-4ac7-af1c-ea81dfb6822c
description: Das Watermark-Element stellt eine Ereignislesemarke in der Postfachereigniswarteschlange dar.
ms.openlocfilehash: 959ae7369195a164d257b8805a8c985f1fdca53b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59524399"
---
# <a name="watermark"></a>Watermark

Das **Watermark-Element** stellt eine Ereignislesemarke in der Postfachereigniswarteschlange dar. 
  
```xml
<Watermark/>
```

 **WatermarkType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein pullbasiertes Ereignisbenachrichtigungsabonnement dar.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Push-basiertes Ereignisbenachrichtigungsabonnement dar.  <br/> |
|[GetEvents](getevents.md) <br/> |Stellt den Vorgang dar, der von Pullclients zum Anfordern von Benachrichtigungen vom Server verwendet wird.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner gelöscht wird.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis dar, das von einem neuen E-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Subscribe-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Je nachdem, wie dieses Element verwendet wird, kann ein Textwert erforderlich oder optional sein.
  
## <a name="remarks"></a>HinwBemerkungeneise

Wenn eine Subscribe-Anforderung ein Wasserzeichen enthält, wird das Abonnement anhand des Wasserzeichens vorwärts erstellt. Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, das in der Postfachereignistabelle nicht gefunden wird, wird ein  `ErrorInvalidWatermark` Fehler an die Clientanwendung zurückgegeben. Dies kann vorkommen, wenn das Wasserzeichen zu alt ist und aus dem 30-Tage-Fenster der Ereignistabelle entfernt wurde oder wenn das Wasserzeichen nie in der Ereignistabelle vorhanden war. Dies kann beispielsweise passieren, wenn ein Wasserzeichen aus einem anderen Abonnement für ein Postfach in einer anderen Datenbank abgerufen wird. 
  
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

