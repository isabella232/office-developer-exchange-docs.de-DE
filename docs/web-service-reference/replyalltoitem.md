---
title: ReplyAllToItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- ReplyAllToItem
api_type:
- schema
ms.assetid: 8ca970ca-ca73-40db-9233-7b271cc5f44f
description: Das ReplyToAllItem-Element enthält eine Antwort an den Absender und alle identifizierten Empfänger eines Elements im Exchange Speicher.
ms.openlocfilehash: 33dc348686e99e4f21b67b18780a6a6691a7d72a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519016"
---
# <a name="replyalltoitem"></a>ReplyAllToItem

Das **ReplyToAllItem-Element** enthält eine Antwort an den Absender und alle identifizierten Empfänger eines Elements im Exchange Speicher. 
  
```xml
<ReplyAllToItem>
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
</ReplyAllToItem>
```

 **ReplyAllToItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Betreff](subject.md) <br/> |Stellt die Betreffeigenschaft Exchange Speicherelemente dar.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht dar.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Enthält eine Reihe von Empfängern eines Elements. Dies sind die primären Empfänger eines Elements.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Stellt eine Auflistung von Empfängern dar, die eine blinde Kopie (Bcc) einer E-Mail-Nachricht erhalten sollen.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements einen Übermittlungsbeleg anfordert.  <br/> |
|[From](from.md) <br/> |Stellt die Adresse dar, von der die Nachricht gesendet wurde.  <br/> |
|[ReferenceItemId](referenceitemid.md) <br/> |Gibt das Element an, auf das sich das Antwortobjekt bezieht.  <br/> |
|[NewBodyContent](newbodycontent.md) <br/> |Stellt den neuen Textkörperinhalt einer Nachricht dar.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Identifiziert den Delegaten in einem Delegatzugriffsszenario. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffsszenario. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> | Beschreibt alle Elemente neben einer Besprechungszeit.  <br/><br/>  Nachfolgend sind einige der XPath-Ausdrücke für dieses Element aufgeführt:  <br/><br/>  `/CalendarItem/AdjacentMeetings` <br/>  `/MeetingRequest/AdjacentMeetings` <br/>  `/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/AdjacentMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/AdjacentMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/AdjacentMeetings` <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> | Beschreibt alle Elemente, die mit einer Besprechungszeit in Konflikt geraten.  <br/><br/>  Nachfolgend sind einige der XPath-Ausdrücke für dieses Element aufgeführt: <br/> <br/>  `/CalendarItem/ConflictingMeetings` <br/>  `/MeetingRequest/ConflictingMeetings` <br/>  `/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/AcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/DeclineItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/TentativelyAcceptItem/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/SetItemField/CalendarItem/ConflictingMeetings` <br/>  `/UpdateItem/ItemChanges/ItemChange/Updates/AppendToItemField/CalendarItem/ConflictingMeetings` <br/>  `/CreateAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/>  `/GetAttachmentResponseMessage/Attachments/ItemAttachment/CalendarItem/ConflictingMeetings` <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwortobjekte, die einem Element im Exchange Speicher zugeordnet sind.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in dem ordner erstellt werden sollen, der durch das [ParentFolderIdId(TargetFolderIdType)-Element](parentfolderid-targetfolderidtype.md) identifiziert wird.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das [From-Element](from.md) sollte auf die E-Mail-Adresse des Prinzipals festgelegt werden, wenn ein Element eine Antwort eines Delegaten ist. Wenn der Delegat die [From-Eigenschaft](from.md) nicht festgelegt hat, scheint das Element direkt aus dem Postfach der Stellvertretung gesendet worden zu sein. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

