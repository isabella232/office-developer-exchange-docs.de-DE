---
title: MeetingTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingTimeZone
api_type:
- schema
ms.assetid: 413b47d9-8126-462c-9a4f-4e771a5e8889
description: Das MeetingTimeZone-Element stellt die Zeitzone des Orts dar, an dem die Besprechung gehostet wird.
ms.openlocfilehash: 5920e05b09ff02fafe58f38e94e3671a8234fd21
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532448"
---
# <a name="meetingtimezone"></a>MeetingTimeZone

Das **MeetingTimeZone-Element** stellt die Zeitzone des Orts dar, an dem die Besprechung gehostet wird. 
  
```xml
<MeetingTimeZone>
   <BaseOffset/>
   <Standard/>
   <Daylight/>
</MeetingTimeZone>
```

 **TimeZoneType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Timezonename** <br/> |Beschreibt den Namen der Zeitzone.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[BaseOffset](baseoffset.md) <br/> |Stellt den stündliche Offset von UTC für die aktuelle Zeitzone dar.  <br/> |
|[Standard](standard.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Sommerzeit in Standardzeit geändert wird.  <br/> |
|[Daylight](daylight.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

