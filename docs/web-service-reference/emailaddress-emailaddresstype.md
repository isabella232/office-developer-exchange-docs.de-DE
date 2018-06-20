---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: Das EmailAddress-Element gibt die vollständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugeordneten Rolle.
ms.openlocfilehash: c31a37fc0dbdcc2b501b82346a17a0a3b4775556
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758158"
---
# <a name="emailaddress-emailaddresstype"></a>EmailAddress (EmailAddressType)

Das **EmailAddress** -Element gibt die vollständig aufgelöste SMTP-Adresse für das websitepostfach oder die zugeordneten Rolle. 
  
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
|[Name (Zeichenfolge)](name-string.md) <br/> |Gibt einen Suchbegriff Einschränkung und Schlüssel oder den Namen eines e-Mail-Benutzers an.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Definiert die primäre SMTP-Adresse eines Postfachbenutzers an.  <br/> |
|[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) <br/> |Gibt an, welche routing von e-Mail-Adresse.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Stellt den Typ des Postfachs an, das die e-Mail-Adresse dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Rolle](persona.md) <br/> |Gibt einen Satz von Persona Daten von einer Anforderung **GetPersona** zurückgegeben.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Dieses Element ist optional.
  
Das **EmailAddress** -Element ist für Clients, die Exchange Online und Versionen von Microsoft Exchange Server beginnend mit Exchange 2013 abzielen. 
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

