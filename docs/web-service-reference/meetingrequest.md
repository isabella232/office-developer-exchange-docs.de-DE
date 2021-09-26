---
title: MeetingRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MeetingRequest
api_type:
- schema
ms.assetid: c44f8804-a355-473d-a837-48cc91617251
description: Das MeetingRequest-Element stellt eine Besprechungsanfrage im Exchange Store dar.
ms.openlocfilehash: 76bad3d920aa38bd2b7f42a9d0b30b8f01c8d1bd
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59542183"
---
# <a name="meetingrequest"></a>MeetingRequest

Das **MeetingRequest-Element** stellt eine Besprechungsanfrage im Exchange Store dar. 
  
```xml
<MeetingRequest>
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
   <MeetingRequestType/>
   <IntendedFreeBusyStatus/>
   <Start/>
   <End/>
   <OriginalStart/>
   <IsAllDayEvent/>
   <LegacyFreeBusyStatus/>
   <Location/>
   <When/>
   <IsMeeting/>
   <IsCancelled/>
   <IsRecurring/>
   <MeetingRequestWasSent/>
   <CalendarItemType/>
   <MyResponseType/>
   <Organizer/>
   <RequiredAttendees/>
   <OptionalAttendees/>
   <Resources/>
   <ConflictingMeetingCount/>
   <AdjacentMeetingCount/>
   <ConflictingMeetings/>
   <AdjacentMeetings/>
   <Duration/>
   <TimeZone/>
   <AppointmentReplyTime/>
   <AppointmentSequenceNumber/>
   <AppointmentState/>
   <Recurrence/>
   <FirstOccurrence/>
   <LastOccurrence/>
   <ModifiedOccurrences/>
   <DeletedOccurrences/>
   <MeetingTimeZone/>
   <StartTimeZone/>
   <EndTimeZone/>
   <ConferenceType/>
   <AllowNewTimeProposal/>
   <IsOnlineMeeting/>
   <MeetingWorkspaceUrl/>
   <NetShowUrl/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</MeetingRequest>
```

 **MeetingRequestMessageType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Enthält den systemeigenen MIME-Stream (Multipurpose Internet Mail Extensions) eines Objekts, das im base64Binary-Format dargestellt wird.  <br/> |
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
|[DisplayCc](displaycc.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird. Dies ist die verkettete Zeichenfolge aller CC-Empfängeranzeigenamen.  <br/> |
|[DisplayTo](displayto.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt der Zeile "An" verwendet wird. Dies ist die verkettete Zeichenfolge aller An-Empfänger-Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft dar, die auf **"true"** festgelegt ist, wenn ein Element mindestens eine anlage sichtbar hat. Diese Eigenschaft ist schreibgeschützter Wert.  <br/> |
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
|[ResponseType](responsetype.md) <br/> |Stellt die Art der Empfängerantwort dar, die für eine Besprechung empfangen wird.  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |Beschreibt den Typ der Besprechungsanfrage.  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |Stellt den beabsichtigten Status für das Kalenderelement dar, das der Besprechungsanfrage zugeordnet ist.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang eines Kalenderelements dar. Dieses Element gilt nur für ein einzelnes Vorkommen eines Kalenderelements.  <br/> |
|[Ende ](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar. Dieses Element gilt nur für ein einzelnes Vorkommen eines Kalenderelements.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprüngliche Startzeit eines Kalenderelements dar.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Stellt den Frei/Gebucht-Status des Kalenderelements dar.  <br/> |
|[Ort](location.md) <br/> |Stellt den Ort einer Besprechung oder eines Termins dar.  <br/> |
|[When](when.md) <br/> |Stellt eine Beschreibung des Zeitpunkts einer Besprechung bereit.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Gibt an, ob das Kalenderelement eine Besprechung oder ein Termin ist.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Gibt an, ob ein Termin oder eine Besprechung abgesagt wurde.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Gibt an, ob ein Kalenderelement Teil einer Terminserie ist. Dieses Element ist schreibgeschützt.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Gibt an, ob eine Besprechungsanfrage an die angeforderten Teilnehmer gesendet wurde.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Stellt den Vorkommenstyp eines Kalenderelements dar.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Enthält den Status oder die Antwort auf ein Kalenderelement.  <br/> |
|[Organisator](organizer.md) <br/> |Stellt den Organisator einer Besprechung dar.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt Teilnehmer dar, die an einer Besprechung teilnehmen müssen.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt Teilnehmer dar, die nicht an einer Besprechung teilnehmen müssen.  <br/> |
|[Ressourcen](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung dar.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Stellt die Anzahl der Besprechungen dar, die mit der Besprechungsanfrage in Konflikt geraten.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Stellt die Gesamtanzahl der Kalenderelemente dar, die sich neben einer Besprechungszeit befinden.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt geraten.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente neben einer Besprechungszeit.  <br/> |
|[Dauer (Elemente)](duration-items.md) <br/> |Stellt die Dauer eines Kalenderelements dar.  <br/> |
|[TimeZone (Element)](timezone-item.md) <br/> |Stellt eine Textbeschreibung einer Zeitzone bereit.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Gibt das Datum und die Uhrzeit an, zu der ein Teilnehmer auf eine Besprechungsanfrage geantwortet hat.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Gibt die Sequenznummer einer Version eines Termins an.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Gibt den Status des Termins an.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält ein Array wiederkehrender Kalenderelementvorkommen, die geändert wurden, sodass sie sich vom Serienmasterelement unterscheiden.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Enthält ein Array gelöschter Vorkommen eines Terminserienkalenderelements.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Orts dar, an dem die Besprechung gehostet wird.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Stellt die Startzeitzone des Kalenderelements dar.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Stellt die Endzeitzone des Kalenderelements dar.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Beschreibt den Konferenztyp, der mit einem Kalenderelement ausgeführt wird.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Gibt an, ob eine neue Besprechungszeit für eine Besprechung vorgeschlagen werden kann.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Gibt an, ob die Besprechung online ist.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Enthält die URL für den Besprechungsarbeitsbereich, mit dem das Kalenderelement verknüpft ist.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Gibt die URL für eine Microsoft Netshow-Onlinebesprechung an.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des letzten Benutzers, der ein Element geändert hat.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Outlook Web App Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur Text dar, das den eindeutigen Textkörper dieser Unterhaltung darstellt.  <br/> |
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
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

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

