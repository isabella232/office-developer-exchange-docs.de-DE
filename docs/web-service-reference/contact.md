---
title: Kontakt
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Contact
api_type:
- schema
ms.assetid: 66bfff50-7a91-4d81-b6a0-610b9962f677
description: Das Contact-Element stellt ein Kontaktelement im Exchange-Informationsspeicher dar.
ms.openlocfilehash: b5b4af211815dbbd09449ca2f3c6b6b2dfba6f93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44445650"
---
# <a name="contact"></a>Kontakt

Das **Contact** -Element stellt ein Kontaktelement im Exchange-Informationsspeicher dar. 
  
```XML
<Contact>
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
   <FileAs/>
   <FileAsMapping/>
   <DisplayName/>
   <GivenName/>
   <Initials/>
   <MiddleName/>
   <Nickname/>
   <CompleteName/>
   <CompanyName/>
   <EmailAddresses/>
   <PhysicalAddresses/>
   <PhoneNumbers/>
   <AssistantName/>
   <Birthday/>
   <BusinessHomePage/>
   <Children/>
   <Companies/>
   <ContactSource/>
   <Department/>
   <Generation/>
   <ImAddresses/>
   <JobTitle/>
   <Manager/>
   <Mileage/>
   <OfficeLocation/>
   <PostalAddressIndex/>
   <Profession/>
   <SpouseName/>
   <Surname/>
   <WeddingAnniversary/>
   <HasPicture/>
   <PhoneticFullName/>
   <PhoneticFirstName/>
   <PhoneticLastName/>
   <Alias/>
   <Notes/>
   <Photo/>
   <UserSMIMECertificate/>
   <MSExchangeCertificate/>
   <DirectoryId/>
   <ManagerMailbox/>
   <DirectReports/>
</Contact>
```

 **ContactItemType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Elementname**|**Beschreibung**|
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
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen dar, die ermitteln, zu welchen Kategorien ein Element im Postfach gehört.  <br/> |
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
|[DisplayCc](displaycc.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt der CC-Zeile verwendet wird. Dies ist die verkettete Zeichenfolge aller Anzeigenamen des CC-Empfängers.  <br/> |
|[Displayto ursprünglicher](displayto.md) <br/> |Stellt die Anzeigezeichenfolge dar, die für den Inhalt der an-Verbindung verwendet wird. Dies ist die verkettete Zeichenfolge aller in Empfänger Anzeigenamen.  <br/> |
|[HasAttachments](hasattachments.md) <br/> |Stellt eine Eigenschaft dar, die auf **true** festgelegt ist, wenn ein Element mindestens eine sichtbare Anlage aufweist. Diese Eigenschaft ist schreibgeschützt.  <br/> |
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
|[FileAs](fileas.md) <br/> |Stellt dar, wie ein Kontakt im Ordner Kontakte gespeichert wird.  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |Definiert, wie die für einen Kontakt angezeigte Anzeige erstellt wird.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Kontakts.  <br/> |
|[GivenName](givenname.md) <br/> |Enthält den angegebenen Namen des Kontakts.  <br/> |
|[Initialen](initials.md) <br/> |Stellt die Initialen eines Kontakts dar.  <br/> |
|[MiddleName](middlename.md) <br/> |Stellt den zweiten Vornamen eines Kontakts dar.  <br/> |
|[Spitzname](nickname.md) <br/> |Stellt den Spitznamen eines Kontakts dar.  <br/> |
|[Completename](completename.md) <br/> |Stellt den vollständigen Namen eines Kontakts dar.  <br/> |
|[CompanyName](companyname.md) <br/> |Stellt den Firmennamen dar, der einem Kontakt zugeordnet ist.  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |Stellt eine Auflistung von e-Mail-Adressen für einen Kontakt dar.  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |Enthält eine Auflistung von physikalischen Adressen, die einem Kontakt zugeordnet sind.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.  <br/> |
|[AssistantName](assistantname.md) <br/> |Stellt einen Assistenten für einen Kontakt dar.  <br/> |
|[Birthday](birthday.md) <br/> |Stellt das Geburtsdatum eines Kontakts dar.  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |Stellt die Startseite (Webadresse) für den Kontakt dar.  <br/> |
|[Children](children.md) <br/> |Enthält die Namen der untergeordneten Elemente eines Kontakts.  <br/> |
|[Companies](companies.md) <br/> |Stellt die Auflistung von Unternehmen dar, die einem Kontakt zugeordnet sind.  <br/> |
|[ContactSource](contactsource.md) <br/> |Beschreibt, ob sich der Kontakt im Exchange-Informationsspeicher oder im Active Directory Verzeichnisdienst befindet.  <br/> |
|[Department](department.md) <br/> |Stellt die Abteilung des Kontakts bei der Arbeit dar.  <br/> |
|[Erzeugung](generation.md) <br/> |Stellt eine Generierungs Abkürzung dar, die dem vollständigen Namen eines Kontakts folgt.  <br/> |
|[Imaddresses](imaddresses.md) <br/> |Stellt eine Auflistung von Instant Messaging-Adressen für einen Kontakt dar.  <br/> |
|[JobTitle](jobtitle.md) <br/> |Stellt die Position eines Kontakts dar.  <br/> |
|[Manager](manager.md) <br/> |Stellt den Vorgesetzten eines Kontakts dar.  <br/> |
|[Mileage](mileage.md) <br/> |Stellt die Kilometerleistung für ein Kontaktelement dar.  <br/> |
|[OfficeLocation](officelocation.md) <br/> |Stellt die Office-Position eines Kontakts dar.  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |Stellt die Anzeigetypen für physikalische Adressen dar.  <br/> |
|[Profession](profession.md) <br/> |Stellt den Beruf eines Kontakts dar.  <br/> |
|[Ehepartnername](spousename.md) <br/> |Stellt den Namen des Ehepartners/Partners eines Kontakts dar.  <br/> |
|[Nachname](surname.md) <br/> |Steht für den Namen eines Kontakts.  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |Enthält das Hochzeitsjubiläum eines Kontakts.  <br/> |
|[HasPicture](haspicture.md) <br/> |Gibt an, ob das Kontaktelement über eine Dateianlage verfügt, die das Bild des Kontakts darstellt.  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |Enthält den vollständigen Namen eines Kontakts, einschließlich des vor-und Nachnamens, phonetisch buchstabiert.  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |Enthält den Vornamen eines Kontakts, der phonetisch buchstabiert ist.  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |Enthält den Nachnamen eines Kontakts, der phonetisch buchstabiert ist.  <br/> |
|[Alias](alias.md) <br/> |Enthält den e-Mail-Alias eines Kontakts.  <br/> |
|[Hinweise (Kontakt)](notes-contact.md) <br/> |Enthält zusätzliche Kontaktinformationen.  <br/> |
|[Foto](photo.md) <br/> |Enthält einen Wert, der das Foto eines Kontakts codiert.  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |Enthält einen Wert, der das SMIME-Zertifikat eines Kontakts codiert.  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |Enthält einen Wert, der das Microsoft Exchange Zertifikat eines Kontakts codiert.  <br/> |
|[Verzeichnis-Nr](directoryid.md) <br/> |Enthält die Verzeichnis-ID eines Kontakts.  <br/> |
|[Manager Mailbox](managermailbox.md) <br/> |Enthält SMTP-Informationen, die das Manager Postfach des Kontakts identifizieren.  <br/> |
|[DirectReports](directreports.md) <br/> |Enthält SMTP-Informationen, die die direkten Berichte eines Kontakts identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Beschreibt alle Kalenderelemente, die an eine Besprechungszeit angrenzen.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements oder Ordners angefügt werden sollen.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einer Besprechungszeit in Konflikt stehen.  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Gibt einen einzelnen Ordner an, der im lokalen Clientspeicher erstellt werden soll.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element dar, das an ein anderes Exchange-Element angefügt ist.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen, die in dem Ordner erstellt werden sollen, der durch das [parentfolderid (TargetFolderIdType)-](parentfolderid-targetfolderidtype.md) Element identifiziert wird.  <br/> |
|[Lösung](resolution.md) <br/> |Enthält eine einzelne aufgelöste Entität.  <br/> |
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](https://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Aktualisieren von Kontakten](https://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Deleting Contacts](https://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

