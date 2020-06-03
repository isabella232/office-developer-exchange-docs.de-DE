---
title: CalendarItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarItem
api_type:
- schema
ms.assetid: b0c1fd27-b6da-46e5-88b8-88f00c71ba80
description: Das CalendarItem-Element stellt ein Exchange-Kalenderelement dar.
ms.openlocfilehash: b29141470d157ef5bd67be06a1e1fa1c9536b042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529483"
---
# <a name="calendaritem"></a>CalendarItem

Das **CalendarItem** -Element stellt ein Exchange-Kalenderelement dar. 
  
```XML
<CalendarItem>
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
   <IsResponseRequested/>
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
</CalendarItem>
```

 **CalendarItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.  <br/> |
|[ItemClass](itemclass.md) <br/> |Stellt die Nachrichtenklasse eines Elements dar.  <br/> |
|[Betreff](subject.md) <br/> |Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Gibt die Empfindlichkeitsstufe eines Elements an.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textinhalt einer Nachricht dar.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe eines Elements in Bytes dar. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen dar, die die Kategorien identifizieren, zu denen ein Element im Postfach gehört.  <br/> |
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
|[UID](uid.md) <br/> |Identifiziert ein Kalenderelement.  <br/> |
|[Wiederholungs-Nr](recurrenceid.md) <br/> |Wird verwendet, um eine bestimmte Instanz eines wiederkehrenden Kalenderelements zu identifizieren.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Gibt das Datum und die Uhrzeit der Erstellung einer Instanz eines iCalendar-Objekts an.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang eines Kalenderelements dar. Dieses Element gilt nur für ein einzelnes Vorkommen eines Kalenderelements.  <br/> |
|[End](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar. Dieses Element gilt nur für ein einzelnes Vorkommen eines Kalenderelements.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprüngliche Startzeit eines Kalenderelements dar.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Gibt an, ob ein Kalenderelement oder eine Besprechungsanfrage ein ganztägiges Ereignis darstellt.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Stellt den Frei/Gebucht-Status des Kalenderelements dar.  <br/> |
|[Standort](location.md) <br/> |Stellt den Ort einer Besprechung oder eines Termins dar.  <br/> |
|[Wann](when.md) <br/> |Enthält Informationen zum Zeitpunkt des Auftretens eines Kalenderelements.  <br/> |
|[Ismeeting](ismeeting.md) <br/> |Gibt an, ob es sich beim Kalenderelement um eine Besprechung oder einen Termin handelt.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Gibt an, ob ein Termin oder eine Besprechung abgebrochen wurde.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Gibt an, ob ein Kalenderelement Teil eines wiederkehrenden Elements ist. Dieses Element ist schreibgeschützt.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Gibt an, ob eine Besprechungsanfrage an angeforderte Teilnehmer gesendet wurde.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Gibt an, ob eine Antwort auf ein Element erforderlich ist.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Stellt den Typ des Vorkommens eines Kalenderelements dar.  <br/> |
|[Myresponsetype](myresponsetype.md) <br/> |Enthält den Status oder die Antwort auf ein Kalenderelement.  <br/> |
|[Organisator](organizer.md) <br/> |Stellt den Organisator einer Besprechung dar.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung erforderlich sind.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt Teilnehmer dar, die für die Teilnahme an einer Besprechung nicht erforderlich sind.  <br/> |
|[Ressourcen](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung dar.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Stellt die Anzahl von Besprechungen dar, die mit dem Kalenderelement in Konflikt stehen.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Gibt die Gesamtzahl der Kalenderelemente an, die an eine Besprechungszeit angrenzen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
|[Dauer (Elemente)](duration-items.md) <br/> |Stellt die Dauer eines Kalenderelements dar.  <br/> |
|[Zeitzone (Element)](timezone-item.md) <br/> |Stellt eine Textbeschreibung einer Zeitzone bereit.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu der ein Teilnehmer auf eine Besprechungsanfrage geantwortet hat.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Gibt die Sequenznummer einer Version eines Termins an.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Gibt den Status des Termins an.  <br/> |
|[Serie (serietype)](recurrence-recurrencetype.md) <br/> |Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines wiederkehrenden Kalenderelements dar.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält ein Array von wiederkehrenden Kalenderelement vorkommen, die geändert wurden, sodass Sie sich vom Serienmasterelement unterscheiden.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Enthält ein Array von gelöschten Vorkommen eines wiederkehrenden Kalenderelements.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Speicherorts dar, an dem die Besprechung gehostet wird.  <br/> |
|[StartTimeZone](starttimezone.md) <br/> |Stellt die Start Zeitzone des Kalenderelements dar.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Stellt die Ende Zeitzone des Kalenderelements dar.  <br/> |
|[Conferencetype](conferencetype.md) <br/> |Beschreibt die Art der Konferenz, die mit einem Kalenderelement durchgeführt wird.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Gibt an, ob eine neue Besprechungszeit für eine Besprechung von einem Teilnehmer vorgeschlagen werden kann.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Gibt an, ob die Besprechung Online ist.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Enthält die URL des Besprechungsarbeitsbereichs, mit dem das Kalenderelement verknüpft ist.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Gibt die URL für eine Microsoft NetShow Online-Besprechung an.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[Isassociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements oder Ordners angefügt werden sollen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Wenn ein einzelnes Kalenderelement als wiederkehrendes Master Kalenderelement aktualisiert wird, muss das [MeetingTimeZone](meetingtimezone.md) -Element angegeben werden, um die ursprüngliche Zeitzone des Kalenderelements beizubehalten. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
  
[EWS-Referenz für Exchange](ews-reference-for-exchange.md)

