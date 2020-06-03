---
title: IconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 92020822-2a86-4dfc-aee1-3067af4d4edf
description: Das IconIndex-Element identifiziert den Symbolindex für ein Element oder eine Unterhaltung.
ms.openlocfilehash: 0f932f5632422a8786e74500bf83cb1337f780c3
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460785"
---
# <a name="iconindex"></a>IconIndex

Das **IconIndex** -Element identifiziert den Symbolindex für ein Element oder eine Unterhaltung. 
  
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

Unter [Haltung (conversationtype)](conversation-conversationtype.md)  |  [Element](item.md)  |  [Kontaktinformationen](contact.md)  |  [Verteilerliste](distributionlist.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Text Werte für das **IconIndex** -Element. 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|||
|Standard  <br/> |Gibt das Standardsymbol an.  <br/> |
|PostItem  <br/> |Gibt das Symbol für ein Beitrags Element an.  <br/> |
|Mailread  <br/> |Gibt das Symbol e-Mail-Lesezugriff an.  <br/> |
|MailUnread  <br/> |Gibt das Symbol für ungelesene Nachrichten an.  <br/> |
|Mailantwortete  <br/> |Gibt das Antwort-e-Mail-Symbol an.  <br/> |
|Mailforwarded  <br/> |Gibt das Symbol weitergeleitete e-Mail an.  <br/> |
|Mailencrypted  <br/> |Gibt das verschlüsselte e-Mail-Symbol an.  <br/> |
|MailSmimeSigned  <br/> |Gibt das Symbol Secure/Multipurpose Internet Mail Extensions (S/MIME) signierten e-Mail an.  <br/> |
|MailEncryptedReplied  <br/> |Gibt das verschlüsselte Antwort-e-Mail-Symbol an.  <br/> |
|MailSmimeSignedReplied  <br/> |Gibt das signierte S/MIME-Symbol für Antworten auf e-Mail an.  <br/> |
|MailEncryptedForwarded  <br/> |Gibt das Symbol für verschlüsselte weitergeleitete e-Mails an.  <br/> |
|MailSmimeSignedForwarded  <br/> |Gibt das Symbol S/MIME signiert weitergeleitete e-Mails an.  <br/> |
|MailEncryptedRead  <br/> |Gibt das verschlüsselte Symbol "e-Mail lesen" an.  <br/> |
|MailSmimeSignedRead  <br/> |Gibt das Symbol S/MIME signierte Nachrichten lesen an.  <br/> |
|MailIrm  <br/> |Gibt das Symbol für die Verwaltung von Informationsrechten (IRM)-geschützter e-Mail an.  <br/> |
|MailIrmForwarded  <br/> |Gibt das Symbol für IRM-geschützte weitergeleitete Nachrichten an.  <br/> |
|MailIrmReplied  <br/> |Gibt das IRM-geschützte Antwort-e-Mail-Symbol an.  <br/> |
|SmsSubmitted  <br/> |Gibt das Symbol an, das für das SMS-Routing (Short Message Service) gesendet wurde.  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Gibt das Symbol für das SMS-Routing an einen externen Zustellungspfad an.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Gibt das Symbol für die SMS-Weiterleitung an ein externes Messagingsystem an.  <br/> |
|SmsDelivered  <br/> |Gibt das Symbol für die SMS-Zustellung an.  <br/> |
|OutlookDefaultForContacts  <br/> |Gibt das Standardsymbol für Kontakte an.  <br/> |
|AppointmentItem  <br/> |Gibt das Symbol für das Terminelement an.  <br/> |
|AppointmentRecur  <br/> |Gibt das Symbol für Terminserien Termine an.  <br/> |
|AppointmentMeet  <br/> |Gibt das Besprechungssymbol an.  <br/> |
|AppointmentMeetRecur  <br/> |Gibt das Symbol für Besprechungsserien an.  <br/> |
|AppointmentMeetNY  <br/> |Gibt das Symbol für eine vorläufige Antwort an die Besprechung an.  <br/> |
|AppointmentMeetYes  <br/> |Gibt das Symbol für die Besprechungs Akzeptanz an.  <br/> |
|AppointmentMeetNo  <br/> |Gibt das Symbol für Besprechungsablehnung an.  <br/> |
|AppointmentMeetMaybe  <br/> |Gibt das Symbol für eine eventuelle Antwort auf die Besprechung an.  <br/> |
|AppointmentMeetCancel  <br/> |Gibt das Symbol für das Besprechungs Abbruch an.  <br/> |
|AppointmentMeetInfo  <br/> |Gibt das Symbol für die Besprechungsinformationen an.  <br/> |
|TaskItem  <br/> |Gibt das Aufgabenelement Symbol an.  <br/> |
|TaskRecur  <br/> |Gibt das Symbol für wiederkehrende Aufgaben an.  <br/> |
|TaskOwned  <br/> |Gibt das Symbol für den Aufgaben Besitz an.  <br/> |
|TaskDelegated  <br/> |Gibt das Symbol Aufgabe delegiertes an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   

