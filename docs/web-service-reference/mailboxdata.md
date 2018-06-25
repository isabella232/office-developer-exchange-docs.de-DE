---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: Das MailboxData-Element stellt ein einzelnes Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll.
ms.openlocfilehash: df60294e7d83b1459e5cca7d75c2b6b4bb9d931d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830281"
---
# <a name="mailboxdata"></a>MailboxData

Das **MailboxData** -Element stellt ein einzelnes Postfachbenutzer und Optionen für den Typ der Daten zu den Postfachbenutzer zurückgegeben werden soll. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
  
- [MailboxDataArray](mailboxdataarray.md)
  
- [MailboxData](mailboxdata.md)
  
```xml
<MailboxData>
   <Email>...</Email>
   <AttendeeType>...</AttendeeType>
   <ExcludeConflicts>...</ExcludeConflicts>
<MailboxData>
```

**MailboxData**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[E-Mail (EmailAddressType)](email-emailaddresstype.md) <br/> |Stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.  <br/> |
|[AttendeeType](attendeetype.md) <br/> |Stellt den Typ des Teilnehmers [(EmailAddressType) E-Mail](email-emailaddresstype.md) -Element identifiziert. Dies wird in Anforderungen für Besprechungsvorschläge verwendet.  <br/> |
|[ExcludeConflicts](excludeconflicts.md) <br/> |Gibt an, ob zurückzugebenden vorgeschlagenen Zeiten für Kalender Versuche, die auf der Teilnehmerliste in Konflikt stehen.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxDataArray](mailboxdataarray.md) <br/> |Enthält eine Liste der Postfächer, um Informationen zur Verfügbarkeit abzufragen.  <br/> Es folgt der XPath-Ausdruck für dieses Element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a>Hinweise

Eine Clientanwendung kann auf viele **MailboxData** -Elemente definieren. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Exchange Server 2007 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist. 
  
## <a name="example"></a>Beispiel

```xml
<MailboxDataArray>
  <MailboxData xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
    <Email>
      <Name></Name>
      <Address>someone@ExServer.example.com</Address>
      <RoutingType>SMTP</RoutingType>
    </Email>
    <AttendeeType>Organizer</AttendeeType>
    <ExcludeConflicts>false</ExcludeConflicts>
  </MailboxData>
</MailboxDataArray>
```

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

