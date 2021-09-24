---
title: Kontakt (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: Das Contact-Element gibt einen Kontakt in der einheitlichen Kontakt-Store an.
ms.openlocfilehash: e52573841f934a11c05a1da9e19f91146ed9c774
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511993"
---
# <a name="contact-contacttype"></a>Kontakt (ContactType)

Das **Contact-Element** gibt einen Kontakt in der einheitlichen Kontakt-Store an. 
  
```XML
<Contact>
    <PersonName></PersonName>
    <BusinessName></BusinessName>
    <PhoneNumbers></PhoneNumbers>
    <Urls></Urls>
    <EmailAddresses></EmailAddresses>
    <Addresses></Addesses>    <ContactString></ContactString
</Contact>
```

 **ContactType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[PersonName](personname.md) <br/> |Gibt den Namen einer Person an.  <br/> |
|[BusinessName](businessname.md) <br/> |Gibt den Namen eines Unternehmens an.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.  <br/> |
|[Urls](urls.md) <br/> |Gibt ein Array von URLs für eine Persona an.  <br/> |
|[EmailAddresses (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |Gibt ein Array extrahierter E-Mail-Adressen an.  <br/> |
|[Adressen (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Gibt ein Array von **Address-Elementen** an.  <br/> |
|[ContactString](contactstring.md) <br/> |Gibt den Anzeigenamen eines Kontakts an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Kontakte (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Gibt ein Array von Kontakten an.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

