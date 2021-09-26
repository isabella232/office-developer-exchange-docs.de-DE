---
title: EmailAddress (EmailAddressType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 0cdabfcb-7658-4c7d-bb03-1e776ed11e43
description: Das EmailAddress-Element gibt die vollständig aufgelöste SMTP-Adresse für das Websitepostfach oder die zugeordnete Persona an.
ms.openlocfilehash: 76b279a82f6f277d9f231866437359ceae46df59
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59545258"
---
# <a name="emailaddress-emailaddresstype"></a>EmailAddress (EmailAddressType)

Das **EmailAddress-Element** gibt die vollständig aufgelöste SMTP-Adresse für das Websitepostfach oder die zugeordnete Persona an. 
  
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
|[Name (Zeichenfolge)](name-string.md) <br/> |Gibt einen Namen oder Schlüssel der Sucheinschränkung oder den Namen eines E-Mail-Benutzers an.  <br/> |
|[EmailAddress (NonEmptyStringType)](emailaddress-nonemptystringtype.md) <br/> |Definiert die primäre SMTP-Adresse eines Postfachbenutzers.  <br/> |
|[RoutingType (EmailAddressType)](routingtype-emailaddresstype.md) <br/> |Gibt den Routingtyp einer E-Mail-Adresse an.  <br/> |
|[MailboxType](mailboxtype.md) <br/> |Stellt den Typ des Postfachs dar, das durch die E-Mail-Adresse dargestellt wird.  <br/> |
|[ItemId](itemid.md) <br/> |Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements im Exchange Speicher.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Persona](persona.md) <br/> |Gibt eine Reihe von Persona-Daten an, die von einer **GetPersona-Anforderung** zurückgegeben werden.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element ist optional.
  
Das **EmailAddress-Element** gilt für Clients, die ab Exchange 2013 auf Exchange Online und Versionen von Microsoft Exchange Server abzielen. 
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

