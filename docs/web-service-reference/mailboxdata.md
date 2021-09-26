---
title: MailboxData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxData
api_type:
- schema
ms.assetid: e9e3f50c-5a7b-49c7-a9ea-117959c08352
description: Das MailboxData-Element stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.
ms.openlocfilehash: 62c8c816fc0b0e0c6831d468d90e7303fb72d9be
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59546133"
---
# <a name="mailboxdata"></a>MailboxData

Das **MailboxData-Element** stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen. 
  
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
|[AttendeeType](attendeetype.md) <br/> |Stellt den Im Email [-Element (EmailAddressType)](email-emailaddresstype.md) identifizierten Teilnehmertyp dar. Dies wird in Anfragen für Besprechungsvorschläge verwendet.  <br/> |
|[ExcludeConflicts](excludeconflicts.md) <br/> |Gibt an, ob vorgeschlagene Uhrzeiten für Kalenderzeiten zurückgegeben werden sollen, die zwischen den Teilnehmern in Konflikt geraten.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxDataArray](mailboxdataarray.md) <br/> |Enthält eine Liste der Postfächer, die nach Verfügbarkeitsinformationen abgefragt werden sollen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Eine Clientanwendung kann eins bis viele **MailboxData-Elemente** definieren. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist. 
  
## <a name="example"></a>Beispiel

```xml
<MailboxDataArray>
  <MailboxData xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

