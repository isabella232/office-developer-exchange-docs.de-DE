---
title: UniqueBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueBody
api_type:
- schema
ms.assetid: 06bc95d7-121c-433b-bd27-c2b0eb8c011f
description: Das UniqueBody-Element stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.
ms.openlocfilehash: 0a8d52c7d4eb8bda9fd41c4c25e448523185df93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461919"
---
# <a name="uniquebody"></a>UniqueBody

Das **UniqueBody** -Element stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt. 
  
```XML
<UniqueBody BodyType=""/>
```

 **BodyType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**BodyType** <br/> |Beschreibt, wie der Element Text im Element gespeichert wird.  <br/> |
   
#### <a name="bodytype-attribute"></a>BodyType-Attribut

|**Wert**|**Beschreibung**|
|:-----|:-----|
|**HTML** <br/> |Wandelt alle Textkörper in HTML um.  <br/> |
|**Text** <br/> |Wandelt alle Textkörper in nur-Text um.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[PostItem](postitem.md) <br/> |Stellt ein Post-Element im Exchange-Informationsspeicher dar.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

