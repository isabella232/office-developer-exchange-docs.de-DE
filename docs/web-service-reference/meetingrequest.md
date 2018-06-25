---
title: MeetingRequest
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequest
api_type:
- schema
ms.assetid: c44f8804-a355-473d-a837-48cc91617251
description: Das MeetingRequest-Element darstellt, eine Besprechungsanfrage im Exchange-Speicher.
ms.openlocfilehash: 3e290613293cb6ad1563912e5015742ffc503d08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830450"
---
# <a name="meetingrequest"></a>MeetingRequest

Das **MeetingRequest** -Element darstellt, eine Besprechungsanfrage im Exchange-Speicher. 
  
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
|[' MimeContent '](mimecontent.md) <br/> |Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts in base64Binary Format dargestellt.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ItemClass](itemclass.md) <br/> |Die Nachrichtenklasse eines Elements darstellt.  <br/> |
|[Betreff](subject.md) <br/> |Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt. Der Betreff ist auf 255 Zeichen beschränkt.  <br/> |
|[Vertraulichkeit](sensitivity.md) <br/> |Gibt die Vertraulichkeitsstufe eines Elements an.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt dar, der Datum und Uhrzeit, die ein Element in einem Postfach empfangen wurde.  <br/> |
|[Size](size.md) <br/> |Die Größe in Bytes eines Elements darstellt. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Bedeutung eines Elements an.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Gibt an, ob ein Element noch nicht gesendet wurde.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Gibt an, ob ein Benutzer ein Element auf sich selbst gesendet.  <br/> |
|[IsResend](isresend.md) <br/> |Gibt an, ob das Element zuvor gesendet wurden.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Gibt an, ob das Element geändert wurde.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internet Message Header, die innerhalb eines Elements in einem Postfach enthalten sind.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.  <br/> |
|["Datetimecreated"](datetimecreated.md) <br/> |Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten. Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Stellt die Zeichenfolge, die für den Inhalt der CC-Zeile verwendet wird. Dies ist die verkettete Zeichenfolge alle Anzeigenamen der CC-Empfänger.  <br/> |
|[DisplayTo](displayto.md) <br/> |Stellt die Zeichenfolge, die für den Inhalt der Zeile verwendet wird. Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
|[Kultur](culture.md) <br/> |Stellt die Kultur für ein bestimmtes Element in einem Postfach an.  <br/> |
|[Absender](sender.md) <br/> |Bezeichnet den Absender eines Elements.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Enthält einen Satz an Empfänger einer Nachricht.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine lesebestätigung anfordert.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine Empfangsbestätigung anfordert.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Enthält eine binäre Kennung, die den Thread darstellt, zu dem diese Nachricht gehört.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Den Bezeichner für die Unterhaltung darstellt.  <br/> |
|[Von](from.md) <br/> |Stellt den Adressat dar, der die Nachricht gesendet hat.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Die Internetnachricht-ID eines Elements darstellt.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Gibt an, ob eine Antwort auf eine E-mail-Nachricht angefordert wird.  <br/> |
|[Referenzen](references.md) <br/> |Stellt den Usenet-Header, der zum Korrelieren Antworten mit ihrer ursprünglichen Nachrichten verwendet wird.  <br/> |
|[ReplyTo](replyto.md) <br/> |Identifiziert eine Reihe von Adressen, die an die Antworten gesendet werden soll.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Stellt das Kalenderelement, das eine [MeetingMessage](meetingmessage.md)zugeordnet ist.  <br/> |
|[IsDelegated](isdelegated.md) <br/> |Gibt an, ob eine Besprechung über ein Konto mit Stellvertretungszugriff behandelt wurde.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Gibt an, ob eine Besprechungsnachricht nicht mehr aktuell ist.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Gibt an, ob eine Besprechungsnachricht Element verarbeitet wurde.  <br/> |
|[ResponseType](responsetype.md) <br/> |Stellt die Art der Empfänger Antwort, die für eine Besprechung empfangen wird.  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |Beschreibt die Art der Besprechungsanfrage.  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |Stellt den gewünschten Status für den Kalenderelement, das die Besprechungsanfrage zugeordnet ist.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang des ein Kalenderelement. Dieses Element gilt nur für ein einzelnes Vorkommen des ein Kalenderelement.  <br/> |
|[Ende](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar. Dieses Element gilt nur für ein einzelnes Vorkommen des ein Kalenderelement.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprünglichen Startzeit eines Kalenderelements an.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Gibt an, ob ein Kalender-Elements oder einer Besprechungsanfrage ein ganztägiges Ereignis darstellt.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Stellt den Frei/Gebucht-Status des Kalenderelements an.  <br/> |
|[Ort](location.md) <br/> |Stellt den Speicherort einer Besprechung oder eines Termins.  <br/> |
|[Wenn](when.md) <br/> |Enthält eine Beschreibung der tritt einer Besprechung.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Gibt an, ob das Kalenderelement entweder einer Besprechung oder eines Termins ist.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Gibt an, ob eines Termins oder einer Besprechung abgebrochen wurde.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Gibt an, ob ein Kalenderelement Teil einer Terminserie ist. Dieses Element ist schreibgeschützt.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Gibt an, ob eine Besprechungsanfrage an den gewünschten Teilnehmer gesendet wurde.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Stellt den Typ der Vorkommen eines Kalenderelements.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Enthält den Status des oder der Antwort auf ein Kalenderelement.  <br/> |
|[Organisator](organizer.md) <br/> |Stellt den Organisator einer Besprechung dar.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt die Teilnehmer, die erforderlich sind, an einer Besprechung teilnehmen.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt die Teilnehmer, die nicht erforderlich sind, an einer Besprechung teilnehmen.  <br/> |
|[Ressourcen ](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Stellt die Anzahl der Besprechungen, die mit der Besprechungsanfrage in Konflikt stehen.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Die Gesamtzahl der Kalenderelemente, die an eine Besprechungszeit angrenzen darstellt.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.  <br/> |
|[Dauer (Elemente)](duration-items.md) <br/> |Stellt die Dauer der ein Kalenderelement.  <br/> |
|[TimeZone (Element)](timezone-item.md) <br/> |Enthält einen beschreibenden Text für eine Zeitzone.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Stellt das Datum und Uhrzeit, wenn ein Teilnehmer darauf geantwortet, auf eine Besprechungsanfrage.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Gibt die Sequenznummer einer Version eines Termins.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Gibt den Status des Termins.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält ein Array von sich wiederholenden Kalender Element vorkommen, die geändert wurden, damit diese als das Master-Shape Recurrence-Element unterschiedlich sind.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Enthält ein Array von gelöschten Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.  <br/> |
|[StartTimeZone-Zeitzone](starttimezone.md) <br/> |Stellt die Start-Zeitzone des Kalenderelements an.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Stellt die End-Zeitzone des Kalenderelements an.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Beschreibt die Art der Konferenz, die mit einem Kalenderelement ausgeführt wird.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Stellt dar, ob eine neue Besprechungszeit für eine Besprechung vorgeschlagen werden kann.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Gibt an, ob die Besprechung online ist.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Enthält die URL für den Besprechungsarbeitsbereich, der durch das Kalenderelement verknüpft ist.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Gibt die URL für eine Microsoft Netshow online-Besprechung.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Die Rechte des Clients basierend auf die berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.  <br/> |
|[ZuletztGeändertUm](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält die ID eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.  <br/> |
|[UID](uid.md) <br/> |Ein Kalenderelement identifiziert.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Gibt an, das Datum und die Uhrzeit der Erstellung eine Instanz eines iCalendar-Objekts.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Gibt ein einzelnes Element in der lokalen Client-Speicher zu erstellen.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen an.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen zu erstellen.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

