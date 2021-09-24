---
title: Postfach
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Mailbox
api_type:
- schema
ms.assetid: befc70fd-51cb-4258-884c-80c9050f0e82
description: Das Mailbox-Element bezeichnet ein E-Mail-aktiviertes Active Directory-Objekt.
ms.openlocfilehash: 8065c0472c3b847d538422aa77cd93f75d919a9b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59535003"
---
# <a name="mailbox"></a>Postfach

Das **Mailbox**-Element bezeichnet ein E-Mail-aktiviertes Active Directory-Objekt. 
  
```XML
<Mailbox>
   <Name/>
   <EmailAddress/>
   <RoutingType/>
   <MailboxType/>
   <ItemId/>
</Mailbox>
```

**EmailAddressType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (EmailAddressType)](name-emailaddresstype.md) <br/> |Definiert den Namen des Postfachbenutzers. Dieses Element ist optional.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Definiert die Simple Mail Transfer Protocol (SMTP)-Adresse eines Postfachbenutzers. Dieses Element ist optional.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Element ist optional.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Definiert den Postfachtyp eines Postfachbenutzers. Dieses Element ist optional.  <br/> |
|[ItemId](itemid.md) <br/> |Definiert den Elementbezeichner eines Kontakts oder die private Verteilungsliste für Empfänger aus dem Kontaktordner eines Benutzers. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[ExpandDL](expanddl.md) <br/> |Definiert eine Anforderung zum Erweitern einer Verteilerliste. <br/> <br/> Für dieses Element wird folgender XPath-Ausdruck verwendet: ` /ExpandDL ` <br/> |
|[ToRecipients](torecipients.md) <br/> |Enthält eine Reihe von Benutzern eines Elements.  <br/> |
|[CcRecipients](ccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Kopie der Nachricht erhalten.  <br/> |
|[BccRecipients](bccrecipients.md) <br/> |Stellt eine Auflistung der Empfänger dar, die eine Blindkopie (Bcc) einer E-Mail erhalten sollen.  <br/> |
|[ReplyTo](replyto.md) <br/> |Bezeichnet eine Reihe von E-Mail-Adressen, an die Antworten gesendet werden sollen.  <br/> |
|[Absender](sender.md) <br/> |Bezeichnet den Absender eines Elements.  <br/> |
|[Von](from.md) <br/> |Stellt den Adressat dar, der die Nachricht gesendet hat.  <br/> |
|[Organisator](organizer.md) <br/> |Stellt den Organisator einer Besprechung dar.  <br/> |
|[DistinguishedFolderId](distinguishedfolderid.md) <br/> | Bezeichnet die standarmäßigen Microsoft Exchange Server 2007-Ordner.  <br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet: <br/> <br/>  `/CreateItem/ParentFolderId/DistinguishedFolderId` <br/>  `/CreateFolder/ParentFolderId/DistinguishedFolderId` <br/> |
|[Lösung](resolution.md) <br/> |Enthält eine einzelne aufgelöste Entität.  <br/> |
|[DLExpansion](dlexpansion.md) <br/> |Enthält eine Reihe von Postfächern, die in einer Verteilerliste enthalten sind.  <br/> |
|[Attendee](attendee.md) <br/> |Stellt Teilnehmer und Ressourcen für ein Kalenderelement dar.  <br/> |
|[CreateManagedFolder](createmanagedfolder.md) <br/> |Definiert eine Anforderung zum Hinzufügen verwalteter Ordner für ein Postfach.  <br/> |
|[AddDelegate](adddelegate.md) <br/> |Definiert eine Anforderung zum Hinzufügen von Stellvertretern für ein Postfach.  <br/> |
|[GetDelegate](getdelegate.md) <br/> |Definiert eine Anforderung zum Abrufen von Informationen zu Stellvertretern für ein Postfach.  <br/> |
|[RemoveDelegate](removedelegate.md) <br/> |Definiert eine Anforderung zum Entfernen von Stellvertretern aus einem Postfach.  <br/> |
|[UpdateDelegate](updatedelegate.md) <br/> |Definiert eine Anforderung zum Aktualisieren von Stellvertretern in einem Postfach.  <br/> |
|[ReceivedBy](receivedby.md) <br/> |Erläutert den Stellvertreter anhand eines Stellvertreterzugriffsszenarios.  <br/> |
|[ReceivedRepresenting](receivedrepresenting.md) <br/> |Erläutert den Prinzipal anhand eines Stellvertreterzugriffsszenarios.  <br/> |
|[Member](member-ex15websvcsotherref.md) <br/> |Stellt ein Element einer Verteilerliste dar.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)- und [ItemId](itemid.md)-Element bezeichnen ein Postfach oder eine Verteilerliste. 

Das [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)-Element bezeichnet ein Postfach oder eine Verteilerliste anhand der SMTP-Adresse. 

Das [ItemId](itemid.md)-Element bezeichnet ein Postfach anhand eines Elementbezeichners, der einem bestimmten Postfach zugeordnet ist. 

Das [ItemId](itemid.md)-Element kann nicht zum Senden einer Nachricht an eine Verteilerliste oder einen Kontakt in einem öffentlichen Kontaktordner verwendet werden. Wenn es in einem CreateItem-, UpdateItem- oder SendItem-Vorgang verwendet wird, wird beim Versuch eine Nachricht an eine Verteilerliste oder einen öffentlichen Kontaktordner zu senden ein Fehler ausgelöst. Verwenden Sie zum Abrufen der SMTP-Adresse den ExpandDL-Vorgang und senden Sie die Nachricht anschließend mit dem [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)-Element, statt das [ItemId](itemid.md)-Element zu verwenden. 
  
Ein anderes Element, [Postfach (Verfügbarkeit)](mailbox-availability.md), stellt Informationen zu Verfügbarkeitsvorgängen bereit. 
  
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

