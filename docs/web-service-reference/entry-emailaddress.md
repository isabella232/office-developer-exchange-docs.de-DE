---
title: Eintrag (e-mailemail)
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
description: Das Entry-Element stellt eine einzelne e-Mail-Adresse für einen Kontakt dar.
ms.openlocfilehash: 766d67cda10b02c07a7677e541fddfc38a4285cf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459644"
---
# <a name="entry-emailaddress"></a>Eintrag (e-mailemail)

Das **Entry** -Element stellt eine einzelne e-Mail-Adresse für einen Kontakt dar. 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

**EmailAddressDictionaryEntryType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Key** <br/> | Identifiziert die e-Mail-Adresse.<br/><br/>Es folgen die möglichen Werte für dieses Attribut.<br/><br/>-EmailAddress1  <br/>-EmailAddress2  <br/>- EmailAddress3 <br/><br/>  Dieses Attribut ist erforderlich.  <br/> |
|**Name** <br/> |Definiert den Namen des Postfachbenutzers. Dieses Attribut ist optional.  <br/> |
|**Routing Type** <br/> |Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Attribut ist optional.  <br/> |
|**MailboxType** <br/> |Definiert den Postfachtyp eines Postfachbenutzers. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EmailAddresses](emailaddresses.md) <br/> |Stellt eine Auflistung von e-Mail-Adressen für einen Kontakt dar.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

