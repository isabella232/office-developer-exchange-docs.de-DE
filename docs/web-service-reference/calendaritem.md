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
description: CalendarItem-Element stellt ein Element der Exchange-Kalender.
ms.openlocfilehash: c7b6d4930bc42fbe26d35264e2eae0c986cc8db7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757532"
---
# <a name="calendaritem"></a>CalendarItem

**CalendarItem** -Element stellt ein Element der Exchange-Kalender. 
  
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
|[' MimeContent '](mimecontent.md) <br/> |Enthält den systemeigene Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im Format base64Binary dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, der das Element oder Ordner enthält.  <br/> |
|[ItemClass](itemclass.md) <br/> |Die Nachrichtenklasse eines Elements darstellt.  <br/> |
|[Betreff](subject.md) <br/> |Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.  <br/> |
|[Vertraulichkeit](sensitivity.md) <br/> |Gibt die Vertraulichkeitsstufe eines Elements an.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach empfangen wurde.  <br/> |
|[Size](size.md) <br/> |Die Größe in Bytes eines Elements darstellt. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen, die die Kategorien zu identifizieren, zu denen ein Element im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Bedeutung eines Elements an.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Gibt an, ob ein Element noch nicht gesendet wurde.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Gibt an, ob ein Benutzer ein Element an sich gesendet.  <br/> |
|[IsResend](isresend.md) <br/> |Gibt an, ob das Element zuvor gesendet wurden.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Gibt an, ob das Element geändert wurde.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internet Message Header, die in einem Element in einem Postfach enthalten sind.  <br/> |
|[DateTimeSent](datetimesent.md) <br/> |Stellt das Datum und die Uhrzeit, die ein Element in einem Postfach gesendet wurde.  <br/> |
|["Datetimecreated"](datetimecreated.md) <br/> |Stellt das Datum und die Uhrzeit, die ein bestimmtes Element im Postfach erstellt wurde.  <br/> |
|[ResponseObjects](responseobjects.md) <br/> |Enthält eine Auflistung aller Antwort-Objekte, die ein Element in der Exchange-Informationsspeicher zugeordnet sind.  <br/> |
|[ReminderDueBy](reminderdueby.md) <br/> |Stellt das Datum und die Uhrzeit bei des Ereignisses eintreten. Dies wird durch die [ReminderMinutesBeforeStart](reminderminutesbeforestart.md) -Element verwendet, um zu bestimmen, wann die Erinnerung angezeigt wird.  <br/> |
|[ReminderIsSet](reminderisset.md) <br/> |Gibt an, ob eine Erinnerung für ein Element in der Exchange-Informationsspeicher festgelegt wurde.  <br/> |
|[ReminderMinutesBeforeStart](reminderminutesbeforestart.md) <br/> |Stellt die Anzahl der Minuten, bevor ein Ereignis, wenn eine Erinnerung angezeigt wird.  <br/> |
|[DisplayCc](displaycc.md) <br/> |Stellt die Zeichenfolge, die für den Inhalt der Cc-Zeile verwendet wird. Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.  <br/> |
|[DisplayTo](displayto.md) <br/> |Stellt die Zeichenfolge, die für den Inhalt der Zeile verwendet wird. Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
|[Kultur](culture.md) <br/> |Stellt die Kultur für ein bestimmtes Element in einem Postfach an.  <br/> |
|[UID](uid.md) <br/> |Ein Kalenderelement identifiziert.  <br/> |
|[RecurrenceId](recurrenceid.md) <br/> |Verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.  <br/> |
|[DateTimeStamp](datetimestamp.md) <br/> |Gibt an, das Datum und die Uhrzeit der Erstellung eine Instanz eines iCalendar-Objekts.  <br/> |
|[Start](start.md) <br/> |Stellt den Anfang des ein Kalenderelement. Dieses Element gilt nur für ein einzelnes Vorkommen des ein Kalenderelement.  <br/> |
|[Ende](end-ex15websvcsotherref.md) <br/> |Stellt das Ende einer Dauer dar. Dieses Element gilt nur für ein einzelnes Vorkommen des ein Kalenderelement.  <br/> |
|[OriginalStart](originalstart.md) <br/> |Stellt die ursprünglichen Startzeit eines Kalenderelements an.  <br/> |
|[IsAllDayEvent](isalldayevent.md) <br/> |Gibt an, ob ein Kalender-Elements oder einer Besprechungsanfrage ein ganztägiges Ereignis darstellt.  <br/> |
|[LegacyFreeBusyStatus](legacyfreebusystatus.md) <br/> |Stellt den Frei/Gebucht-Status des Kalenderelements an.  <br/> |
|[Ort](location.md) <br/> |Stellt den Speicherort einer Besprechung oder eines Termins.  <br/> |
|[Wenn](when.md) <br/> |Enthält Informationen dazu, wann ein Kalenderelement auftritt.  <br/> |
|[IsMeeting](ismeeting.md) <br/> |Gibt an, ob das Kalenderelement einer Besprechung oder eines Termins ist.  <br/> |
|[IsCancelled](iscancelled.md) <br/> |Gibt an, ob eines Termins oder einer Besprechung abgebrochen wurde.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Gibt an, ob ein Kalenderelement Teil einer Terminserie ist. Dieses Element ist schreibgeschützt.  <br/> |
|[MeetingRequestWasSent](meetingrequestwassent.md) <br/> |Gibt an, ob eine Besprechungsanfrage an den gewünschten Teilnehmer gesendet wurde.  <br/> |
|[IsResponseRequested](isresponserequested.md) <br/> |Gibt an, ob eine Antwort auf ein Element erforderlich ist.  <br/> |
|[CalendarItemType](calendaritemtype.md) <br/> |Stellt den Typ der Vorkommen eines Kalenderelements.  <br/> |
|[MyResponseType](myresponsetype.md) <br/> |Enthält den Status des oder der Antwort auf ein Kalenderelement.  <br/> |
|[Organisator](organizer.md) <br/> |Stellt den Organisator einer Besprechung dar.  <br/> |
|[RequiredAttendees](requiredattendees.md) <br/> |Stellt die Teilnehmer, die erforderlich sind, an einer Besprechung teilnehmen.  <br/> |
|[OptionalAttendees](optionalattendees.md) <br/> |Stellt die Teilnehmer, die nicht erforderlich sind, an einer Besprechung teilnehmen.  <br/> |
|[Ressourcen ](resources.md) <br/> |Stellt eine geplante Ressource für eine Besprechung.  <br/> |
|[ConflictingMeetingCount](conflictingmeetingcount.md) <br/> |Stellt die Anzahl der Besprechungen, die mit dem Kalenderelement in Konflikt stehen.  <br/> |
|[AdjacentMeetingCount](adjacentmeetingcount.md) <br/> |Die Gesamtzahl der Kalenderelemente, die an eine Besprechungszeit angrenzen darstellt.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.  <br/> |
|[Dauer (Elemente)](duration-items.md) <br/> |Stellt die Dauer der ein Kalenderelement.  <br/> |
|[TimeZone (Element)](timezone-item.md) <br/> |Enthält einen beschreibenden Text für eine Zeitzone.  <br/> |
|[AppointmentReplyTime](appointmentreplytime.md) <br/> |Stellt das Datum und Uhrzeit, wenn ein Teilnehmer darauf geantwortet, auf eine Besprechungsanfrage.  <br/> |
|[AppointmentSequenceNumber](appointmentsequencenumber.md) <br/> |Gibt die Sequenznummer einer Version eines Termins.  <br/> |
|[AppointmentState](appointmentstate.md) <br/> |Gibt den Status des Termins.  <br/> |
|[Serie (RecurrenceType)](recurrence-recurrencetype.md) <br/> |Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[FirstOccurrence](firstoccurrence.md) <br/> |Stellt das erste Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[LastOccurrence](lastoccurrence.md) <br/> |Stellt das letzte Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[ModifiedOccurrences](modifiedoccurrences.md) <br/> |Enthält ein Array von sich wiederholenden Kalender Element vorkommen, die geändert wurden, damit sie aus dem master Recurrence-Element unterscheiden.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[DeletedOccurrences](deletedoccurrences.md) <br/> |Enthält ein Array von gelöschten Vorkommen eines sich wiederholenden Kalenderelements an.  <br/> Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.  <br/> |
|[MeetingTimeZone](meetingtimezone.md) <br/> |Stellt die Zeitzone des Speicherorts, in die Besprechung gehostet wird.  <br/> |
|[StartTimeZone-Zeitzone](starttimezone.md) <br/> |Stellt die Start-Zeitzone des Kalenderelements an.  <br/> |
|[EndTimeZone](endtimezone.md) <br/> |Stellt die End-Zeitzone des Kalenderelements an.  <br/> |
|[ConferenceType](conferencetype.md) <br/> |Beschreibt die Art der Konferenz, die mit einem Kalenderelement ausgeführt wird.  <br/> |
|[AllowNewTimeProposal](allownewtimeproposal.md) <br/> |Gibt an, ob für eine Besprechung durch ein Teilnehmer eine neue Besprechungszeit vorgeschlagen werden kann.  <br/> |
|[IsOnlineMeeting](isonlinemeeting.md) <br/> |Gibt an, ob die Besprechung online ist.  <br/> |
|[MeetingWorkspaceUrl](meetingworkspaceurl.md) <br/> |Enthält die URL für den Besprechungsarbeitsbereich, der durch das Kalenderelement verknüpft ist.  <br/> |
|[NetShowUrl](netshowurl.md) <br/> |Gibt die URL für eine Microsoft NetShow online-Besprechung.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.  <br/> |
|[ZuletztGeändertUm](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App bearbeiten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält die ID eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten an eine einzelne Eigenschaft eines Elements oder Ordners während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen an.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Gibt ein einzelnes Element in den Speicher des lokalen Client aktualisieren.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Wenn ein einzelnes Kalenderelement ein wiederkehrendes master Kalenderelement vertraut aktualisiert wird, muss das [MeetingTimeZone](meetingtimezone.md) -Element, um das Kalenderelement ursprüngliche Zeitzone beibehalten angegeben werden. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
  
[EWS-Referenz für Exchange](ews-reference-for-exchange.md)

