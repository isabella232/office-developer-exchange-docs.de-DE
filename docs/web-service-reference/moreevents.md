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
description: Das MoreEvents-Element gibt an, ob weitere Ereignisse in der Warteschlange vorhanden sind, die an den Client übermittelt werden sollen.
ms.openlocfilehash: fd12dd2e2e64ce1711e553ba5eb29bd0eb64c892
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462731"
---
# <a name="moreevents"></a>MoreEvents

Das **MoreEvents** -Element gibt an, ob weitere Ereignisse in der Warteschlange vorhanden sind, die an den Client übermittelt werden sollen. 
  
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

Der Wert Text stellt einen booleschen Wert dar. Der Wert **true** gibt an, dass sich weitere Ereignisse in der Warteschlange befinden. Der Wert **false** gibt an, dass sich keine weiteren Ereignisse in der Warteschlange befinden. Diese Eigenschaft ist schreibgeschützt. 
  
## <a name="remarks"></a>Bemerkungen

Im Fall von Pull-Benachrichtigungen gibt ein Wert **true** in diesem Element an den Client an, dass eine andere GetEvents-Anforderung ausgegeben werden soll, um die restlichen Ereignisse abzurufen. Unter der Voraussetzung, dass die Client Spezifikationen eine minimale Wartezeit für Ereignisbenachrichtigungen erfordern, sollten GetEvents-Anforderungen in einer kontinuierlichen Reihenfolge fortgesetzt werden, bis ein **falscher** **MoreEvents** -Wert zurückgegeben wird. 
  
Im Fall von Push-Benachrichtigungen gibt ein **echter** Wert für **MoreEvents** dem Client an, dass eine andere Benachrichtigungsanforderung an den Client gesendet wird, um die verbleibenden Ereignisse zuzustellen. Ähnlich wie Pull-Benachrichtigungen werden diese nachverfolgungsanforderungen in Folge fortgesetzt, bis die Ereigniswarteschlange auf dem Client Zugriffsserver leer ist. 
  
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

