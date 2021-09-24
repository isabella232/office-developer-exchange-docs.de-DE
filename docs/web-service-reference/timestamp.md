---
title: TimeStamp
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- TimeStamp
api_type:
- schema
ms.assetid: 5eae859a-5a74-4bf6-b196-d1b2fd38501a
description: Das Timestamp-Element stellt den Zeitstempel eines Postfachereignisses dar.
ms.openlocfilehash: 87264f25cb8902d7306e1c8c42bef600520175be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531375"
---
# <a name="timestamp"></a>TimeStamp

Das **Timestamp-Element** stellt den Zeitstempel eines Postfachereignisses dar. 
  
```xml
<TimeStamp/>
```

 **DateTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CopiedEvent](copiedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner kopiert wird.  <br/> |
|[CreatedEvent](createdevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner erstellt wird.  <br/> |
|[DeletedEvent](deletedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner gelöscht wird.  <br/> |
|[ModifiedEvent](modifiedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner geändert wird.  <br/> |
|[MovedEvent](movedevent.md) <br/> |Stellt ein Ereignis dar, bei dem ein Element oder Ordner von einem übergeordneten Ordner in einen anderen übergeordneten Ordner verschoben wird.  <br/> |
|[NewMailEvent](newmailevent.md) <br/> |Stellt ein Ereignis dar, das von einem neuen E-Mail-Element in einem Postfach ausgelöst wird.  <br/> |
   
## <a name="text-value"></a>Textwert

Diese Eigenschaft ist schreibgeschützt.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist in erster Linie für die Clientermittlung der Ereignishäufigkeit verfügbar. Dies ist in [StatusEvent](statusevent.md)nicht vorhanden.
  
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

