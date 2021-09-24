---
title: EmailAddress (NonEmptyStringType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.localizationpriority: medium
api_name:
- EmailAddress
api_type:
- schema
ms.assetid: c0c708d1-b016-4902-a294-9af44aea2050
description: Das EmailAddress-Element definiert die primäre SMTP-Adresse eines Postfachbenutzers.
ms.openlocfilehash: 8740f6f7f67269de86aaa7383a7ad8f3cdf07a4a
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59512996"
---
# <a name="emailaddress-nonemptystringtype"></a>EmailAddress (NonEmptyStringType)

Das **EmailAddress-Element** definiert die primäre SMTP-Adresse eines Postfachbenutzers. 
  
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
|[ActingAs](actingas.md) <br/> |Gibt an, an wen der Anrufer gesendet wird.  <br/> |
|[Postfach](mailbox.md) <br/> | Identifiziert eine vollständig aufgelöste E-Mail-Adresse.  <br/><br/>Im Folgenden sind einige XPath-Ausdrücke für dieses Element aufgeführt:<br/><br/>`/CreateItem/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`/CreateFolder/ParentFolderId/DistinguishedFolderId/Mailbox`<br/><br/>`CreateItem/Items/AcceptItem/ToRecipients/Mailbox`<br/><br/>`SyncFolderItemsResponseMessage/Changes/Create/CalendarItem/ConflictingMeetings/AcceptItem/CcRecipients/Mailbox`<br/><br/>Nachfolgend finden Sie weitere übergeordnete Elemente des Mailbox-Elements:<br/><br/>- [BccRecipients](bccrecipients.md) <br/>- [Replyto](replyto.md) <br/>- [Absender](sender.md) <br/>- [Von](from.md) <br/>- [Veranstalter](organizer.md) <br/>- [DistinguishedFolderId](distinguishedfolderid.md) <br/>- [Auflösung](resolution.md) <br/>- [DLExpansion](dlexpansion.md) <br/>- [Teilnehmer](attendee.md) <br/> |
|[RoomList](roomlist.md) <br/> |Identifiziert eine Liste von Besprechungsräumen nach E-Mail-Adresse.  <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert, der eine SMTP-Adresse darstellt, ist erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **EmailAddress-Element** kann SMTP- oder Legacy-Exchange Distinguished Name -Adressen (auch als DN bezeichnet) darstellen. Das **EmailAddress-Element** ist das einzige erforderliche [Mailbox-Element.](mailbox.md) 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   

