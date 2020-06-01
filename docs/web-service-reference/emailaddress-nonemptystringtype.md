---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: Das Address-Element definiert die primäre SMTP-Adresse eines Postfachbenutzers.
ms.openlocfilehash: fcc3e650d5fc32344022ed6f015d4096a4461f63
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463132"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

Das Address **-Element definiert die primäre** SMTP-Adresse eines Postfachbenutzers. 
  
```XML
<EmailAddress/>
```

 **NonEmptyStringType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Actingies](actingas.md) <br/> |Gibt an, wen der Anrufer sendet.  <br/> |
|[Postfach](mailbox.md) <br/> | Identifiziert eine vollständig aufgelöste e-Mail-Adresse.  <br/><br/>Im folgenden finden Sie einige XPath-Ausdrücke für dieses Element:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>Im folgenden sind zusätzliche übergeordnete Elemente des Mailbox-Elements angegeben:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [Absender](sender.md) <br/>- [Von](from.md) <br/>- [Organisator](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [Lösung](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Teilnehmer](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Identifiziert eine Liste von Besprechungsräumen per e-Mail-Adresse.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.
  
## <a name="remarks"></a>Bemerkungen

Das **Address** -Element kann SMTP-oder Legacy-Exchange Distinguished Name (auch als DN bekannt)-Adressen darstellen. Das Element " **Email** " ist das einzige erforderliche [Post Fach](mailbox.md) Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

