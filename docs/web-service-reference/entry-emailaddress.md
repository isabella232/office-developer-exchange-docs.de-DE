---
title: Eintrag (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: Entry-Element stellt eine einzelne e-Mail-Adresse für einen Kontakt.
ms.openlocfilehash: 1852584e507c38da030815c37f85f7c4af4e2ba4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758250"
---
# <a name="entry-emailaddress"></a>Eintrag (EmailAddress)

**Entry** -Element stellt eine einzelne e-Mail-Adresse für einen Kontakt. 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

**EmailAddressDictionaryEntryType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Key** <br/> | Gibt die e-Mail-Adresse.<br/><br/>Es folgen die möglichen Werte für dieses Attribut.<br/><br/>-EmailAddress1  <br/>-EmailAddress2  <br/>-EmailAddress3 <br/><br/>  Dieses Attribut ist erforderlich.  <br/> |
|**Name** <br/> |Definiert den Namen des Postfachbenutzers. Dieses Attribut ist optional.  <br/> |
|**RoutingType** <br/> |Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Attribut ist optional.  <br/> |
|**MailboxType** <br/> |Definiert den Postfachtyp eines Postfachbenutzers. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EmailAddresses](emailaddresses.md) <br/> |Stellt eine Auflistung von E-mail-Adressen für einen Kontakt.  <br/> |
   
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

