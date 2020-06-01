---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: Das PreviousWatermark-Element stellt das Wasserzeichen des letzten Ereignisses dar, das erfolgreich an den Client für das Abonnement kommuniziert wurde.
ms.openlocfilehash: 1b26a645a5ec6dbbd2874b118f968866aadc32af
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461653"
---
# <a name="previouswatermark"></a>PreviousWatermark

Das **PreviousWatermark** -Element stellt das Wasserzeichen des letzten Ereignisses dar, das erfolgreich an den Client für das Abonnement kommuniziert wurde. 
  
```xml
<PreviousWatermark/>
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
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Wert Text stellt das neueste Wasserzeichen dar. Der Textwert darf keine leere Zeichenfolge sein.
  
## <a name="remarks"></a>Bemerkungen

Die **PreviousWatermark** -Eigenschaft ist hilfreich für den Client beim Bestimmen der letzten erfolgreichen Benachrichtigung. Wenn ein Abonnement beispielsweise drei Ereignisse mit Wasserzeichen 1, 2 und 3 aufweist und die nächste Benachrichtigung mit dem **PreviousWatermark** -Wert 3 gesendet wird, kann der Client diesen Wert mit dem Wasserzeichen Wert der letzten empfangenen Benachrichtigung vergleichen. Auf diese Weise kann der Client die Kontinuität von Ereignissen sicherstellen. 
  
Bei Push-Clients wird das **PreviousWatermark** mit dem lokalen, clientseitigen letzten bekannten Wasserzeichen verglichen. Wenn die Werte unterschiedlich sind, hat der Client eine Ereignisbenachrichtigung verpasst und sollte ein Abonnement mit dem neuesten lokalen Wasserzeichen wiederherstellen. Wenn beispielsweise ein Push-Client drei Ereignisse für ein Abonnement mit Wasserzeichen 1, 2 und 3 erhält und die nächste Benachrichtigung mit einem **PreviousWatermark** -Wert von 5 geliefert wird, hat der Client mindestens eine Benachrichtigung verpasst und sollte ein neues Abonnement erstellen, wobei ein 3 als Wasserzeichen übergeben wird. 
  
Im Fall eines Pull-Clients ist der Wert von **PreviousWatermark** identisch mit dem [Wasserzeichen](watermark.md) , das vom Client im GetEvents-Aufruf enthalten ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

