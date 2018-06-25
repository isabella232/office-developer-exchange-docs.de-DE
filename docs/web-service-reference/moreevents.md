---
title: MoreEvents
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MoreEvents
api_type:
- schema
ms.assetid: 76a7ea58-a44f-49b8-baba-d21302d742ad
description: Das MoreEvents-Element gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden.
ms.openlocfilehash: cc3f7ed3b4b5f5ce27a9d45d508506bfa62e5086
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830489"
---
# <a name="moreevents"></a>MoreEvents

Das **MoreEvents** -Element gibt an, ob es sind mehr Ereignisse in der Warteschlange an den Client übermittelt werden. 
  
```xml
<MoreEvents/>
```

 **Boolean**
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

Der Textwert stellt einen Boolean-Wert. Der Wert **true** gibt an, dass mehr Ereignisse in der Warteschlange befinden. Der Wert **false** gibt an, dass keine weiteren Ereignisse in der Warteschlange befinden. Diese Eigenschaft ist schreibgeschützt. 
  
## <a name="remarks"></a>Hinweise

Im Fall von Pull-Benachrichtigungen gibt ein **true** -Wert in diesem Element an den Client, dass eine andere GetEvents Anforderung ausgegeben werden soll, wenn Sie die verbleibenden Ereignisse erhalten möchten. Unter der Annahme, dass die Client-Spezifikationen minimale Wartezeit für ereignisbenachrichtigungen benötigen, sollten GetEvents Anforderungen einer continuous nacheinander fortgesetzt, bis ein **false** **MoreEvents** Wert zurückgegeben wird. 
  
Im Fall von Pushbenachrichtigungen gibt der Wert **true** für **MoreEvents** an den Client, dass eine weitere Benachrichtigung-Anforderung an den Client gesendet wird die verbleibenden Ereignisse zu übermitteln. Ähnlich wie bei Pull Benachrichtigungen, werden diese weiteren Anforderungen kontinuierliche nacheinander fortgesetzt, bis die Ereigniswarteschlange auf dem Clientzugriffsserver leer ist. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
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

