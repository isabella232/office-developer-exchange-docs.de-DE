---
title: Perioden
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: Perioden-Element stellt ein Array von Zeiträumen, mit die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definiert.
ms.openlocfilehash: f2f9cf7c724b453d2b1975fcf72c55bc02caa54b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830729"
---
# <a name="periods"></a>Perioden

**Perioden** -Element stellt ein Array von Zeiträumen, mit die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definiert. 
  
```xml
<Periods>
   <Period/>
</Periods>
```

 **NonEmptyArrayOfPeriodsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Period](period.md) <br/> |Definiert die Namen sowie die Uhrzeitoffset und eindeutiger Bezeichner für eine bestimmte Phase der Zeitzone.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTimeZone-Zeitzone](starttimezone.md) <br/> |Definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).  <br/> |
|[Zeitzonendefinition](timezonedefinition.md) <br/> |Definiert eine Zeitzone.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

