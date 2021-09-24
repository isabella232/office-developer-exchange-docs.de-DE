---
title: E-Mail (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Email
api_type:
- schema
ms.assetid: dfffa1d5-2c3c-4f56-af63-5853df462e58
description: Das Email-Element stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar.
ms.openlocfilehash: 1176eeaac47e27971683d025beec29c1710432a1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513017"
---
# <a name="email-emailaddresstype"></a>E-Mail (EmailAddressType)

Das **Email-Element** stellt den Postfachbenutzer für eine GetUserAvailability-Abfrage dar. 
  
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)  
- [MailboxDataArray](mailboxdataarray.md) 
- [MailboxData](mailboxdata.md) 
- [E-Mail (EmailAddressType)](email-emailaddresstype.md)
  
```xml
<Email>
   <Name>...</Name>
   <Address>...</Address>
   <RoutingType>...</RoutingType>
</Email>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (EmailAddress)](name-emailaddress.md) <br/> |Stellt den Anzeigenamen des Postfachbenutzers dar.  <br/> |
|[Adresse (Zeichenfolge)](address-string.md) <br/> |Stellt die E-Mail-Adresse des Postfachbenutzers dar.  <br/> |
|[RoutingType (EmailAddress)](routingtype-emailaddress.md) <br/> |Stellt das Routingprotokoll für die Nachricht dar.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxData](mailboxdata.md) <br/> |Stellt einen einzelnen Postfachbenutzer und Optionen für den Typ der Daten dar, die über den Postfachbenutzer zurückgegeben werden sollen.  <br/> Es folgt der XPath für dieses Element:  <br/>  `/GetUserAvailabilityRequest/MailboxDataArray[i]/MailboxData` <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im Verzeichnis /EWS/ des Computers, auf dem MicrosoftExchange Server 2007 ausgeführt wird, auf dem die Clientzugriffsserverrolle installiert ist.
  
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

