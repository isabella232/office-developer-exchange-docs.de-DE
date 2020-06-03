---
title: Zeiten
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
description: Das Periods-Element stellt ein Array von Punkten dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.
ms.openlocfilehash: 773457a6e4c0237eaeaf23109a7022427cc7dd0d
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467774"
---
# <a name="periods"></a>Zeiten

Das **Periods** -Element stellt ein Array von Punkten dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren. 
  
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
|[Period](period.md) <br/> |Definiert den Namen, den Zeit Offset und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |Definiert die Zeitzone für die Startzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Start Zeit.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Definiert die Zeitzone für die Endzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Datei.  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Definiert eine Zeitzone.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

