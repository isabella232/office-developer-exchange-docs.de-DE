---
title: GlobalIconIndex
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 3d28ed70-4cfe-46e4-8d15-593c6e355bcf
description: Das GlobalIconIndex-Element identifiziert den globalen Symbolindex für alle Elemente in einer Unterhaltung.
ms.openlocfilehash: 1f88f3627d24c720dbf3dd7036a7f60a9efeddcc
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59519639"
---
# <a name="globaliconindex"></a>GlobalIconIndex

Das **GlobalIconIndex-Element** identifiziert den globalen Symbolindex für alle Elemente in einer Unterhaltung. 
  
```XML
<IconIndex>Default | PostItem | MailRead | MailUnread | MailReplied | MailForwarded | MailEncrypted | MailSmimeSigned | MailEncrytedReplied | MailSmimeSignedReplied | MailEncryptedForwarded | MailSmimeSignedForwarded | MailEncryptedRead | MailSmimeSignedRead | MailIrm | MaillrmForwarded | MaillrmReplied | SmsSubmitted | SmsRoutedToDeliveryPoint | SmsRoutedToExternalMessagingSystem | SmsDelivered | OutlookDefaultForContacts | AppointmentItem | AppointmentRecur | AppointmentMeet | AppointmentMeetRecur | AppointmentMeetNY | AppointmentMeetYes | AppointmentMeetNo | AppointmentMeetMaybe | AppointmentMeetCancel | AppointmentMeetInfo | TaskItem | TaskRecur | TaskOwned | TaskDelegated</IconIndex>
```

 **IconIndexType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[Unterhaltung (ConversationType)](conversation-conversationtype.md)  |  [Element](item.md)  |  [Kontakt](contact.md)  |  [DistributionList](distributionlist.md)  |  [Nachricht](message-ex15websvcsotherref.md)  |  [CalendarItem](calendaritem.md)  |  [PostItem](postitem.md)  |  [Aufgabe](task.md)
  
## <a name="text-value"></a>Textwert

Die folgende Tabelle enthält die möglichen Textwerte für das **GlobalIconIndex-Element.** 
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|||
|Standard  <br/> |Gibt das Standardsymbol an.  <br/> |
|PostItem  <br/> |Gibt das Symbol für ein Beitragselement an.  <br/> |
|MailRead  <br/> |Gibt das Symbol zum Lesen von E-Mails an.  <br/> |
|MailUnread  <br/> |Gibt das ungelesene E-Mail-Symbol an.  <br/> |
|MailReplied  <br/> |Gibt das Symbol für die Antwort auf E-Mail an.  <br/> |
|MailForwarded  <br/> |Gibt das Symbol für weitergeleitete E-Mails an.  <br/> |
|MailEncrypted  <br/> |Gibt das verschlüsselte E-Mail-Symbol an.  <br/> |
|MailSmimeSigned  <br/> |Gibt das S/MIME-Signierte E-Mail-Symbol (Secure/Multipurpose Internet Mail Extensions) an.  <br/> |
|MailEncryptedReplied  <br/> |Gibt das symbol für verschlüsselte Antworten auf E-Mails an.  <br/> |
|MailSmimeSignedReplied  <br/> |Gibt das S/MIME-Symbol an, auf das mit E-Mail-Antworten geantwortet wird.  <br/> |
|MailEncryptedForwarded  <br/> |Gibt das symbol für verschlüsselte weitergeleitete E-Mails an.  <br/> |
|MailSmimeSignedForwarded  <br/> |Gibt das S/MIME-Symbol für signierte weitergeleitete E-Mails an.  <br/> |
|MailEncryptedRead  <br/> |Gibt das verschlüsselte Lese-E-Mail-Symbol an.  <br/> |
|MailSmimeSignedRead  <br/> |Gibt das mit S/MIME signierte Lese-E-Mail-Symbol an.  <br/> |
|MailIrm  <br/> |Gibt das IRM-geschützte E-Mail-Symbol an.  <br/> |
|MailIrmForwarded  <br/> |Gibt das IRM-geschützte Symbol für weitergeleitete E-Mails an.  <br/> |
|MailIrmReplied  <br/> |Gibt das IRM-geschützte Symbol für antwortende E-Mails an.  <br/> |
|SmsSubmitted  <br/> |Gibt das Symbol für E-Mails an, die für sms-Routing (Short Message Service) übermittelt werden.  <br/> |
|SmsRoutedToDeliveryPoint  <br/> |Gibt das Symbol für das SMS-Routing an einen externen Zustellungspunkt an.  <br/> |
|SmsRoutedToExternalMessagingSystem  <br/> |Gibt das Symbol für das SMS-Routing an ein externes Messagingsystem an.  <br/> |
|Zugestellte SMS  <br/> |Gibt das Symbol für zugestellte SMS-E-Mails an.  <br/> |
|OutlookDefaultForContacts  <br/> |Gibt das Standardsymbol für Kontakte an.  <br/> |
|AppointmentItem  <br/> |Gibt das Symbol für das Terminelement an.  <br/> |
|AppointmentRecur  <br/> |Gibt das Terminseriensymbol an.  <br/> |
|AppointmentMeet  <br/> |Gibt das Besprechungssymbol an.  <br/> |
|AppointmentMeetRecur  <br/> |Gibt das Symbol für Besprechungsserien an.  <br/> |
|AppointmentMeetNY  <br/> |Gibt das Symbol für eine Mit Vorbehaltsantwort auf die Besprechung an.  <br/> |
|AppointmentMeetYes  <br/> |Gibt das Symbol für die Besprechungsakzeptanz an.  <br/> |
|AppointmentMeetNo  <br/> |Gibt das Symbol "Besprechung abgelehnt" an.  <br/> |
|AppointmentMeetMaybe  <br/> |Gibt das Symbol für eine vielleicht Antwort auf die Besprechung an.  <br/> |
|AppointmentMeetCancel  <br/> |Gibt das Symbol zum Abbrechen einer Besprechung an.  <br/> |
|AppointmentMeetInfo  <br/> |Gibt das Symbol für Besprechungsinformationen an.  <br/> |
|TaskItem  <br/> |Gibt das Aufgabenelementsymbol an.  <br/> |
|TaskRecur  <br/> |Gibt das Symbol für wiederkehrende Aufgaben an.  <br/> |
|TaskOwned  <br/> |Gibt das Symbol im Besitz des Vorgangs an.  <br/> |
|TaskDelegated  <br/> |Gibt das Symbol "Aufgabe delegiert" an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

