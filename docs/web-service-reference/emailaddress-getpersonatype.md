---
title: EmailAddress (GetPersonaType)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: Das EmailAddress (GetPersonaType)-Element gibt die E-Mail-Adresse an, die der Persona zugeordnet ist.
ms.openlocfilehash: 7d024234c66c2b90bdd5d04f25d67db54770bdb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520805"
---
# <a name="emailaddress-getpersonatype"></a>EmailAddress (GetPersonaType)

Das **EmailAddress (GetPersonaType)-Element** gibt die E-Mail-Adresse an, die der Persona zugeordnet ist. 
  
```XML
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
    <OriginalDisplayName></OriginalDisplayName>
</EmailAddress>>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Name (Zeichenfolge)](name-string.md)  |  [EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md)  |  [RoutingType (EmailAddressType)](routingtype-emailaddresstype.md)  |  [MailboxType](mailboxtype.md)  |  [ItemId](itemid.md)  |  [OriginalDisplayName](originaldisplayname.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetPersona](getpersona.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetPersona](getpersona.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

