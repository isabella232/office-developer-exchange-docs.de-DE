---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: Das MailboxSmtpAddress-Element stellt die SMTP-Adresse des Benutzers dar, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen. oder deren Kennwort-Ablaufdatum abgerufen werden soll.
ms.openlocfilehash: 613e8098210257280bec47f2b22a2d29d04fa07c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530544"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

Das **MailboxSmtpAddress** -Element stellt die SMTP-Adresse des Benutzers dar, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen. oder deren Kennwort-Ablaufdatum abgerufen werden soll. 
  
```XML
<MailboxSmtpAddress/>
```

**Zeichenfolge**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetInboxRules](getinboxrules.md) <br/> |Definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Server Speicher.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Definiert eine Anforderung zum Abrufen des Kennwortablauf Datums eines e-Mail-Kontos.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Server Speicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das **MailboxSmtpAddress** -Element ist ein optionales Element. Wenn das **MailboxSmtpAddress** -Element ausgelassen wird, wird die Adresse des angemeldeten Benutzers verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetInboxRules-Vorgang](getinboxrules-operation.md)
- [GetPasswordExpirationDate-Vorgang](getpasswordexpirationdate-operation.md)
- [UpdateInboxRules-Vorgang](updateinboxrules-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

