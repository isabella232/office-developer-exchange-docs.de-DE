---
title: PostItem
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PostItem
api_type:
- schema
ms.assetid: 7727ed84-9591-4a1c-bb04-12129926499b
description: Das PostItem-Element stellt ein Post-Element im Exchange-Informationsspeicher dar.
ms.openlocfilehash: 5fba1a9a6a3abc95ea2ce65cafa2b62bc7423f28
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44528867"
---
# <a name="postitem"></a>PostItem

Das **PostItem** -Element stellt ein Post-Element im Exchange-Informationsspeicher dar. 
  
```xml
<PostItem>
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
   <ConversationIndex/>
   <ConversationTopic/>
   <From/>
   <InternetMessageId/>
   <IsRead/>
   <PostedTime/>
   <References/>
   <Sender/>
</PostItem>
```

 **PostItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MimeContent](mimecontent.md) <br/> |Enthält den systemeigenen Multipurpose Internet Mail Extensions (MIME) Stream eines Objekts, das im base64Binary-Format dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ParentFolderId](parentfolderid.md) <br/> |Stellt den Bezeichner des übergeordneten Ordners dar, der das Element oder den Ordner enthält. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ItemClass](itemclass.md) <br/> |Stellt die Nachrichtenklasse eines Elements dar.  <br/> |
|[Betreff](subject.md) <br/> |Stellt den Betreff für Exchange-Informationsspeicher Elemente und Response-Objekte dar. Der Betreff ist auf 255 Zeichen limitiert.  <br/> |
|[Sensitivity](sensitivity.md) <br/> |Gibt die Empfindlichkeitsstufe eines Elements an.  <br/> |
|[Body](body.md) <br/> |Stellt den tatsächlichen Textinhalt einer Nachricht dar.  <br/> |
|[Anlagen](attachments-ex15websvcsotherref.md) <br/> |Enthält die Elemente oder Dateien, die an ein Element im Exchange-Informationsspeicher angefügt sind.  <br/> |
|[DateTimeReceived](datetimereceived.md) <br/> |Stellt das Datum und die Uhrzeit dar, zu denen ein Element in einem Postfach empfangen wurde.  <br/> |
|[Größe](size.md) <br/> |Stellt die Größe eines Elements in Bytes dar. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen dar, die die Kategorien identifizieren, zu denen ein Element im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Wichtigkeit eines Elements.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements dar, zu dem dieses Element eine Antwort ist.  <br/> |
|[Issubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element an den Standardordner Postausgang übermittelt wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Stellt dar, ob ein Element noch nicht gesendet wurde.  <br/> |
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
|[DisplayCc](displaycc.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds CC verwendet wird. Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.  <br/> |
|[Displayto ursprünglicher](displayto.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt des Felds an verwendet wird. Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine Anlage aufweist. Diese Eigenschaft ist schreibgeschützt.  <br/> |
|[ExtendedProperty](extendedproperty.md) <br/> |Erweiterte Eigenschaften für Ordner und Elemente identifiziert.  <br/> |
|[Kultur](culture.md) <br/> |Stellt die Kultur für ein bestimmtes Element in einem Postfach dar.  <br/> |
|[EffectiveRights](effectiverights.md) <br/> |Enthält die Rechte des Clients basierend auf den Berechtigungseinstellungen für das Element oder den Ordner. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des letzten Benutzers, der ein Element ändern soll.  <br/> |
|[LastModifiedTime](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[Isassociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Microsoft Office Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL dar, die mit dem Outlook Web App-Endpunkt verkettet werden soll, um ein Element in Outlook Web App zu bearbeiten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält den Bezeichner eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.  <br/> |
|[ConversationIndex](conversationindex.md) <br/> |Enthält eine binäre ID, die den Thread darstellt, zu dem diese Nachricht gehört.  <br/> |
|[ConversationTopic](conversationtopic.md) <br/> |Stellt den Konversationsbezeichner dar.  <br/> |
|[From](from.md) <br/> |Stellt die Adresse dar, von der das Post-Element gesendet wurde. Das **from** -Element kann nur zum Zeitpunkt der Erstellung festgelegt werden.  <br/> |
|[InternetMessageId](internetmessageid.md) <br/> |Stellt die Internet Nachrichten-ID eines Elements dar.  <br/> |
|[IsRead](isread.md) <br/> |Gibt an, ob eine Nachricht gelesen wurde.  <br/> |
|[Gebucht](postedtime.md) <br/> |Stellt die Uhrzeit dar, zu der ein [PostItem](postitem.md) bereitgestellt wurde.  <br/> |
|[References](references.md) <br/> |Stellt den Usenet-Header dar, der zum Zuordnen von Antworten zu den ursprünglichen Nachrichten verwendet wird.  <br/> |
|[Absender](sender.md) <br/> |Bezeichnet den Absender eines Elements.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SetItemField](setitemfield.md) <br/> |Stellt eine Aktualisierung einer einzelnen Eigenschaft eines Elements in einer UpdateItem-Operation dar.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements oder Ordners angefügt werden sollen.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[Update (ItemSync)](update-itemsync.md) <br/> |Identifiziert ein einzelnes Element, das im lokalen Clientspeicher aktualisiert werden soll.  <br/> |
|[ReadFlagChange](readflagchange.md) <br/> |Wird in [SyncFolderItems](syncfolderitems.md) -Antworten zurückgegeben, wenn ein Element gelesen wurde. Diese Eigenschaft ist schreibgeschützt. Dieses Element wurde in Exchange 2007 SP1 eingeführt.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.  <br/> |
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
   
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

