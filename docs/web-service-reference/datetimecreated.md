---
title: DateTimeCreated
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- DateTimeCreated
api_type:
- schema
ms.assetid: 42ae0067-4688-49d9-93c5-c4dbeb54cee1
description: Das DateTimeCreated-Element stellt das Datum und die Uhrzeit der Erstellung eines Elements im Postfach dar.
ms.openlocfilehash: 065ad1b362ba903cc2e29f071347cbb0d19d8452
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535703"
---
# <a name="datetimecreated"></a>DateTimeCreated

Das **DateTimeCreated-Element** stellt das Datum und die Uhrzeit der Erstellung eines Elements im Postfach dar. 
  
```xml
<DateTimeCreated/>
```

**DateTime**

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
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[Element](item.md) <br/> |Stellt ein Element im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Der Textwert stellt das Datum und die Uhrzeit dar, zu der ein Element im Postfach erstellt wurde.
  
## <a name="remarks"></a>HinwBemerkungeneise

Mithilfe von Kalenderantwortobjekten wird die [DateTimeCreated-Eigenschaft](datetimecreated.md) für das zugeordnete Kalenderelement aktualisiert. Das erwartete Verhalten ist, dass die **DateTimeCreated-Eigenschaft** unverändert bleibt. Beispielsweise sendet Benutzer A eine Besprechungsanfrage an Benutzer B. Benutzer B akzeptiert die Besprechungsanfrage mit dem Bezeichner der Besprechungsanfrage. Die **DateTimeCreated-Eigenschaft** des zugeordneten Kalenderelements wird geändert. 
  
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

