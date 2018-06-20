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
description: Das PreviousWatermark-Element darstellt, das Wasserzeichen des neuesten Ereignisses, das an den Client für das Abonnement erfolgreich übermittelt wurde.
ms.openlocfilehash: 93c6f90d0866ae13618391b8544ab593fe33922b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830886"
---
# <a name="previouswatermark"></a>PreviousWatermark

Das **PreviousWatermark** -Element darstellt, das Wasserzeichen des neuesten Ereignisses, das an den Client für das Abonnement erfolgreich übermittelt wurde. 
  
```xml
<PreviousWatermark/>
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
|[Benachrichtigung](notification-ex15websvcsotherref.md) <br/> |Enthält Informationen über das Abonnement und die Ereignisse, die seit der letzten Benachrichtigung aufgetreten sind.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich. Der Textwert stellt das neuesten Wasserzeichen. Der Textwert darf nicht auf eine leere Zeichenfolge sein.
  
## <a name="remarks"></a>Hinweise

Die **PreviousWatermark** -Eigenschaft ist hilfreich, den Client bei der Bestimmung der letzten erfolgreichen benachrichtigungs. Beispielsweise kann, wenn ein Abonnement verfügt über drei Ereignisse mit Wasserzeichen 1, 2 und 3, und die nächste Benachrichtigung mit dem Wert **PreviousWatermark** 3 gesendet wird, der Client dieser Wert auf den Wasserzeichen-Wert, der die letzte Benachrichtigung empfangen vergleichen. Dies ermöglicht dem Client um sicherzustellen, dass die Kontinuität von Ereignissen. 
  
Für Push-Clients wird der **PreviousWatermark** auf das lokale, mithilfe der clientseitigen letzte bekannte Wasserzeichen verglichen. Wenn die Werte unterschiedlich sind, wird der Client eine ereignisbenachrichtigung verpasst hat und sollte ein Abonnement mit den neuesten lokalen Wasserzeichen wiederherzustellen. Beispielsweise wenn ein Push-Client drei Ereignisse für ein Abonnement mit Wasserzeichen 1, 2 und 3 empfängt und die nächste Benachrichtigung mit dem Wert **PreviousWatermark** 5 stammen, der Client verpasst hat mindestens eine Benachrichtigung und sollten ein neues Abonnement erstellen, übergeben einen 3 das Wasserzeichen. 
  
Bei einem Pull-Client wird der Wert der **PreviousWatermark** der vom Client in den Anruf GetEvents enthalten [Wasserzeichen](watermark.md) identisch sein. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[Vorgang abonnieren](subscribe-operation.md)
  
[GetEvents-Vorgang](getevents-operation.md)
  
[Vorgang des Kündigens von Abonnements](unsubscribe-operation.md)

