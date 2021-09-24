---
title: EmailAddressEntity
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 20049467-c01a-4c7d-8ada-ca1801cc95ed
description: Das EmailAddressEntity-Element gibt eine einzelne E-Mail-Adressentität an.
ms.openlocfilehash: ecdf97d64e5c743cab3002091196deeba509c5eb
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59513010"
---
# <a name="emailaddressentity"></a>EmailAddressEntity

Das **EmailAddressEntity-Element** gibt eine einzelne E-Mail-Adressentität an. 
  
```XML
<EmailAddressEntity>
    <EmailAddress></EmailAddress>
</EmailAddressEntity>
```

 **EmailAddressEntityType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EmailAddress (Zeichenfolge)](emailaddress-string.md) <br/> |Gibt eine einzelne E-Mail-Adresse an.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EmailAddresses (ArrayOfEmailAddressEntitiesType)](emailaddresses-arrayofemailaddressentitiestype.md) <br/> |Gibt ein Array von E-Mail-Adressentitäten an.  <br/> |
   
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

