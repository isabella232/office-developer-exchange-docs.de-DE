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
description: Das MailboxSmtpAddress-Element darstellt, die SMTP-Adresse des Benutzers, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen; oder, deren Ablaufdatum Kennwort abgerufen werden sollen.
ms.openlocfilehash: 60b2c018f2a05e9630e92e28de1054a421b41e52
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830303"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

Das **MailboxSmtpAddress** -Element darstellt, die SMTP-Adresse des Benutzers, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen; oder, deren Ablaufdatum Kennwort abgerufen werden sollen. 
  
```XML
<MailboxSmtpAddress/>
```

**string**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[GetInboxRules](getinboxrules.md) <br/> |Definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Serverspeicher.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Definiert eine Anforderung an das Kennwort Ablaufdatum ein e-Mail-Konto zu erhalten.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Hinweise

Das **MailboxSmtpAddress** -Element ist ein optionales Element. Wenn das Element **MailboxSmtpAddress** ausgelassen wird, wird die Adresse des angemeldeten Benutzers verwendet. 
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch

- [GetInboxRules-Vorgang](getinboxrules-operation.md)
- [GetPasswordExpirationDate-Vorgang](getpasswordexpirationdate-operation.md)
- [UpdateInboxRules-Vorgang](updateinboxrules-operation.md)
- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

