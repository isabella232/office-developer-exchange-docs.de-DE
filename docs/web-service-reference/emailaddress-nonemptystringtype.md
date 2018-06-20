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
description: Das EmailAddress-Element definiert die primäre SMTP-Adresse eines Postfachbenutzers an.
ms.openlocfilehash: fcf2839c1e2e40a22d6b6a856608f52f2c9c2a1a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758165"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

Das **EmailAddress** -Element definiert die primäre SMTP-Adresse eines Postfachbenutzers an. 
  
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
|[ActingAs](actingas.md) <br/> |Identifiziert, die der Anrufer als sendet.  <br/> |
|[Postfach](mailbox.md) <br/> | Identifiziert eine vollständig aufgelöster E-mail-Adresse.  <br/><br/>Im folgenden sind einige XPath-Ausdrücke auf dieses Element:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>Im folgenden sind zusätzliche übergeordnete Elemente des Postfach-Elements:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [ReplyTo](replyto.md) <br/>- [Absender](sender.md) <br/>- [Von](from.md) <br/>- [Organizer](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [Lösung](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Teilnehmer](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Eine Liste der Besprechungsräumen von e-Mail-Adresse identifiziert.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.
  
## <a name="remarks"></a>Hinweise

Das **EmailAddress** -Element kann SMTP darstellen oder legacy-Exchange-distinguished Name (DN)-Adressen. Das **EmailAddress** -Element ist das einzige erforderliche [Postfach](mailbox.md) -Element. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

