---
title: ForwardItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ForwardItem
api_type:
- schema
ms.assetid: 97786086-8b91-4471-8af8-d21e8d66de87
description: Das ForwardItem-Element enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet.
ms.openlocfilehash: 8a82ff28ad1d0dc965a3284c1d0eac9b2fa38301
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758526"
---
# <a name="forwarditem"></a>ForwardItem

Das **ForwardItem** -Element enthält ein Exchange-Speicher-Element an Empfänger weitergeleitet. 
  
```xml
<ForwardItem>
   <Subject/>
   <Body/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <From/>
   <ReferenceItemId/>
   <NewBodyContent/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
</ForwardItem>
```

**ForwardItemType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Betreff](subject.md) <br/> |Die Subject-Eigenschaft der Exchange-Speicher-Elemente darstellt.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Enthält eine Reihe von Empfänger eines Elements an. Dies sind die primären Empfänger eines Elements.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.  <br/> |
|[Von](from.md) <br/> |Stellt die Adresse an, von der die Nachricht gesendet wurde.  <br/> |
|[ReferenceItemId](referenceitemid.md) <br/> |Identifiziert das Element auf dem im Response-Objekt verweist.  <br/> |
|[NewBodyContent](newbodycontent.md) <br/> |Stellt den neuen Textkörperinhalt einer Nachricht.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Identifiziert den Delegaten in eine Access Stellvertreter-Szenario. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Identifiziert den Prinzipal in einer Access Stellvertreter-Szenario. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> | Werden alle Elemente, die an eine Besprechungszeit angrenzen beschrieben.  <br/><br/>  Im folgenden sind einige der XPath-Ausdrücke auf dieses Element: <br/> <br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> | Beschreibt alle Elemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.  <br/><br/>  Im folgenden sind einige der XPath-Ausdrücke auf dieses Element: <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.  <br/> |
   
## <a name="remarks"></a>Hinweise

Das Element [von](from.md) sollte die e-Mail-Adresse des Prinzipals festgelegt werden, wenn ein Element von einer Stellvertretung weitergeleitet wird. Wenn die Eigenschaft [aus](from.md) die Stellvertretung nicht festlegt, erscheint das Element direkt aus der Stellvertretung Postfach gesendet wurden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

