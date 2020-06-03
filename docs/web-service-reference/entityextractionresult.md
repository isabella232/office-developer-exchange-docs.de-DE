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
ms.openlocfilehash: f2f069717a5862adff3349090c35f95499d135f8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456955"
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
|[Adressen (ArrayOfAddressEntitiesType)](addresses-arrayofaddressentitiestype.md) <br/> |Gibt ein Array von **AddressEntity** -Elementen an.  <br/> |
|[MeetingSuggestions](meetingsuggestions.md) <br/> |Gibt ein Array von **MeetingSuggestion** -Elementen an.  <br/> |
|[TaskSuggestions](tasksuggestions.md) <br/> |Gibt ein Array von **Task Suggestion** -Elementen an.  <br/> |
|[Emails (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Gibt ein Array von e-Mail-Adress Entitäten an.  <br/> |
|[Kontakte (ArrayOfContactsType)](contacts-arrayofcontactstype.md) <br/> |Gibt ein Array von Kontakten an.  <br/> |
|[URLs (ArrayOfUrlEntitiesType)](urls-arrayofurlentitiestype.md) <br/> |Gibt ein Array von URLs an.  <br/> |
|[PhoneNumbers (ArrayOfPhoneEntitiesType)](phonenumbers-arrayofphoneentitiestype.md) <br/> |Gibt ein Array von Telefonnummern an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[Item](item.md) <br/> |Stellt ein generisches Element in der Exchange-Informationsspeicher dar.  <br/> |
   
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

