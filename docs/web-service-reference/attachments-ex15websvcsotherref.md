---
title: Anlagen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Attachments
api_type:
- schema
ms.assetid: b470e614-34bb-44f0-8790-7ddbdcbbd29d
description: Das Attachments-Element enthält die Elemente oder Dateien, die an ein Element im Exchange Speicher angefügt sind.
ms.openlocfilehash: e37ff7710aaa08f3caabcecb056331091e50933c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59531201"
---
# <a name="attachments"></a>Anlagen

Das **Attachments-Element** enthält die Elemente oder Dateien, die an ein Element im Exchange Speicher angefügt sind. 
  
```xml
<Attachments>
   <ItemAttachment/>
   <FileAttachment/>
</Attachments>
```

 **ArrayOfAttachmentsType** und **NonEmptyArrayOfAttachmentsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange Element dar, das einem anderen Exchange Element zugeordnet ist.  <br/> |
|[FileAttachment](fileattachment.md) <br/> |Stellt eine Datei dar, die an ein Element im Exchange Speicher angefügt ist.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[CreateAttachment](createattachment.md) <br/> |Definiert eine Anforderung zum Erstellen einer Anlage zu einem Element im Exchange Speicher.<br/><br/> Es folgt der XPath-Ausdruck für dieses Element:  `/CreateAttachment` <br/> |
|[AcceptItem](acceptitem.md) <br/> | Stellt eine Accept-Antwort auf eine Besprechungsanfrage.<br/><br/>Nachfolgend sind einige der XPath-Ausdrücke für dieses Element aufgeführt:<ul><li>`/CreateItem/Items`</li><li>`/MeetingRequest/ConflictingMeetings` </li><li>`/SetItemField/CalendarItem/ConflictingMeetings`</li><li>`/AppendToItemField/CalendarItem/ConflictingMeetings`</li><li>`/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings`</li><li>`/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings`</li><li>`/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li><li>`/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings`</li></ul> |
|[DeclineItem](declineitem.md) <br/> |Stellt eine ablehnen Antwort auf eine Besprechungsanfrage.  <br/> |
|[TentativelyAcceptItem](tentativelyacceptitem.md) <br/> |Stellt eine mit Vorbehalt Antworten auf eine Besprechungsanfrage.  <br/> |
|[RemoveItem](removeitem.md) <br/> |Entfernt ein Element aus dem Exchange-Informationsspeicher.  <br/> |
|[Aspekt](item.md) <br/> |Stellt ein generisches Exchange Element dar.  <br/> |
|[MeetingMessage](meetingmessage.md) <br/> |Stellt eine Besprechung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingRequest](meetingrequest.md) <br/> |Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingResponse](meetingresponse.md) <br/> |Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.  <br/> |
|[MeetingCancellation](meetingcancellation.md) <br/> |Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.  <br/> |
|[Message](message-ex15websvcsotherref.md) <br/> |Stellt eine Exchange-E-Mail-Nachricht dar.  <br/> |
|[Aufgabe](task.md) <br/> |Stellt eine Aufgabe im Exchange-Informationsspeicher dar.  <br/> |
|[CalendarItem](calendaritem.md) <br/> |Stellt ein Element im Exchange-Kalender dar.  <br/> |
|[Kontaktperson](contact.md) <br/> |Stellt ein Exchange-Kontaktelement dar.  <br/> |
|[DistributionList](distributionlist.md) <br/> |Stellt eine Verteilerliste dar.  <br/> |
|[CreateAttachmentResponseMessage](createattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer einzelnen CreateAttachment-Anforderung.  <br/> |
|[GetAttachmentResponseMessage](getattachmentresponsemessage.md) <br/> |Enthält den Status und das Ergebnis einer GetAttachment-Anforderung.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Die **Attachments-Elemente** haben die gleichen untergeordneten Elemente, basieren jedoch auf verschiedenen Typen: **ArrayOfAttachmentsType** und **NonEmptyArrayOfAttachmentsType**. Die Typen definieren, ob ein untergeordnetes Element erforderlich ist. **ArrayOfAttachmentsType** wird nur in der Antwortnachricht verwendet. Es ist auch wichtig zu beachten, dass diese Elemente sowohl in den Nachrichten- als auch in Typennamespaces vorkommen. 
  
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

