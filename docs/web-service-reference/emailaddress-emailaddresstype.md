---
title: E-mailemail (e-)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: Das Address-Element gibt die vollständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugehörige Rolle an.
ms.openlocfilehash: 8b04b75e91cc16be7f88c9a0ac08c5e36855056e
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463461"
---
# <a name="emailaddress-emailaddresstype"></a>E-mailemail (e-)

Das Address **-Element gibt die voll** ständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugehörige Rolle an. 
  
```xml
<EmailAddress>
    <Name></Name>
    <EmailAddress></EmailAddress>
    <RoutingType></RoutingType>
    <MailboxType></MailboxType>
    <ItemId></ItemId>
</EmailAddress>
```

 **EmailAddressType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Name (Zeichenfolge)](name-string.md) <br/> |Gibt einen Such Einschränkungsnamen oder-Schlüssel oder den Namen eines e-Mail-Benutzers an.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Definiert die primäre SMTP-Adresse eines Postfachbenutzers.  <br/> |
|[Routingtype (e-mailemailtype)](routingtype-emailaddresstype.md) <br/> |Gibt den Routingtyp einer e-Mail-Adresse an.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Stellt den Typ des Postfachs dar, der durch die e-Mail-Adresse dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Gibt eine Gruppe von Persona-Daten an, die von einer **getpersona** -Anforderung zurückgegeben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Dieses Element ist optional.
  
Das **Email** -Element ist für Clients gültig, die Exchange Online und Versionen von Exchange Server, die mit Exchange 2013 beginnen, abzielen. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

