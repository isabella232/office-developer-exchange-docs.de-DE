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
description: Das StatusEvent-Element stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist.
ms.openlocfilehash: 8158a47937a810be2ea22346384b4e61da56ac48
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468257"
---
# <a name="statusevent"></a>StatusEvent

Das **StatusEvent** -Element stellt eine Benachrichtigung dar, dass keine neue Aktivität im Postfach aufgetreten ist. 
  
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
   
## <a name="remarks"></a>Bemerkungen

Das **StatusEvent** -Element wird aus einem der folgenden Gründe in einer Benachrichtigung zurückgegeben: 
  
- Ein Pull-Client gibt eine GetEvents-Anforderung für ein Abonnement aus, das über keine Aktivität verfügt.
    
- Ein Push-Client hat keine Ereignisse in der Warteschlange, wenn die [StatusFrequency](statusfrequency.md) erreicht wurde. 
    
Das **StatusEvent**-[Wasserzeichen](watermark.md) wird von einer Clientanwendung auf die gleiche Weise wie die anderen Wasserzeichen von Ereignistypen verwendet. Das Wasserzeichen für das **StatusEvent** ist jedoch nicht identisch mit den Wasserzeichen, die für andere Ereignisse verwendet werden. Beispielsweise hat ein Abonnement Ereignisse mit Wasserzeichen 1, 2 und 3, und diese Ereignisse wurden in einer Benachrichtigung erfolgreich kommuniziert. Ein Zeitraum der Inaktivität tritt auf, und es wird eine **GetEvents** -Anforderung gesendet. Der Client Zugriffsserver (CAS) gibt ein Status Ereignis zurück und enthält das letzte Wasserzeichen, 3, als [PreviousWatermark](previouswatermark.md) und das aktuelle [Wasserzeichen](watermark.md).
  
Das Wasserzeichen wird nicht in allen Fällen gleich bleiben. Ereigniseinträge werden für 30 Tage beibehalten. Um ein aktives Abonnement beizubehalten, werden die Wasserzeichen für Abonnement Warteschlangen von der Zertifizierungsstellen regelmäßig aktualisiert. Die aktualisierten Wasserzeichen werden an Clients gesendet, um ein aktives Abonnement beizubehalten.
  
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

