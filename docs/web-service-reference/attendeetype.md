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
description: Das Element AttendeeType stellt den Typ des Teilnehmers, der in der E-Mail (EmailAddressType)-Element identifiziert wird. Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet.
ms.openlocfilehash: a08532ed78296102ee252c1e0c40beee7ca8ea5d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757404"
---
# <a name="attendeetype"></a>AttendeeType

Das Element **AttendeeType** stellt den Typ des Teilnehmers, der in der [E-Mail (EmailAddressType)](email-emailaddresstype.md) -Element identifiziert wird. Dieses Element wird in Anforderungen für Besprechungsvorschläge verwendet. 
  
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
|[MailboxData](mailboxdata.md) <br/> |Stellt eine einzelne Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="text-value"></a>Textwert

Es wird ein Textwert für dieses Element erforderlich. Die folgende Tabelle enthält die möglichen Werte für dieses Element.
  
|**Wert**|**Beschreibung**|
|:-----|:-----|
|Organisator  <br/> |Die Postfachbenutzer und Teilnehmer, die das Kalenderelement erstellt hat.  <br/> |
|Erforderlich  <br/> |Einen Postfachbenutzer an, der ein Erforderlicher Teilnehmer der Besprechung ist.  <br/> |
|Optional  <br/> |Einen Postfachbenutzer an, der einem optionalen Teilnehmer der Besprechung ist.  <br/> |
|Raum  <br/> |Ein Postfach-Entität, die eine Raum Ressource für die Besprechung verwendet darstellt.  <br/> |
|Ressource  <br/> |Eine Ressource wie TV oder für die Verwendung in der Besprechung geplant ist Projektor.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element ist ein erforderliches untergeordnetes Element des Elements [MailboxData](mailboxdata.md) . Dieses Element kann nur einmal im Element [MailboxData](mailboxdata.md) auftreten. Das Schema, das dieses Element beschreibt befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
> [!NOTE]
> Der Typ des AttendeeType-Schema wird verwendet, um Teilnehmer für ein Kalenderelement darstellen. Verwechseln Sie nicht dieses Element mit Elementen des Typs AttendeeType Schema. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

