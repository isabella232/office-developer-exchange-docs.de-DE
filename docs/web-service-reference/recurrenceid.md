---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: Das RecurrenceId-Element wird verwendet, um eine bestimmte Instanz eines Wiederkehrenden Kalenderelements zu identifizieren.
ms.openlocfilehash: 863673f7439c12ce4c74e8e0ef4ddea996fb4eb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59527564"
---
# <a name="recurrenceid"></a>RecurrenceId

Das **RecurrenceId-Element** wird verwendet, um eine bestimmte Instanz eines Wiederkehrenden Kalenderelements zu identifizieren. 
  
```xml
<RecurrenceId/>
```

 **dateTime**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechungsnachricht dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanfrage dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt einen Datums-/Uhrzeitwert dar, der ein Kalendervorkommen identifiziert.
  
## <a name="remarks"></a>HinwBemerkungeneise

Diese Eigenschaft wird mit der [UID-Eigenschaft](uid.md) verwendet, um eine bestimmte Instanz eines Terminserienkalenderelements zu identifizieren. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

