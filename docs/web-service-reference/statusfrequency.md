---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: Das StatusFrequency-Element stellt den Timeoutwert maximale in Minuten ein, in denen Wiederholungsversuche vom Server versucht werden.
ms.openlocfilehash: 402f8978c0ec6b377dfa020f23595c8954509a07
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831589"
---
# <a name="statusfrequency"></a>StatusFrequency

Das **StatusFrequency** -Element stellt den Timeoutwert maximale in Minuten ein, in denen Wiederholungsversuche vom Server versucht werden. 
  
[Abonnieren](subscribe.md)
  
[PushSubscriptionRequest](pushsubscriptionrequest.md)
  
[StatusFrequency](statusfrequency.md)
  
```XML
<StatusFrequency/>
```

 **SubscriptionStatusFrequencyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Benachrichtigungsabonnement Push-Ereignis.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird. Die möglichen Werte für dieses Element sind 1 bis 1440, inklusive. Dieses Element ist optional. Der Standardwert ist 30 Minuten.
  
## <a name="remarks"></a>Hinweise

Der Wert **StatusFrequency** wird vom Server verwendet, eine Push-Benachrichtigung zu wiederholen, wenn eine Antwort auf eine Push-Benachrichtigung oder Status Ping vom Client nicht empfangen wird. Wenn der Server keine Antwort erhalten, versucht er senden die Benachrichtigung mehrmals, bevor es beendet, das die Benachrichtigung gesendet. In der Exchange-Webdienste das Standard-Wiederholungsintervall beträgt 30 Sekunden und nachfolgende Wiederholungsversuche sind immer double der Zeitpunkt der letzten Wiederholungsintervall. Wie oft wiederholen sind nicht genau, wie sie andere Lasten auf dem Server aufgrund von verzögert werden können. In der folgenden Tabelle veranschaulicht, wie die Wiederholungsversuchen treten in der 30 Minuten Projektzuordnungstermin vom **StatusFrequency** Standardwert (vorausgesetzt, dass der Server keine Verzögerungen auftreten). 
  
|**Wiederholen**|**Sekunden**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |Ersten Synchronisierung  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4  <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6  <br/> |960  <br/> |16:00 Uhr  <br/> |
|7  <br/> |1920  <br/> |32:00 - **StatusFrequency** Standardwert 30 überschritten, wiederholen Sie den Vorgang nicht gesendet  <br/> |
   
Erhält der Client keine Benachrichtigungsnachrichten vom Server für eine bestimmte Zeitspanne, die zweimal die Zeit, die durch **StatusFrequency**angegebenen überschreitet, sollte der Client eine Aktion wie das Abonnement Neuerstellen verwenden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
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
  
[Wasserzeichen](watermark.md)

