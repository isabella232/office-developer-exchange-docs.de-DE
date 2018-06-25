---
title: StatusEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusEvent
api_type:
- schema
ms.assetid: d3901818-2640-4bed-aad8-21a61aee62a1
description: Das Element StatusEvent stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist.
ms.openlocfilehash: e214918f9795e9e29061d4aac72ab144d2b24267
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831592"
---
# <a name="statusevent"></a>StatusEvent

Das Element **StatusEvent** stellt eine Benachrichtigung, dass keine neue Aktivität im Postfach aufgetreten ist. 
  
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
|[Wasserzeichen](watermark.md) <br/> |Stellt das letzte gültige Wasserzeichen für ein Abonnement.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das **StatusEvent** -Element wird in einer Benachrichtigung für einen der folgenden Gründe zurückgegeben: 
  
- Ein Pull-Client sendet eine Anforderung GetEvents auf einem Abonnement, das keine Aktivität verfügt.
    
- Ein Push-Client hat keine Ereignisse in der Warteschlange, wenn die [StatusFrequency](statusfrequency.md) erreicht wurde. 
    
Das **StatusEvent**[Wasserzeichen](watermark.md) wird von einer Clientanwendung in die gleiche Weise wie das Ereignis Typ Wasserzeichen verwendet. Das Wasserzeichen für die **StatusEvent** ist jedoch nicht identisch mit der Wasserzeichen für andere Ereignisse verwendet. Angenommen, haben ein Abonnement von Ereignissen mit Wasserzeichen 1 aufweist, 2 und 3 und die Ereignisse, die erfolgreich in einer Benachrichtigung mitgeteilt wurden. Tritt auf ein Zeitraum der Inaktivität, und eine Anforderung **GetEvents** gesendet. Der Clientzugriffsserver (CAS) liefert ein Statusereignis und das letzte Wasserzeichen, 3, als die [PreviousWatermark](previouswatermark.md) und das aktuelle [Wasserzeichen](watermark.md).
  
Das Wasserzeichen wird nicht in allen Fällen unverändert. Einträge werden für 30 Tage beibehalten. Um ein aktives Abonnement zu gewährleisten, aktualisiert die CAS in regelmäßigen Abständen die Wasserzeichen für Abonnementwarteschlangen. Die aktualisierten Wasserzeichen sind an Clients gesendet, um ein aktives Abonnement verwalten.
  
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

