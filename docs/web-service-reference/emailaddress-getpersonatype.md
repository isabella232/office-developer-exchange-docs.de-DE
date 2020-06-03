---
title: E-mailemail (getpersonatype)
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 052055b5-4630-40ed-9b24-9e7f4bf7ba1d
description: Das Address-Element (getpersonatype) gibt die e-Mail-Adresse an, die der Rolle zugeordnet ist.
ms.openlocfilehash: b58f61202cd94ff282b21138b47b40887b38752a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463454"
---
# <a name="emailaddress-getpersonatype"></a>E-mailemail (getpersonatype)

Das Address-Element **(getpersonatype)** gibt die e-Mail-Adresse an, die der Rolle zugeordnet ist. 
  
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

[Name (Zeichenfolge)](name-string.md)  |  [E-mailemail (NonEmptyStringType)](emailaddress-nonemptystringtype.md)  |  [Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md)  |  [Mailboxtype](mailboxtype.md)  |  [ItemID](itemid.md)  |  [OriginalDisplayName](originaldisplayname.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[GetPersona](getpersona.md)
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 Service Pack 1 (SP1) eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetPersona](getpersona.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

