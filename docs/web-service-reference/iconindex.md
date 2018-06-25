---
title: IconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: IconIndex-Element identifiziert den Symbolindex für ein Element oder eine Unterhaltung.
ms.openlocfilehash: 8ada9da2df1cf128009c9b153736b434925f1a3f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829848"
---
# <a name="iconindex"></a>IconIndex

**IconIndex** -Element identifiziert den Symbolindex für ein Element oder eine Unterhaltung. 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MailIrmForwarded | MailIrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Unterhaltung (ConversationType)](conversation-conversationtype.md) | [Element](item.md) | [Kontakt](contact.md) | [DistributionList](distributionlist.md) | [Nachricht](message-ex15websvcsotherref.md) | [CalendarItem](calendaritem.md) | [PostItem](postitem.md) | [Aufgabe ](task.md)
  
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Textwerte für das **IconIndex** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|||
|Standard  <br/> |Gibt das Standardsymbol an.  <br/> |
|PostItem-Objekt  <br/> |Gibt das Symbol für ein Post-Element an.  <br/> |
|MailRead  <br/> |Gibt an, dass die Mail Symbol gelesen.  <br/> |
|MailUnread  <br/> |Gibt das Symbol Ungelesene Nachrichten.  <br/> |
|MailReplied  <br/> |Gibt die beantwortete e-Mail-Symbol an.  <br/> |
|MailForwarded  <br/> |Gibt das weitergeleitete e-Mail-Symbol.  <br/> |
|MailEncrypted  <br/> |Gibt das Symbol für verschlüsselte e-Mails an.  <br/> |
|MailSmimeSigned  <br/> |Gibt das Secure/Multipurpose Internet Mail Extensions (S/MIME) signierten e-Mail-Symbol.  <br/> |
|MailEncryptedReplied  <br/> |Gibt an, die verschlüsselte e-Mail-Symbol geantwortet.  <br/> |
|MailSmimeSignedReplied  <br/> |Gibt an, der S/MIME beantwortete Symbol "Voicemail" angemeldet.  <br/> |
|MailEncryptedForwarded  <br/> |Gibt das Symbol für verschlüsselte weitergeleitete e-Mails an.  <br/> |
|MailSmimeSignedForwarded  <br/> |Gibt an, der S/MIME signiert Symbol "Voicemail" weitergeleitet.  <br/> |
|MailEncryptedRead  <br/> |Gibt das Symbol für verschlüsselte Nachrichten lesen.  <br/> |
|MailSmimeSignedRead  <br/> |Gibt an, der S/MIME signierten e-Mail-Symbol lesen.  <br/> |
|MailIrm  <br/> |Gibt das Information Rights Management, IRM-geschützten e-Mail-Symbol.  <br/> |
|MailIrmForwarded  <br/> |Gibt die IRM-geschützten Symbol "Voicemail" weitergeleitet.  <br/> |
|MailIrmReplied  <br/> |Gibt an, dass die IRM-geschützten e-Mail-Symbol geantwortet.  <br/> |
|SmsSubmitted  <br/> |Gibt die Symbol e-Mail für das routing Short Message Service (SMS) übermittelt.  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Gibt das Symbol für die SMS-Weiterleitung an einen Punkt, externe Zustellung an.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Gibt das Symbol für SMS-routing mit einem externen Messagingsystem an.  <br/> |
|SmsDelivered  <br/> |Gibt das SMS zugestellte e-Mail-Symbol.  <br/> |
|OutlookDefaultForContacts  <br/> |Gibt das Standardsymbol für Kontakte.  <br/> |
|AppointmentItem-Objekts  <br/> |Gibt das Symbol Termin Element an.  <br/> |
|AppointmentRecur  <br/> |Gibt die wiederkehrenden Termin Symbol an.  <br/> |
|AppointmentMeet  <br/> |Gibt das Besprechungssymbol.  <br/> |
|AppointmentMeetRecur  <br/> |Gibt das Symbol für wiederkehrende Besprechung an.  <br/> |
|AppointmentMeetNY  <br/> |Gibt das Symbol für eine mit Vorbehalt Antwort auf die Besprechung an.  <br/> |
|AppointmentMeetYes  <br/> |Gibt an, die Besprechung Annahme-Symbol.  <br/> |
|AppointmentMeetNo  <br/> |Gibt das Besprechungssymbol abgelehnt.  <br/> |
|AppointmentMeetMaybe  <br/> |Gibt das Symbol für eine Antwort möglicherweise zur Besprechung an.  <br/> |
|AppointmentMeetCancel  <br/> |Gibt an, die Besprechung absagen Symbol.  <br/> |
|AppointmentMeetInfo  <br/> |Gibt an, die Besprechung Informationssymbol.  <br/> |
|TaskItem  <br/> |Gibt das Symbol für Element an.  <br/> |
|TaskRecur  <br/> |Gibt das Symbol für wiederkehrende Aufgaben an.  <br/> |
|TaskOwned  <br/> |Gibt die Aufgabe Symbol gehören.  <br/> |
|TaskDelegated  <br/> |Gibt das Symbol für delegierte an.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

