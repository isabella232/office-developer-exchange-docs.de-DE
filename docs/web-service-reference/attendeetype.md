---
title: AttendeeType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeType
api_type:
- schema
ms.assetid: 048043a8-dbad-45a0-97c8-4cad63d8898b
description: Das AttendeeType-Element stellt den Typ des Teilnehmers dar, der im e-Mail-Element (Epost) identifiziert wird. Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet.
ms.openlocfilehash: 104b9f38cc891310ecb47c0b47837a912ced6ab7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462297"
---
# <a name="attendeetype"></a>AttendeeType

Das **AttendeeType** -Element stellt den Typ des Teilnehmers dar, der im [e-Mail-Element (Epost)](email-emailaddresstype.md) identifiziert wird. Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet. 
  
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
|Erforderlich  <br/> |Ein Postfachbenutzer, der ein Erforderlicher Teilnehmer für die Besprechung ist.  <br/> |
|Optional  <br/> |Ein Postfachbenutzer, der ein optionaler Teilnehmer für die Besprechung ist.  <br/> |
|Raum  <br/> |Eine Post Fach Entität, die eine Raum Ressource darstellt, die für die Besprechung verwendet wird.  <br/> |
|Ressource  <br/> |Eine Ressource wie ein Fernsehgerät oder Projektor, die für die Besprechung geplant ist.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element ist ein erforderliches untergeordnetes Element des [MailboxData](mailboxdata.md) -Elements. Dieses Element kann nur einmal im [MailboxData](mailboxdata.md) -Element vorkommen. Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis/EWS/"aus des Computers mit Microsoft Exchange Server 2007, auf dem die Client Zugriffs-Serverrolle installiert ist. 
  
> [!NOTE]
> Der AttendeeType-Schematyp wird zum Darstellen von Teilnehmern eines Kalenderelements verwendet. Verwechseln Sie dieses Element nicht mit Elementen des AttendeeType-Schematyps. 
  
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
- [Verfügbarkeit von Benutzern wird abgerufen](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

