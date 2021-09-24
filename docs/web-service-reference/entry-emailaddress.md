---
title: Eintrag (EmailAddress)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- Entry
api_type:
- schema
ms.assetid: b028c5c7-3494-4ecd-96d1-78783daa660f
description: Das Entry-Element stellt eine einzelne E-Mail-Adresse für einen Kontakt dar.
ms.openlocfilehash: 96351a82e113f2c4aa73776e89e1eb7e7a683433
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59520668"
---
# <a name="entry-emailaddress"></a>Eintrag (EmailAddress)

Das **Entry-Element** stellt eine einzelne E-Mail-Adresse für einen Kontakt dar. 
  
```XML
<Entry Key="" Name="" RoutingType="" MailboxType="" />
```

**EmailAddressDictionaryEntryType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

|**Attribut**|**Beschreibung**|
|:-----|:-----|
|**Key** <br/> | Gibt die E-Mail-Adresse an.<br/><br/>Es folgen die möglichen Werte für dieses Attribut.<br/><br/>- EmailAddress1  <br/>- EmailAddress2  <br/>- EmailAddress3 <br/><br/>  Dieses Attribut ist erforderlich.  <br/> |
|**Name** <br/> |Definiert den Namen des Postfachbenutzers. Dieses Attribut ist optional.  <br/> |
|**RoutingType** <br/> |Definiert die Weiterleitung, die für das Postfach verwendet wird. Der Standard lautet SMTP. Dieses Attribut ist optional.  <br/> |
|**MailboxType** <br/> |Definiert den Postfachtyp eines Postfachbenutzers. Dieses Attribut ist optional.  <br/> |
   
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[EmailAddresses](emailaddresses.md) <br/> |Stellt eine Auflistung von E-Mail-Adressen für einen Kontakt dar.  <br/> |
   
## <a name="remarks"></a>HinwBemerkungeneise

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

