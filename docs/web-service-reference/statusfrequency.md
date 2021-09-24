---
title: StatusFrequency
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- StatusFrequency
api_type:
- schema
ms.assetid: 917474e2-a426-4166-b825-53783a41dad4
description: Das StatusFrequency-Element stellt den maximalen Timeoutwert in Minuten dar, in dem versucht wird, wiederholungsversuche vom Server durchzuführen.
ms.openlocfilehash: f0359bab58167bbe7be5cce8c250240bebc7cc08
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59525533"
---
# <a name="statusfrequency"></a>StatusFrequency

Das **StatusFrequency-Element** stellt den maximalen Timeoutwert in Minuten dar, in dem versucht wird, wiederholungsversuche vom Server durchzuführen. 
  
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
|[PushSubscriptionRequest](pushsubscriptionrequest.md) <br/> |Stellt ein Abonnement für ein Push-basiertes Ereignisbenachrichtigungsabonnement dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine ganze Zahl darstellt, ist erforderlich, wenn dieses Element verwendet wird. Die möglichen Werte für dieses Element sind 1 bis einschließlich 1440. Dieses Element ist optional. Der Standardwert beträgt 30 Minuten.
  
## <a name="remarks"></a>HinwBemerkungeneise

Der **StatusFrequency-Wert** wird vom Server verwendet, um eine Pushbenachrichtigung zu wiederholen, wenn er keine Antwort auf eine Pushbenachrichtigung oder einen Status-Ping vom Client empfängt. Wenn der Server keine Antwort empfängt, versucht er mehrmals, die Benachrichtigung zu senden, bevor das Senden der Benachrichtigung beendet wird. In EWS beträgt das Standardmäßige Wiederholungsintervall 30 Sekunden, und nachfolgende Wiederholungsversuche sind immer doppelt so lang wie die Zeit des letzten Wiederholungsintervalls. Wiederholungszeiten sind nicht exakt, da sie aufgrund anderer Lasten auf dem Server verzögert werden können. Die folgende Tabelle zeigt, wie die Wiederholungsintervalle in den 30 Minuten auftreten, die dem **Standardmäßigen StatusFrequency-Wert** zugewiesen sind (vorausgesetzt, der Server hat keine Verzögerungen festgestellt). 
  
|**Wiederholen**|**Sekunden**|**Time**|
|:-----|:-----|:-----|
|0  <br/> |0  <br/> |Anfängliche Synchronisierung  <br/> |
|1  <br/> |30  <br/> |00:30  <br/> |
|2  <br/> |60  <br/> |01:00  <br/> |
|3  <br/> |120  <br/> |02:00  <br/> |
|4   <br/> |240  <br/> |04:00  <br/> |
|5  <br/> |480  <br/> |08:00  <br/> |
|6   <br/> |960  <br/> |16:00  <br/> |
|7   <br/> |1920  <br/> |32:00 - **StatusFrequency-Standardwert** von 30 überschritten, wiederholungsgeschützt  <br/> |
   
Wenn der Client für einen Zeitraum, der die von **StatusFrequency** angegebene Zeit überschreitet, keine Benachrichtigungen vom Server empfängt, sollte der Client eine Aktion wie das Erneute Erstellen des Abonnements ausführen. 
  
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

