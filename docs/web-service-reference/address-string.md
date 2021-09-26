---
title: Adresse (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: Das Address-Element stellt die E-Mail-Adresse des Postfachbenutzers dar.
ms.openlocfilehash: a3648246b6be8c4f7d6421fc979a57e782ef3598
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59543800"
---
# <a name="address-string"></a>Adresse (Zeichenfolge)

Das **Address-Element** stellt die E-Mail-Adresse des Postfachbenutzers dar. 
  
```xml
<Address>...</Address>
```

 **Zeichenfolge**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[E-Mail (EmailAddressType)](email-emailaddresstype.md) <br/> |Gibt die E-Mail-Adresse des MailboxData-Objekts an. Dieses Element wird im [GetUserAvailability-Vorgang](getuseravailability-operation.md)verwendet.<br/><br/> Es folgt der XPath für dieses Element:<br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Postfach (Verfügbarkeit)](mailbox-availability.md) <br/> | Stellt den Postfachbenutzer für eine SetUserOofSettings- oder GetUserOofSettings-Anforderung dar.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Textwert

Wenn dieses Element verwendet wird, ist ein Textwert erforderlich.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element kann höchstens einmal im [Email-Element (EmailAddressType)](email-emailaddresstype.md) und im [Mailbox-Element (Availability)](mailbox-availability.md) auftreten. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetUserAvailability-Vorgang](getuseravailability-operation.md)
- [GetUserOofSettings-Vorgang](getuseroofsettings-operation.md)
- [SetUserOofSettings-Vorgang](setuseroofsettings-operation.md)
- [GetUserAvailabilityRequest](getuseravailabilityrequest.md)
- [GetUserOofSettingsRequest](getuseroofsettingsrequest.md)
- [SetUserOofSettingsRequest](setuseroofsettingsrequest.md)
- [Abrufen der Benutzerverfügbarkeit](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

