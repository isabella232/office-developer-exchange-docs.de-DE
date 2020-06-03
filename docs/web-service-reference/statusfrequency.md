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
description: Das StatusFrequency-Element stellt den maximalen Timeoutwert in Minuten dar, in dem Wiederholungsversuche vom Server versucht werden.
ms.openlocfilehash: db14ecfd54584188b3da16bb369db6c8089c70f4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468243"
---
# <a name="statusfrequency"></a>StatusFrequency

Das **StatusFrequency** -Element stellt den maximalen Timeoutwert in Minuten dar, in dem Wiederholungsversuche vom Server versucht werden. 
  
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
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Push-basiertes Ereignis Benachrichtigungsabonnement dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird. Die möglichen Werte für dieses Element sind 1 bis 1440, einschließlich. Dieses Element ist optional. Der Standardwert beträgt 30 Minuten.
  
## <a name="remarks"></a>Bemerkungen

Der **StatusFrequency** -Wert wird vom Server verwendet, um eine Push-Benachrichtigung zu wiederholen, wenn keine Antwort auf eine Push-Benachrichtigung oder einen Status-Ping vom Client empfangen wird. Wenn der Server keine Antwort erhält, wird erneut versucht, die Benachrichtigung mehrmals zu senden, bevor das Senden der Benachrichtigung beendet wird. In EWS beträgt das Standardintervall für Wiederholungen 30 Sekunden, und nachfolgende Wiederholungsversuche sind immer doppelt so lang wie beim letzten Wiederholungsintervall. Wiederholungszeiten sind nicht exakt, da Sie aufgrund anderer Lasten auf dem Server verzögert werden können. In der folgenden Tabelle wird gezeigt, wie die Wiederholungsintervalle in den 30 Minuten auftreten, die dem Standardwert **StatusFrequency** zugewiesen wurden (vorausgesetzt, der Server hat keine Verzögerungen auftreten). 
  
|**Wiederholen**|**Sekunden**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |Erstsynchronisierung  <br/> |
|1   <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4   <br/> |240  <br/> |04:00  <br/> |
|5   <br/> |480  <br/> |08:00  <br/> |
|6   <br/> |960  <br/> |16:00  <br/> |
|7   <br/> |1920  <br/> |32:00- **StatusFrequency** Standardwert 30 überschritten, wiederholen nicht gesendet  <br/> |
   
Wenn der Client für einen Zeitraum, der das Doppelte der durch **StatusFrequency**angegebenen Zeitspanne überschreitet, keine Benachrichtigungen vom Server erhält, sollte der Client eine Aktion wie das erneute Erstellen des Abonnements durchführen. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
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
  
[Watermark](watermark.md)

