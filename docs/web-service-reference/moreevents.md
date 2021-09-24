---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: Das MoreEvents-Element gibt an, ob mehr Ereignisse in der Warteschlange vorhanden sind, die an den Client übermittelt werden sollen.
ms.openlocfilehash: 7a19349e406a7e55e52c8a8cf0c3febba0a7301b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59521809"
---
# <a name="moreevents"></a>MoreEvents

Das **MoreEvents-Element** gibt an, ob mehr Ereignisse in der Warteschlange vorhanden sind, die an den Client übermittelt werden sollen. 
  
```xml
<MoreEvents/>
```

 **Boolescher Wert**
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

Der Textwert stellt einen booleschen Wert dar. Der Wert **"true"** gibt an, dass sich weitere Ereignisse in der Warteschlange befinden. Der Wert **"false"** gibt an, dass sich keine weiteren Ereignisse in der Warteschlange befinden. Diese Eigenschaft ist schreibgeschützt. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Bei Pullbenachrichtigungen gibt ein **wahrer** Wert in diesem Element dem Client an, dass eine andere GetEvents-Anforderung ausgegeben werden soll, um die verbleibenden Ereignisse abzurufen. Unter der Annahme, dass die Clientspezifikationen eine minimale Latenz für Ereignisbenachrichtigungen erfordern, sollten GetEvents-Anforderungen fortlaufend fortgesetzt werden, bis ein **falscher** **MoreEvents-Wert** zurückgegeben wird. 
  
Bei Pushbenachrichtigungen gibt ein **wahrer** Wert für **MoreEvents** dem Client an, dass eine weitere Benachrichtigungsanforderung an den Client gesendet wird, um die verbleibenden Ereignisse zu übermitteln. Ähnlich wie Pullbenachrichtigungen werden diese Nachverfolgungsanforderungen fortlaufend nacheinander fortgesetzt, bis die Ereigniswarteschlange auf dem Clientzugriffsserver leer ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
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

