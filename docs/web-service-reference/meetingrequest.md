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
description: Das MeetingRequest-Element stellt eine Besprechungsanfrage im Exchange-Informationsspeicher dar.
ms.openlocfilehash: 7b39ec52d2b4fe8b3cdd2b6fd5e7ba97cfa69c7e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465828"
---
# <a name="meetingrequest"></a>MeetingRequest

Das **MeetingRequest** -Element stellt eine Besprechungsanfrage im Exchange-Informationsspeicher dar. 
  
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
|[MimeContent](mimecontent.md) <br/> |Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines im base64Binary-Format dargestellten Objekts.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ItemClass](itemclass.md) <br/> |Stellt die Nachrichtenklasse eines Elements dar.  <br/> |
|[Betreff](subject.md) <br/> |Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar. Der Betreff ist auf 255 Zeichen limitiert.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Gibt die Empfindlichkeitsstufe eines Elements an.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textinhalt einer Nachricht dar.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt die Daten und die Zeit dar, die ein Element in einem Postfach empfangen wurde.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe eines Elements in Bytes dar. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Wichtigkeit eines Elements.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.  <br/> |
|[Issubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Gibt an, ob ein Element noch nicht gesendet wurde.  <br/> |
|[Isfromme](isfromme.md) <br/> |Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.  <br/> |
|[IsResend](isresend.md) <br/> |Gibt an, ob das Element zuvor gesendet wurde.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Gibt an, ob das Element geändert wurde.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internet Nachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach gesendet wurde.  <br/> |
|[DateTimeCreated](datetimecreated.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der ein bestimmtes Element im Postfach erstellt wurde.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Response-Objekte, die einem Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Stellt das Datum und die Uhrzeit des Eintretens des Ereignisses dar. Dies wird vom [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Gibt an, ob für ein Element im Exchange-Informationsspeicher eine Erinnerung festgelegt wurde.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Stellt die Anzahl von Minuten vor einem Ereignis dar, wenn eine Erinnerung angezeigt wird.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird. Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.  <br/> |
|[Displayto ursprünglicher](displayto.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt der an-Verbindung verwendet wird. Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
|[Kultur](culture.md) <br/> |Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.  <br/> |
|[Absender](sender.md) <br/> |Bezeichnet den Absender eines Elements.  <br/> |
|[ToRecipients](torecipients.md) <br/> |Enthält eine Gruppe von Empfängern einer Nachricht.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.  <br/> |
|[IsReadReceiptRequested](isreadreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine Lesebestätigung anfordert.  <br/> |
|[IsDeliveryReceiptRequested](isdeliveryreceiptrequested.md) <br/> |Gibt an, ob der Absender eines Elements eine Zustellungsbestätigung anfordert.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Stellt den Konversationsbezeichner dar.  <br/> |
|[Von](from.md) <br/> |Stellt den Adressat dar, der die Nachricht gesendet hat.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Stellt die Internet Nachrichten-ID eines Elements dar.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Gibt an, ob eine Antwort auf eine e-Mail-Nachricht angefordert wird.  <br/> |
|[References](references.md) <br/> |Stellt den Usenet-Header dar, der zum Korrelieren von Antworten mit ihren ursprünglichen Nachrichten verwendet wird.  <br/> |
|[ReplyTo](replyto.md) <br/> |Gibt eine Reihe von Adressen an, an die Antworten gesendet werden sollen.  <br/> |
|[AssociatedCalendarItemId](associatedcalendaritemid.md) <br/> |Stellt das Kalenderelement dar, das einem [MeetingMessage](meetingmessage.md)zugeordnet ist.  <br/> |
|[Isdelegated wurde](isdelegated.md) <br/> |Gibt an, ob eine Besprechung von einem Konto mit Stellvertretungszugriff verarbeitet wurde.  <br/> |
|[IsOutOfDate](isoutofdate.md) <br/> |Gibt an, ob eine Besprechungsnachricht veraltet ist.  <br/> |
|[HasBeenProcessed](hasbeenprocessed.md) <br/> |Gibt an, ob ein Besprechungsnachrichten Element verarbeitet wurde.  <br/> |
|[ResponseType](responsetype.md) <br/> |Stellt die Art der Empfängerantwort dar, die für eine Besprechung empfangen wird.  <br/> |
|[MeetingRequestType](meetingrequesttype.md) <br/> |Beschreibt den Typ der Besprechungsanfrage.  <br/> |
|[IntendedFreeBusyStatus](intendedfreebusystatus.md) <br/> |Stellt den beabsichtigten Status für das Kalenderelement dar, das der Besprechungsanfrage zugeordnet ist.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang eines Kalenderelements dar. Dieses Element gilt nur für ein einzelnes Vorkommen eines Kalenderelements.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar. Dieses Element gilt nur für ein einzelnes Vorkommen eines Kalenderelements.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprüngliche Startzeit eines Kalenderelements dar.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Stellt den Frei/Gebucht-Status des Kalenderelements dar.  <br/> |
|[Standort](location.md) <br/> |Stellt den Ort einer Besprechung oder eines Termins dar.  <br/> |
|[Wann](when.md) <br/> |Enthält eine Beschreibung des Auftretens einer Besprechung.  <br/> |
|[Ismeeting](ismeeting.md) <br/> |Gibt an, ob es sich beim Kalenderelement entweder um eine Besprechung oder einen Termin handelt.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Gibt an, ob ein Termin oder eine Besprechung storniert wurde.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Gibt an, ob ein Kalenderelement Teil eines wiederkehrenden Elements ist. Dieses Element ist schreibgeschützt.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Gibt an, ob eine Besprechungsanfrage an angeforderte Teilnehmer gesendet wurde.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Stellt den Typ des Vorkommens eines Kalenderelements dar.  <br/> |
|[Myresponsetype](myresponsetype.md) <br/> |Enthält den Status oder die Antwort auf ein Kalenderelement.  <br/> |
|[Organisator](organizer.md) <br/> |Stellt den Organisator einer Besprechung dar.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung erforderlich sind.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung nicht erforderlich sind.  <br/> |
|[Ressourcen](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung dar.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Stellt die Anzahl von Besprechungen dar, die mit der Besprechungsanfrage in Konflikt stehen.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Gibt die Gesamtzahl der Kalenderelemente an, die an eine Besprechungszeit angrenzen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
|[Dauer (Elemente)](duration-items.md) <br/> |Stellt die Dauer eines Kalenderelements dar.  <br/> |
|[Zeitzone (Element)](timezone-item.md) <br/> |Stellt eine Textbeschreibung einer Zeitzone bereit.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der ein Teilnehmer auf eine Besprechungsanfrage geantwortet hat.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Gibt die Sequenznummer einer Version eines Termins an.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Gibt den Status des Termins an.  <br/> |
|[Serie (serietype)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält ein Array von wiederkehrenden Kalenderelement vorkommen, die geändert wurden, sodass Sie sich vom Serienmasterelement unterscheiden.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Enthält ein Array von gelöschten Vorkommen eines wiederkehrenden Kalenderelements.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Speicherorts dar, an dem die Besprechung gehostet wird.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Stellt die Start Zeitzone des Kalenderelements dar.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Stellt die Ende Zeitzone des Kalenderelements dar.  <br/> |
|[Conferencetype](conferencetype.md) <br/> |Beschreibt die Art der Konferenz, die mit einem Kalenderelement durchgeführt wird.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Stellt dar, ob eine neue Besprechungszeit für eine Besprechung vorgeschlagen werden kann.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Gibt an, ob die Besprechung Online ist.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Enthält die URL des Besprechungsarbeitsbereichs, mit dem das Kalenderelement verknüpft ist.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Gibt die URL für eine Microsoft NetShow Online-Besprechung an.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[Isassociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.  <br/> |
|[UID](uid.md) <br/> |Identifiziert ein Kalenderelement.  <br/> |
|[Wiederholungs-Nr](recurrenceid.md) <br/> |Wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Gibt das Datum und die Uhrzeit der Erstellung einer Instanz eines iCalendar-Objekts an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Identifiziert alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während einer [UpdateItem Operation](updateitem-operation.md) an eine einzelne Eigenschaft eines Elements angefügt werden sollen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die erstellt werden sollen.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
   
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

