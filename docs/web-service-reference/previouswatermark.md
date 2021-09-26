---
title: PreviousWatermark
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- PreviousWatermark
api_type:
- schema
ms.assetid: 474f4f7c-47da-47d4-8126-230012172fb5
description: Das PreviousDownmark-Element stellt das Wasserzeichen des neuesten Ereignisses dar, das dem Client für das Abonnement erfolgreich mitgeteilt wurde.
ms.openlocfilehash: c46e18c7a58405fe2149666531cb2af773110816
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543023"
---
# <a name="previouswatermark"></a>PreviousWatermark

Das **PreviousDownmark-Element** stellt das Wasserzeichen des neuesten Ereignisses dar, das dem Client für das Abonnement erfolgreich mitgeteilt wurde. 
  
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

Ein Textwert ist erforderlich. Der Textwert stellt das neueste Wasserzeichen dar. Der Textwert darf keine leere Zeichenfolge sein.
  
## <a name="remarks"></a>HinwBemerkungeneise

Die **PreviousColormark-Eigenschaft** ist für den Client nützlich, um die letzte erfolgreiche Benachrichtigung zu bestimmen. Wenn ein Abonnement beispielsweise drei Ereignisse mit den Wasserzeichen 1, 2 und 3 aufweist und die nächste Benachrichtigung mit dem **Wert "Previous Bytesmark"** von 3 gesendet wird, kann der Client diesen Wert mit dem Wasserzeichenwert der letzten empfangenen Benachrichtigung vergleichen. Dadurch kann der Client die Kontinuität von Ereignissen sicherstellen. 
  
Bei Pushclients wird **previous Ausweichmark** mit dem lokalen, clientseitigen letzten bekannten Wasserzeichen verglichen. Wenn die Werte unterschiedlich sind, hat der Client eine Ereignisbenachrichtigung verpasst und sollte ein Abonnement mithilfe des neuesten lokalen Wasserzeichens wiederherstellen. Wenn ein Pushclient z. B. drei Ereignisse für ein Abonnement mit den Wasserzeichen 1, 2 und 3 empfängt und die nächste Benachrichtigung den **Wert "PreviousNotmark"** von 5 aufweist, hat der Client mindestens eine Benachrichtigung verpasst und sollte ein neues Abonnement erstellen, wobei eine 3 als Wasserzeichen übergeben wird. 
  
Im Fall eines Pullclients ist der Wert von **Previous Auswert** identisch mit dem [Wasserzeichen,](watermark.md) das vom Client im GetEvents-Aufruf enthalten ist. 
  
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

