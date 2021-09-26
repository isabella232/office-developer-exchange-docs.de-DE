---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: Das StatusEvent-Element stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.
ms.openlocfilehash: 777d5cd22e47fea6e7bf7432e58e5d58d1ef67a4
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543975"
---
# <a name="statusevent"></a>StatusEvent

Das **StatusEvent-Element** stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist. 
  
```xml
<StatusEvent>
   <Watermark/>
</StatusEvent>
```

 **BaseNotificationEventType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Watermark](watermark.md) <br/> |Stellt das letzte gültige Wasserzeichen für ein Abonnement dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das **StatusEvent-Element** wird aus einem der folgenden Gründe in einer Benachrichtigung zurückgegeben: 
  
- Ein Pullclient gibt eine GetEvents-Anforderung für ein Abonnement aus, das keine Aktivität hat.
    
- Ein Pushclient hat keine Ereignisse in der Warteschlange, wenn [statusFrequency](statusfrequency.md) erreicht wurde. 
    
Das[StatusEvent-Wasserzeichen](watermark.md) wird von einer Clientanwendung auf die gleiche Weise wie die anderen Ereignistyp-Wasserzeichen verwendet.  Das Wasserzeichen für **StatusEvent** ist jedoch nicht identisch mit den Wasserzeichen, die für andere Ereignisse verwendet werden. Beispielsweise weist ein Abonnement Ereignisse mit den Wasserzeichen 1, 2 und 3 auf, und diese Ereignisse wurden in einer Benachrichtigung erfolgreich kommuniziert. Es tritt ein Zeitraum der Inaktivität auf, und eine **GetEvents-Anforderung** wird gesendet. Der Clientzugriffsserver (Client Access Server, CAS) gibt ein Statusereignis zurück und enthält das letzte Wasserzeichen, 3, sowohl als [Previous Cursormark](previouswatermark.md) als auch als [aktuelles Wasserzeichen.](watermark.md)
  
Das Wasserzeichen bleibt nicht in allen Fällen gleich. Ereigniseinträge werden 30 Tage lang verwaltet. Um ein aktives Abonnement zu verwalten, aktualisiert der CAS regelmäßig die Wasserzeichen für Abonnementwarteschlangen. Die aktualisierten Wasserzeichen werden an Clients gesendet, um ein aktives Abonnement zu verwalten.
  
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

