---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: Das EntityExtractionResult-Element gibt die EntityExtractionResult-Eigenschaft eines Elements an.
ms.openlocfilehash: ef99629beb95f1e1123569fa99e3f495c1b56e95
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758255"
---
# <a name="entityextractionresult"></a>EntityExtractionResult

Das **EntityExtractionResult** -Element gibt die **EntityExtractionResult** -Eigenschaft eines Elements an. 
  
```XML
<EntityExtractionResult>
    <Addresses/>
    <MeetingSuggestions/>
    <TaskSuggestions/>
    <EmailAddresses/>
    <Contacts/>
    <Urls/>
    <PhoneNumbers/>
</EntityExtractionResult>
```

 **EntityExtractionResultType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Adressen (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |Gibt ein Array von **AddressEntity** -Elementen.  <br/> |
|["Meetingsuggestions"](meetingsuggestions.md) <br/> |Gibt ein Array von **MeetingSuggestion** -Elementen.  <br/> |
|["Tasksuggestions"](tasksuggestions.md) <br/> |Gibt ein Array von **TaskSuggestion** -Elementen.  <br/> |
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Gibt ein Array von Entitäten für e-Mail-Adresse.  <br/> |
|[Kontakte (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Gibt ein Array von Kontakten.  <br/> |
|[URLs (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |Gibt ein Array von URLs.  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |Gibt ein Array von Rufnummern.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Item](item.md) <br/> |Stellt ein generisches Element im Exchange-Speicher.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Typschema  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

