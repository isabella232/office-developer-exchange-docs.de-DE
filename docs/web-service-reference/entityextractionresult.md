---
title: EntityExtractionResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 643b99ab-ff90-4411-864c-1077623028d6
description: Das EntityExtractionResult-Element gibt die EntityExtractionResult-Eigenschaft eines Elements an.
ms.openlocfilehash: b550953233999bfd9c4dc08a7f892e798029df3c
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520675"
---
# <a name="entityextractionresult"></a>EntityExtractionResult

Das **EntityExtractionResult-Element** gibt die **EntityExtractionResult-Eigenschaft** eines Elements an. 
  
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
|[Adressen (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |Gibt ein Array von **AddressEntity-Elementen** an.  <br/> |
|[MeetingSuggestions](meetingsuggestions.md) <br/> |Gibt ein Array von **MeetingSuggestion-Elementen** an.  <br/> |
|[TaskSuggestions](tasksuggestions.md) <br/> |Gibt ein Array von **TaskSuggestion-Elementen an.**  <br/> |
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Gibt ein Array von E-Mail-Adressentitäten an.  <br/> |
|[Kontakte (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Gibt ein Array von Kontakten an.  <br/> |
|[Urls (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |Gibt ein Array von URLs an.  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |Gibt ein Array von Telefonnummern an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Item](item.md) <br/> |Stellt ein generisches Element im Exchange Speicher dar.  <br/> |
   
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

