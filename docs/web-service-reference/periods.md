---
title: Zeiten
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Periods
api_type:
- schema
ms.assetid: 7920d81d-abba-4232-8bfe-49267b6c9a36
description: Das Periods-Element stellt ein Array von Zeiträumen dar, die den Zeitversatz in verschiedenen Phasen der Zeitzone definieren.
ms.openlocfilehash: e4a614c71e7194dd85db740da1796b69d9f25d69
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59515313"
---
# <a name="periods"></a>Zeiten

Das **Periods-Element** stellt ein Array von Zeiträumen dar, die den Zeitversatz in verschiedenen Phasen der Zeitzone definieren. 
  
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
|[Period](period.md) <br/> |Definiert den Namen, den Zeitversatz und den eindeutigen Bezeichner für eine bestimmte Phase der Zeitzone.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[StartTimeZone](starttimezone.md) <br/> |Definiert die Zeitzone für die Startzeit eines [CalendarItem-](calendaritem.md) oder [MeetingRequest-Objekt.](meetingrequest.md)  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Definiert die Zeitzone für die Endzeit eines [CalendarItem-](calendaritem.md) oder [MeetingRequest](meetingrequest.md)-Objekt.  <br/> |
|[TimeZoneDefinition](timezonedefinition.md) <br/> |Definiert eine Zeitzone.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

