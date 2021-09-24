---
title: IsOnlineMeeting
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- IsOnlineMeeting
api_type:
- schema
ms.assetid: c29df676-0f3a-4694-a42f-522c6d16872f
description: Das IsOnlineMeeting-Element gibt an, ob die Besprechung online ist.
ms.openlocfilehash: 3521cf82f2b6b2b2514b82478fc4e1e5c6edb563
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514515"
---
# <a name="isonlinemeeting"></a>IsOnlineMeeting

Das **IsOnlineMeeting-Element** gibt an, ob die Besprechung online ist. 
  
```xml
<IsOnlineMeeting/>
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
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich, der einen booleschen Wert darstellt. Der Wert **"true"** gibt an, dass die Besprechung online ist. Der Wert **"false"** gibt an, dass die Besprechung nicht online ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Die IsOnlineMeeting-Eigenschaft ist schreibgeschützt für das Kalenderelement des Organisators. Sie ist schreibgeschützt für Besprechungsanfragen und die Kalenderelemente der Teilnehmer.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem MicrosoftExchange 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

