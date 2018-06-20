---
title: Wasserzeichen
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
description: Das Wasserzeichen-Element stellt ein Lesezeichen Ereignis in der Ereigniswarteschlange Postfach.
ms.openlocfilehash: 1867aa781bc24f5eb3bdb4648fa494a2a7ea396a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839511"
---
# <a name="watermark"></a>Wasserzeichen

Das **Wasserzeichen** -Element stellt ein Lesezeichen Ereignis in der Ereigniswarteschlange Postfach. 
  
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
|[PullSubscriptionRequest](pullsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Benachrichtigungsabonnement Pull-Ereignis.  <br/> |
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.  <br/> |
|[GetEvents](getevents.md) <br/> |Stellt die Operation auf Anforderung-Benachrichtigungen vom Server von Pull-Clients verwendet wird.  <br/> |
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis eines Elements oder Ordners, in dem kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis eines Elements oder Ordners, in dem erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis, bei denen eines Elements oder Ordners gelöscht wird.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis, bei denen eines Elements oder Ordners geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis, auf dem eines Elements oder Ordners aus einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis ausgelöst, indem eine neue e-Mail-Element in einem Postfach an.  <br/> |
|[StatusEvent](statusevent.md) <br/> |Stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.  <br/> |
|[SubscribeResponseMessage](subscriberesponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer Subscribe-Anforderung.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert möglicherweise erforderlich oder optional je nach dieses Elements Verwendung.
  
## <a name="remarks"></a>Hinweise

Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, wird das Abonnement aus der Wasserzeichen vorwärts erstellt. Wenn die Subscribe-Anforderung ein Wasserzeichen enthält, die in der Tabelle Ereignisse Postfach nicht gefunden werden kann ein `ErrorInvalidWatermark` Fehler an die Clientanwendung zurückgegeben. Dies kann auftreten, wenn das Wasserzeichen veraltet ist und wurde aus der Ereignistabelle das 30-Tage-Fenster entfernt oder wenn das Wasserzeichen jemals nicht wurde in der Ereignistabelle. Dies kann beispielsweise auftreten, wenn ein Wasserzeichen aus ein anderes Abonnement für ein Postfach in einer anderen Datenbank abgerufen wird. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

