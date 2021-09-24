---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: Das AttendeeType-Element stellt den Typ des Teilnehmers dar, der im Email (EmailAddressType)-Element identifiziert wird. Dieses Element wird in Anfragen für Besprechungsvorschläge verwendet.
ms.openlocfilehash: 5bcec50fe6cccc3df48ca9615dbd0d9418211b4b
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533934"
---
# <a name="attendeetype"></a>AttendeeType

Das **AttendeeType-Element** stellt den Typ des Teilnehmers dar, der im [Email (EmailAddressType)-Element](email-emailaddresstype.md) identifiziert wird. Dieses Element wird in Anfragen für Besprechungsvorschläge verwendet. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
- [AttendeeType](attendeetype.md)
  
```xml
<AttendeeType>Organizer or Required or Optional or Room or Resource</AttendeeType>
```

 **MeetingAttendeeType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>Textwert

Für dieses Element ist ein Textwert erforderlich. In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Organisator  <br/> |Der Postfachbenutzer und der Teilnehmer, der das Kalenderelement erstellt hat.  <br/> |
|Erforderlich  <br/> |Ein Postfachbenutzer, der ein erforderlicher Teilnehmer an der Besprechung ist.  <br/> |
|Optional  <br/> |Ein Postfachbenutzer, der ein optionaler Teilnehmer an der Besprechung ist.  <br/> |
|Raum  <br/> |Eine Postfachentität, die eine raumressource darstellt, die für die Besprechung verwendet wird.  <br/> |
|Ressource  <br/> |Eine Ressource, z. B. ein Fernsehgerät oder ein Projektor, der für die Verwendung in der Besprechung geplant ist.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist ein erforderliches untergeordnetes Element des [MailboxData-Elements.](mailboxdata.md) Dieses Element kann im [MailboxData-Element](mailboxdata.md) nur einmal auftreten. Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist. 
  
> [!NOTE]
> Der AttendeeType-Schematyp wird verwendet, um Teilnehmer für ein Kalenderelement darzustellen. Verwechseln Sie dieses Element nicht mit Elementen des AttendeeType-Schematyps. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

