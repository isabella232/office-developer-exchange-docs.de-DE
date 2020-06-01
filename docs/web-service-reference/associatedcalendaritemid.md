---
title: AssociatedCalendarItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AssociatedCalendarItemId
api_type:
- schema
ms.assetid: 5b29898c-ea59-4e6a-914c-c011ec754032
description: Das AssociatedCalendarItemId-Element stellt das Kalenderelement dar, das einem MeetingMessage, MeetingRequest, MeetingResponse, MeetingCancellation oder ReminderMessageData zugeordnet ist.
ms.openlocfilehash: 816372c38243ba0fe5a7606c264dd1c5107350f2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460883"
---
# <a name="associatedcalendaritemid"></a>AssociatedCalendarItemId

Das **AssociatedCalendarItemId** -Element stellt das Kalenderelement dar, das einem [MeetingMessage](meetingmessage.md), [MeetingRequest](meetingrequest.md), [MeetingResponse](meetingresponse.md), [MeetingCancellation](meetingcancellation.md)oder [ReminderMessageData](remindermessagedata.md)zugeordnet ist.
  
```XML
<AssociatedCalendarItemId Id="" ChangeKey=""/>
```

 **Itemidtype**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Id** <br/> |Gibt das Kalenderelement an, das der Besprechung zugeordnet ist.  <br/> |
|**ChangeKey** <br/> |Gibt eine bestimmte Version des Kalenderelements an, das einer Besprechung zugeordnet ist.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MeetingMessage](meetingmessage.md)  |  [MeetingRequest](meetingrequest.md)  |  [MeetingResponse](meetingresponse.md)  |  [MeetingCancellation](meetingcancellation.md)  |  [ReminderMessageData](remindermessagedata.md)
  
## <a name="remarks"></a>Bemerkungen

Versionen von Exchange, die mit Buildnummer 15.00.0913.09 beginnen, können das **AssociatedCalendarItemId** -Element als untergeordnetes Element des **ReminderMessageData** -Elements enthalten. 
  
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

