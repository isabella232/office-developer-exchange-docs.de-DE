---
title: Wiederholungs-Nr
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
description: Das Serien-Element wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.
ms.openlocfilehash: 58a379f2cffa7ff37181e93ad1c45c9752e84f1d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461611"
---
# <a name="recurrenceid"></a>Wiederholungs-Nr

Das **Serien** -Element wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren. 
  
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
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt einen Besprechungs Abbruch dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Wert Text stellt einen Datum/Uhrzeit-Wert dar, der ein Kalender vorkommen identifiziert.
  
## <a name="remarks"></a>Bemerkungen

Diese Eigenschaft wird zusammen mit der [UID](uid.md) -Eigenschaft verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

