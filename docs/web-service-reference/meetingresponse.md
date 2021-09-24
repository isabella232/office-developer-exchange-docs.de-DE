---
title: MeetingResponse
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingResponse
api_type:
- schema
ms.assetid: 9f798e79-dafd-4d4d-9967-95fd8e5c0502
description: Das MeetingResponse-Element stellt eine Besprechungsantwort im Exchange Store dar.
ms.openlocfilehash: 7fa4c8d618291e69a668fcc2f9ddcd72e9ca28bc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59532615"
---
# <a name="meetingresponse"></a>MeetingResponse

Das **MeetingResponse-Element** stellt eine Besprechungsantwort im Exchange Store dar. 
  
```xml
<MeetingResponse>
   <MimeContent/>
   <ItemId/>
   <ParentFolderId/>
   <ItemClass/>
   <Subject/>
   <Sensitivity/>
   <Body/>
   <Attachments/>
   <DateTimeReceived/>
   <Size/>
   <Categories/>
   <Importance/>
   <InReplyTo/>
   <IsSubmitted/>
   <IsDraft/>
   <IsFromMe/>
   <IsResend/>
   <IsUnmodified/>
   <InternetMessageHeaders/>
   <DateTimeSent/>
   <DateTimeCreated/>
   <ResponseObjects/>
   <ReminderDueBy/>
   <ReminderIsSet/>
   <ReminderMinutesBeforeStart/>
   <DisplayCc/>
   <DisplayTo/>
   <HasAttachments/>
   <ExtendedProperty/>
   <Culture/>
   <Sender/>
   <ToRecipients/>
   <CcRecipients/>
   <BccRecipients/>
   <IsReadReceiptRequested/>
   <IsDeliveryReceiptRequested/>
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <IsResponseRequested/>
   <References/>
   <ReplyTo/>
   <AssociatedCalendarItemId/>
   <IsDelegated/>
   <IsOutOfDate/>
   <HasBeenProcessed/>
   <ResponseType/>
   <EffectiveRights/>
   <ReceivedBy/>
   <ReceivedRepresenting/>
   <ProposedStart/>
   <ProposedEnd/>
</MeetingResponse>
```

 **MeetingResponseMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Enthält den systemeigenen MIME-Datenstrom eines Objekts, das im base64Binary-Format dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements im Exchange Speicher. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ItemClass](itemclass.md) <br/> |Stellt die Nachrichtenklasse eines Elements dar.  <br/> |
|[Betreff](subject.md) <br/> |Stellt den Betreff für Exchange Speichern von Elementen und Antwortobjekten dar. Der Betreff ist auf 255 Zeichen beschränkt.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Gibt die Vertraulichkeitsstufe eines Elements an.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht dar.  <br/> |
|[Anhänge](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange Speicher angefügt sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt die Daten und die Uhrzeit dar, zu der ein Element in einem Postfach empfangen wurde.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe eines Elements in Byte dar. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen dar, die angeben, zu welchen Kategorien ein Element im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Wichtigkeit eines Elements.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements dar, auf das dieses Element eine Antwort ist.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element an den Standardordner "Postausgang" übermittelt wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Gibt an, ob ein Element noch nicht gesendet wurde.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.  <br/> |
|[IsResend](isresend.md) <br/> |Gibt an, ob das Element zuvor gesendet wurde.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Gibt an, ob das Element geändert wurde.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internet-Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Gibt das Datum und die Uhrzeit an, zu der ein Element in einem Postfach gesendet wurde.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Stellt das Datum und die Uhrzeit der Erstellung eines bestimmten Elements im Postfach dar.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwortobjekte, die einem Element im Exchange Speicher zugeordnet sind.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Gibt das Datum und die Uhrzeit des Auftretens des Ereignisses an. Dies wird vom [ReminderMinutesBeforeStart-Element](reminderminutesbeforestart.md) verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Gibt an, ob eine Erinnerung für ein Element im Exchange Speicher festgelegt wurde.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds "Cc" verwendet wird. Dies ist die verkettete Zeichenfolge aller Cc-Empfängeranzeigenamen.  <br/> |
|[DisplayTo](displayto.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds An verwendet wird. Dies ist die verkettete Zeichenfolge aller An-Empfänger-Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft dar, die auf **"true"** festgelegt ist, wenn ein Element mindestens eine anlage sichtbar hat. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
|[Culture](culture.md) <br/> |Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.  <br/> |
|[Absender](sender.md) <br/> |Bezeichnet den Absender eines Elements.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Enthält eine Reihe von Empfängern einer Nachricht.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements einen Übermittlungsbeleg anfordert.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Stellt den Unterhaltungsbezeichner dar.  <br/> |
|[Von](from.md) <br/> |Stellt den Adressat dar, der die Nachricht gesendet hat.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Stellt den Internetnachrichtenbezeichner eines Elements dar.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Gibt an, ob eine Antwort auf eine E-Mail-Nachricht angefordert wird.  <br/> |
|[Informationsquellen](references.md) <br/> |Stellt den Usenet-Header dar, der verwendet wird, um Antworten mit ihren ursprünglichen Nachrichten zu korrelieren.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifiziert eine Gruppe von Adressen, an die Antworten gesendet werden sollen.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Stellt das Kalenderelement dar, das einer [MeetingMessage](meetingmessage.md)zugeordnet ist.  <br/> |
|[IsDelegated](isdelegated.md) <br/> |Gibt an, ob eine Besprechung von einem Konto mit Stellvertretungszugriff behandelt wurde.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Gibt an, ob eine Besprechungsnachricht veraltet ist.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Gibt an, ob ein Besprechungsnachrichtenelement verarbeitet wurde.  <br/> |
|[ResponseType](responsetype.md) <br/> |Stellt den Typ der Empfängerantwort dar, die für eine Besprechung empfangen wird.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt. Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Identifiziert den Delegaten in einem Delegatzugriffsszenario. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Identifiziert den Prinzipal in einem Stellvertretungs-Zugriffsszenario. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[ProposedStart](proposedstart.md) <br/> |Gibt die vorgeschlagene Startzeit einer Besprechung an. Dieses Element wurde in Microsoft Exchange Server 2013 eingeführt. <br/> |
|[ProposedEnd](proposedend.md) <br/> |Gibt die vorgeschlagene Endzeit einer Besprechung an. Dieses Element wurde in Microsoft Exchange Server 2013 eingeführt. <br/> |
|[UID](uid.md) <br/> |Identifiziert ein Kalenderelement.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Wird verwendet, um eine bestimmte Instanz eines Terminserienkalenderelements zu identifizieren.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Gibt das Datum und die Uhrzeit der Erstellung einer Instanz eines iCalendar-Objekts an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Identifiziert alle Kalenderelemente, die sich neben einer Besprechungszeit befinden.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt geraten.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[Items](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
|[Items (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von zu erstellenden Elementen.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange Element dar, das einem anderen Exchange Element zugeordnet ist.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
   
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

