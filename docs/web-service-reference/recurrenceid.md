---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: Das Element RecurrenceId wird verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.
ms.openlocfilehash: 078bec85e1ca1530137f9935365d7dd3e530ea34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831005"
---
# <a name="recurrenceid"></a>RecurrenceId

Das Element **RecurrenceId** wird verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren. 
  
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
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanfrage an.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Antwort auf Besprechungsanfrage.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Einen Besprechungsabsage darstellt.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt einen Datum/Uhrzeit-Wert, der ein Kalender Vorkommen identifiziert.
  
## <a name="remarks"></a>Hinweise

Diese Eigenschaft wird mit der [UID](uid.md) -Eigenschaft verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

