---
title: Aufgabe
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Task
api_type:
- schema
ms.assetid: 7c84927e-db28-4c5d-b0b5-cbcc2b88d869
description: Das Task-Element stellt eine Aufgabe im Exchange Speicher dar.
ms.openlocfilehash: 1a9d44480ec92c9adf158e7e71cf3f928b20b64d
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59544521"
---
# <a name="task"></a>Aufgabe

Das **Task-Element** stellt eine Aufgabe im Exchange Speicher dar. 
  
```xml
<Task>
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
   <ActualWork/>
   <AssignedTime/>
   <BillingInformation/>
   <ChangeCount/>
   <Companies/>
   <CompleteDate/>
   <Contacts/>
   <DelegationState/>
   <Delegator/>
   <DueDate/>
   <IsAssignmentEditable/>
   <IsComplete/>
   <IsRecurring/>
   <IsTeamTask/>
   <Mileage/>
   <Owner/>
   <PercentComplete/>
   <Recurrence/>
   <StartDate/>
   <Status/>
   <StatusDescription/>
   <TotalWork/>
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
</Task>
```

**TaskType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Enthält den systemeigenen MIME-Stream (Multipurpose Internet Mail Extensions) eines Objekts, das im base64Binary-Format dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements im Exchange Speicher.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält.  <br/> |
|[ItemClass](itemclass.md) <br/> |Stellt die Nachrichtenklasse eines Elements dar.  <br/> |
|[Betreff](subject.md) <br/> |Stellt den Betreff für Exchange Speichern von Elementen und Antwortobjekten dar.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Enthält den Status für die Vertraulichkeit eines Elements.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt einer Nachricht dar.  <br/> |
|[Anhänge](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange Speicher angefügt sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Gibt das Datum und die Uhrzeit des Empfangs eines Elements in einem Postfach an.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe eines Elements in Byte dar. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen dar, die angeben, zu welchen Kategorien ein Element im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Wichtigkeit eines Elements.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements dar, auf das dieses Element eine Antwort ist.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element an den Standardordner "Postausgang" übermittelt wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Gibt an, ob ein Element noch nicht gesendet wurde.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Gibt an, ob ein Benutzer ein Element an sich selbst gesendet hat.  <br/> |
|[IsResend](isresend.md) <br/> |Gibt an, ob das Element zuvor gesendet wurde.  <br/> |
|[IsUnmodified](isunmodified.md) <br/> |Gibt an, ob das Element geändert wurde.  <br/> |
|[InternetMessageHeaders](internetmessageheaders.md) <br/> |Stellt die Auflistung aller Internetnachrichtenkopfzeilen dar, die in einem Element in einem Postfach enthalten sind.  <br/> |
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
|[ActualWork](actualwork.md) <br/> |Stellt den tatsächlichen Zeitaufwand für einen Vorgang dar.  <br/> |
|[AssignedTime](assignedtime.md) <br/> |Stellt den Zeitpunkt dar, zu dem einem Kontakt eine Aufgabe zugewiesen wird.  <br/> |
|[BillingInformation](billinginformation.md) <br/> |Enthält Abrechnungsinformationen für eine Aufgabe.  <br/> |
|[ChangeCount](changecount.md) <br/> |Gibt die Version der Aufgabe an.  <br/> |
|[Companies](companies.md) <br/> |Stellt die Sammlung von Unternehmen dar, die einem Kontakt oder einer Aufgabe zugeordnet sind.  <br/> |
|[CompleteDate](completedate.md) <br/> |Stellt das Datum dar, an dem eine Aufgabe abgeschlossen wird.  <br/> |
|[Kontakte](contacts-ex15websvcsotherref.md) <br/> |Enthält eine Liste der Kontakte, die einem Vorgang zugeordnet sind.  <br/> |
|[DelegationState](delegationstate.md) <br/> |Stellt den Status einer delegierten Aufgabe dar.  <br/> |
|[Delegator](delegator.md) <br/> |Enthält den Namen des Delegators, der die Aufgabe zugewiesen hat.  <br/> |
|[DueDate](duedate.md) <br/> |Stellt das Datum dar, an dem ein Aufgabenelement fällig ist.  <br/> |
|[IsAssignmentEditable](isassignmenteditable.md) <br/> |Gibt an, ob die Aufgabe bearbeitbar ist oder nicht.  <br/> |
|[IsComplete](iscomplete.md) <br/> |Gibt an, ob die Aufgabe abgeschlossen wurde oder nicht.  <br/> |
|[IsRecurring](isrecurring.md) <br/> |Gibt an, ob eine Aufgabe Teil einer Terminserie ist. Dieses Element ist schreibgeschützt.  <br/> |
|[IsTeamTask](isteamtask.md) <br/> |Gibt an, ob die Aufgabe im Besitz eines Teams ist oder nicht.  <br/> |
|[Mileage](mileage.md) <br/> |Stellt die Laufleistung für ein Aufgabenelement dar.  <br/> |
|[Owner](owner.md) <br/> |Stellt den Besitzer einer Aufgabe dar.  <br/> |
|[PercentComplete](percentcomplete.md) <br/> |Beschreibt den Abschlussstatus einer Aufgabe.  <br/> |
|[Serie (TaskRecurrenceType)](recurrence-taskrecurrencetype.md) <br/> |Enthält Serieninformationen für wiederkehrende Vorgänge.  <br/> |
|[StartDate](startdate.md) <br/> |Stellt den Anfangstermin eines Aufgabenelements dar.  <br/> |
|[Status](status.md) <br/> |Stellt den Status eines Aufgabenelements dar.  <br/> |
|[StatusDescription](statusdescription.md) <br/> |Enthält eine Erläuterung des Aufgabenstatus.  <br/> |
|[TotalWork](totalwork.md) <br/> |Enthält eine Beschreibung, wie viel Arbeit einem Element zugeordnet ist.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des letzten Benutzers, der ein Element geändert hat.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Outlook Web App Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur Text dar, das den eindeutigen Textkörper dieser Unterhaltung darstellt.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente neben einer Besprechungszeit.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements/Ordners angefügt werden sollen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt geraten.  <br/> |
|[Create (ItemSync)](create-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange Element dar, das einem anderen Exchange Element zugeordnet ist.  <br/> |
|[Items](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)
- [Erstellen von Aufgaben](https://msdn.microsoft.com/library/0ef97334-e8a0-4f67-a23a-dd9e2bbad49f%28Office.15%29.aspx)
- [Deleting Tasks](https://msdn.microsoft.com/library/a3d7e25f-8a35-4901-b1d9-d31f418ab340%28Office.15%29.aspx)

