---
title: DistributionList
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DistributionList
api_type:
- schema
ms.assetid: f65aea01-e870-44a2-8571-fa6c001341cc
description: Das Element DistributionList stellt eine Verteilerliste dar.
ms.openlocfilehash: 5edcc83eef6a5b16470e6c290aacd057ceecceb1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758077"
---
# <a name="distributionlist"></a>DistributionList

Das Element **DistributionList** stellt eine Verteilerliste dar. 
  
```xml
<DistributionList>
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
   <EffectiveRights/>
   <LastModifiedName/>
   <LastModifiedTime/>
   <IsAssociated/>
   <WebClientReadFormQueryString/>
   <WebClientEditFormQueryString/>
   <ConversationId/>
   <UniqueBody/>
   <DisplayName/>
   <FileAs/>
   <ContactSource/>
   <Members/>
</DistributionList>
```

 **DistributionListType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[' MimeContent '](mimecontent.md) <br/> |Enthält den systemeigenen MIME-Stream eines Objekts in base64Binary Format dargestellt.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Listenelements Verteilung im Exchange-Speicher.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners, der die verteilerlistenelement enthält.  <br/> |
|[ItemClass](itemclass.md) <br/> |Stellt die Nachrichtenklasse eines Listenelements Verteilung.  <br/> |
|[Betreff](subject.md) <br/> |Der Betreff den Exchange-Speicherelemente und Antwortobjekte darstellt.  <br/> |
|[Vertraulichkeit](sensitivity.md) <br/> |Enthält den Status für ein Listenelement Verteilung Vertraulichkeit.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textkörperinhalt eines Listenelements Verteilung.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die ein verteilerlistenelement im Exchange-Speicher zugeordnet sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt das Datum und die Uhrzeit, zu der eine verteilerlistenelement in einem Postfach empfangen wurde.  <br/> |
|[Size](size.md) <br/> |Stellt die Größe in Bytes eines Listenelements Verteilung. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Listenelement Verteilung im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Bedeutung eines Listenelements Verteilung.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements, das dieses Element eine Antwort ist.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Stellt dar, ob ein Element noch nicht gesendet wurde.  <br/> |
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
|[DisplayCc](displaycc.md) <br/> |Stellt die Zeichenfolge, die für den Inhalt der Cc-Zeile verwendet wird. Dies ist die verkettete Zeichenfolge alle Anzeigenamen der Cc-Empfänger.  <br/> |
|[DisplayTo](displayto.md) <br/> |Stellt die Zeichenfolge, die für den Inhalt der Zeile verwendet wird. Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage sichtbar ist. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für ein Listenelement Verteilung identifiziert.  <br/> |
|[Kultur](culture.md) <br/> |Stellt die Kultur für ein Listenelement Verteilung in einem Postfach an.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.  <br/> |
|[ZuletztGeändertUm](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält die ID eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen einer Verteilerliste.  <br/> |
|[FileAs](fileas.md) <br/> |Stellt dar, wie eine Verteilerliste im Ordner "Kontakte" abgelegt wird.  <br/> |
|[ContactSource](contactsource.md) <br/> |Beschreibt, ob der Kontakt in der Exchange-Speicher oder in Active Directory-Domänendienste (AD DS) gespeichert ist.  <br/> |
|[Elemente des Objekts (MemberListType)](members-memberlisttype.md) <br/> |Enthält eine Liste der Mitglieder der Verteilerliste.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten an eine einzelne Eigenschaft einer Verteilerliste während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Identifiziert eine Verteilerliste im lokalen Client-Speicher zu erstellen.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifiziert eine Verteilerliste, die in den Speicher des lokalen Client aktualisiert.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen an.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in den Ordner vom [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) -Element zu erstellen.  <br/> |
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Listenelements Verteilung in einer [UpdateItem Vorgang](updateitem-operation.md)dar.  <br/> |
   
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

