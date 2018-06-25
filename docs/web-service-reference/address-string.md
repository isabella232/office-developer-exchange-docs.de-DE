---
title: Adresse (Zeichenfolge)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Address
api_type:
- schema
ms.assetid: a3cdfcbd-d0c5-46d6-8daa-52405fc63ff0
description: Das Address-Element stellt die e-Mail-Adresse des Postfachbenutzers an.
ms.openlocfilehash: 07c634d6166d88a8912bc66081a13671e600c801
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757241"
---
# <a name="address-string"></a>Adresse (Zeichenfolge)

Das **Address** -Element stellt die e-Mail-Adresse des Postfachbenutzers an. 
  
```xml
<Address>...</Address>
```

 **string**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[E-Mail (EmailAddressType)](email-emailaddresstype.md) <br/> |Gibt die e-Mail-Adresse des MailboxData-Objekts. Dieses Element wird in den [GetUserAvailability-Vorgang](getuseravailability-operation.md)verwendet.<br/><br/> Es folgt der XPath-Ausdruck für dieses Element:<br/><br/>  `/GetUserAvailabilityRequest/MailboxDataArray/MailboxData[i]/Email` <br/> |
|[Postfach (Verfügbarkeit)](mailbox-availability.md) <br/> | Stellt den Postfachbenutzer für eine Anforderung SetUserOofSettings oder GetUserOofSettings.<br/><br/>  Folgende XPath-Ausdrücke werden für dieses Element verwendet:<br/><br/>  `/GetUserOofSettingsRequest/Mailbox` <br/>  `/SetUserOofSettingsRequest/Mailbox` <br/> |
   
## <a name="text-value"></a>Textwert

Ein Textwert ist erforderlich, wenn dieses Element verwendet wird.
  
## <a name="remarks"></a>Hinweise

Dieses Element kann höchstens einmal in das Element [E-Mail (EmailAddressType)](email-emailaddresstype.md) und das [Postfach (Verfügbarkeit)](mailbox-availability.md) Element auftreten. 
  
> [!NOTE]
> Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
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
- [Erste Benutzer Verfügbarkeit](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

