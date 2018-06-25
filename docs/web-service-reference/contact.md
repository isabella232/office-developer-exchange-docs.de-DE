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
description: Das Kontakt-Element stellt ein Kontaktelement im Exchange-Speicher.
ms.openlocfilehash: 7b2e7c0197914c2a0a0ba3815dd05fca52a5f872
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757615"
---
# <a name="contact"></a>Kontakt

**Wenden Sie sich an** -Element stellt ein Kontaktelement im Exchange-Speicher. 
  
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
|[Kategorien](categories-ex15websvcsotherref.md) <br/> |Stellt eine Auflistung von Zeichenfolgen, die identifizieren, welche, die Kategorien ein Elements im Postfach gehört.  <br/> |
|[Importance](importance.md) <br/> |Beschreibt die Bedeutung eines Elements an.  <br/> |
|[InReplyTo](inreplyto.md) <br/> |Stellt den Bezeichner des Elements, der dieses Element eine Antwort ist.  <br/> |
|[IsSubmitted](issubmitted.md) <br/> |Gibt an, ob ein Element in den Standardordner Postausgang gesendet wurde.  <br/> |
|[IsDraft](isdraft.md) <br/> |Stellt dar, ob ein Element noch nicht gesendet wurde.  <br/> |
|[IsFromMe](isfromme.md) <br/> |Gibt an, ob ein Benutzer ein Element auf sich selbst gesendet.  <br/> |
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
|[EffectiveRights](effectiverights.md) <br/> |Der Client Rechte basierend auf den berechtigungseinstellungen für das Element oder Ordner enthält. Dieses Element ist schreibgeschützt.  <br/> |
|[LastModifiedName](lastmodifiedname.md) <br/> |Enthält den Anzeigenamen des Benutzers auf ein Element zu ändern.  <br/> |
|[ZuletztGeändertUm](lastmodifiedtime.md) <br/> |Gibt an, wann ein Element zuletzt geändert wurde.  <br/> |
|[IsAssociated](isassociated.md) <br/> |Gibt an, ob das Element einem Ordner zugeordnet ist.  <br/> |
|[WebClientReadFormQueryString](webclientreadformquerystring.md) <br/> |Stellt eine URL zu verketten an den Microsoft Office Outlook Web App-Endpunkt ein Elements in Outlook Web App zu lesen.  <br/> |
|[WebClientEditFormQueryString](webclienteditformquerystring.md) <br/> |Stellt eine URL an den Endpunkt Outlook Web App so bearbeiten Sie ein Element in Outlook Web App verketten.  <br/> |
|[ConversationId](conversationid.md) <br/> |Enthält die ID eines Elements oder einer Unterhaltung.  <br/> |
|[UniqueBody](uniquebody.md) <br/> |Stellt ein HTML-Fragment oder nur-Text, der den eindeutigen Text an dieser Unterhaltung darstellt.  <br/> |
|[FileAs](fileas.md) <br/> |Stellt dar, wie ein Kontakt im Ordner Kontakte vorgebracht wurde.  <br/> |
|[FileAsMapping](fileasmapping.md) <br/> |Definiert, wie erstellen, was für einen Kontakt angezeigt wird.  <br/> |
|[DisplayName (Zeichenfolge)](displayname-string.md) <br/> |Definiert den Anzeigenamen eines Kontakts an.  <br/> |
|[Vorname](givenname.md) <br/> |Enthält den Namen eines Kontakts angegebenen.  <br/> |
|[Initialen](initials.md) <br/> |Stellt die Initialen eines Kontakts an.  <br/> |
|[MiddleName](middlename.md) <br/> |Stellt den Vornamen eines Kontakts an.  <br/> |
|[Spitzname](nickname.md) <br/> |Stellt den Spitznamen eines Kontakts an.  <br/> |
|[CompleteName](completename.md) <br/> |Stellt den vollständigen Namen eines Kontakts an.  <br/> |
|[Firma](companyname.md) <br/> |Stellt den Firmennamen, der einem Kontakt zugeordnet ist.  <br/> |
|[EmailAddresses](emailaddresses.md) <br/> |Stellt eine Auflistung von E-mail-Adressen für einen Kontakt.  <br/> |
|[PhysicalAddresses](physicaladdresses.md) <br/> |Enthält eine Auflistung von physischen Adressen, die mit einem Kontakt verknüpft sind.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Stellt eine Auflistung von Telefonnummern für einen Kontakt.  <br/> |
|[AssistantName](assistantname.md) <br/> |Stellt dar, wenn ein Assistent einen Kontakt.  <br/> |
|[Birthday](birthday.md) <br/> |Stellt das Geburtsdatum eines Kontakts an.  <br/> |
|[BusinessHomePage](businesshomepage.md) <br/> |Die Homepage (Webadresse) für den Kontakt darstellt.  <br/> |
|[Children](children.md) <br/> |Enthält die Namen der untergeordneten Elemente eines Kontakts.  <br/> |
|[Companies](companies.md) <br/> |Stellt die Auflistung der Unternehmen, die mit einem Kontakt verknüpft sind.  <br/> |
|[ContactSource](contactsource.md) <br/> |Beschreibt, ob der Kontakt in der Exchange-Speicher oder den Active Directory-Verzeichnisdienst befindet.  <br/> |
|[Department](department.md) <br/> |Stellt die Abteilung des Kontakts im Büro.  <br/> |
|[Generierung](generation.md) <br/> |Stellt eine generationsbasierten Abkürzung, die den vollständigen Namen eines Kontakts bildet.  <br/> |
|[ImAddresses](imaddresses.md) <br/> |Stellt eine Auflistung von instant messaging-Adressen für einen Kontakt.  <br/> |
|[JobTitle](jobtitle.md) <br/> |Stellt die Position eines Kontakts an.  <br/> |
|[Manager](manager.md) <br/> |Stellt einen Kontakt-Manager.  <br/> |
|[Mileage](mileage.md) <br/> |Mileage ein Kontaktelement darstellt.  <br/> |
|[OfficeLocation](officelocation.md) <br/> |Stellt den Bürostandort eines Kontakts an.  <br/> |
|[PostalAddressIndex](postaladdressindex.md) <br/> |Stellt die Anzeigetypen für physikalische Adressen an.  <br/> |
|[Profession](profession.md) <br/> |Stellt den Beruf eines Kontakts an.  <br/> |
|[SpouseName](spousename.md) <br/> |Stellt den Namen des eines Kontakts Partner/in.  <br/> |
|[Nachname](surname.md) <br/> |Stellt den Nachnamen eines Kontakts an.  <br/> |
|[WeddingAnniversary](weddinganniversary.md) <br/> |Enthält die Hochzeitstag eines Kontakts an.  <br/> |
|[HasPicture](haspicture.md) <br/> |Gibt an, ob das Kontaktelement eine Dateianlage verfügt, die Bild für den Kontakt darstellt.  <br/> |
|[PhoneticFullName](phoneticfullname.md) <br/> |Enthält den vollständigen Namen eines Kontakts, einschließlich des Namens vor- und Nachname, phonetisch geschrieben.  <br/> |
|[PhoneticFirstName](phoneticfirstname.md) <br/> |Enthält den Vornamen eines Kontakts phonetisch geschrieben.  <br/> |
|[PhoneticLastName](phoneticlastname.md) <br/> |Enthält den Nachnamen eines Kontakts phonetisch geschrieben.  <br/> |
|[Alias](alias.md) <br/> |Enthält den e-Mail-Alias eines Kontakts an.  <br/> |
|[Notizen (Kontakt)](notes-contact.md) <br/> |Zusätzliche Kontaktinformationen enthält.  <br/> |
|[Photo](photo.md) <br/> |Enthält einen Wert, der das Foto des Kontakts codiert.  <br/> |
|[UserSMIMECertificate](usersmimecertificate.md) <br/> |Enthält einen Wert, der das SMIME-Zertifikat eines Kontakts codiert.  <br/> |
|[MSExchangeCertificate](msexchangecertificate.md) <br/> |Enthält einen Wert, der das Microsoft Exchange-Zertifikat eines Kontakts codiert.  <br/> |
|[DirectoryId](directoryid.md) <br/> |Enthält die Verzeichnis-ID eines Kontakts.  <br/> |
|[ManagerMailbox](managermailbox.md) <br/> |Enthält die SMTP-Informationen, die das Postfach Manager des Kontakts zu identifizieren.  <br/> |
|[DirectReports](directreports.md) <br/> |Enthält die SMTP-Informationen, die die direkten Vorgesetzten eines Kontakts zu identifizieren.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Elementname**|**Beschreibung**|
|:-----|:-----|
|[AdjacentMeetings](adjacentmeetings.md) <br/> |Werden alle Kalenderelemente, die an eine Besprechungszeit angrenzen beschrieben.  <br/> |
|[AppendToItemField](appendtoitemfield.md) <br/> |Identifiziert Daten an eine einzelne Eigenschaft eines Elements oder Ordners während eines [Vorgangs UpdateItem](updateitem-operation.md)angefügt.  <br/> |
|[ConflictingMeetings](conflictingmeetings.md) <br/> |Identifiziert alle Elemente, die mit einem bestimmten Zeitpunkt treffen Konflikt  <br/> |
|[Erstellen (ItemSync)](create-itemsync.md) <br/> |Gibt einen einzelnen Ordner im lokalen Client-Speicher zu erstellen.  <br/> |
|[ItemAttachment](itemattachment.md) <br/> |Stellt ein Exchange-Element, das mit einem anderen Exchange-Element zugeordnet ist.  <br/> |
|[Elemente](items.md) <br/> |Enthält ein Array von Elementen an.  <br/> |
|[Elemente (NonEmptyArrayOfAllItemsType)](items-nonemptyarrayofallitemstype.md) <br/> |Enthält ein Array von Elementen im Ordner zu erstellen, die durch das Element [ParentFolderId (TargetFolderIdType)](parentfolderid-targetfolderidtype.md) bezeichnet wird.  <br/> |
|[Lösung](resolution.md) <br/> |Enthält eine einzelne aufgelöste Entität.  <br/> |
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
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)


[Creating Contacts (Exchange Web Services)](http://msdn.microsoft.com/library/4845917e-70d1-481c-bbd7-011ec6571789%28Office.15%29.aspx)
  
[Aktualisierung von Kontakten](http://msdn.microsoft.com/library/9a865953-b94a-4229-b632-2dee433314be%28Office.15%29.aspx)
  
[Deleting Contacts](http://msdn.microsoft.com/library/fcc3dc84-cd3e-455e-a1a7-ae6921c9b588%28Office.15%29.aspx)

