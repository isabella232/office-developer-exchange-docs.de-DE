---
title: Kontakt (ContactType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 7f7119b7-f5b4-484d-a7de-fa74836d9aee
description: Das Contact-Element gibt einen Kontakt im einheitlichen Kontaktspeicher an.
ms.openlocfilehash: e8ebc28456f8bfc26f5d790ac9ff278930041ea0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461520"
---
# <a name="contact-contacttype"></a>Kontakt (ContactType)

Das **Contact** -Element gibt einen Kontakt im einheitlichen Kontaktspeicher an. 
  
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
|[PersonName](personname.md) <br/> |Gibt den Namen eines einzelnen an.  <br/> |
|[Business Name](businessname.md) <br/> |Gibt den Namen eines Unternehmens an.  <br/> |
|[PhoneNumbers](phonenumbers.md) <br/> |Stellt eine Auflistung von Telefonnummern für einen Kontakt dar.  <br/> |
|[Urls](urls.md) <br/> |Gibt ein Array von URLs für eine Rolle an.  <br/> |
|[Emails (ArrayOfExtractedEmailAddresses)](emailaddresses-arrayofextractedemailaddresses.md) <br/> |Gibt ein Array von extrahierten e-Mail-Adressen an.  <br/> |
|[Adressen (ArrayOfAddressesType)](addresses-arrayofaddressestype.md) <br/> |Gibt ein Array von **Address** -Elementen an.  <br/> |
|[ContactType](contactstring.md) <br/> |Gibt den Anzeigenamen eines Kontakts an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Kontakte (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Gibt ein Array von Kontakten an.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types. xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

