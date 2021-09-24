---
title: MailboxSmtpAddress
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- MailboxSmtpAddress
api_type:
- schema
ms.assetid: de7c9035-ebbc-4473-ac14-3b22ce62768c
description: Das MailboxSmtpAddress-Element stellt die SMTP-Adresse des Benutzers dar, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen. oder deren Kennwortablaufdatum abgerufen werden soll.
ms.openlocfilehash: 86a39c416b9674e1f48f0a75508c003ad9d620f1
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59511131"
---
# <a name="mailboxsmtpaddress"></a>MailboxSmtpAddress

Das **MailboxSmtpAddress-Element** stellt die SMTP-Adresse des Benutzers dar, dessen Posteingangsregeln abgerufen oder aktualisiert werden sollen. oder deren Kennwortablaufdatum abgerufen werden soll. 
  
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
|[GetInboxRules](getinboxrules.md) <br/> |Definiert eine Anforderung zum Abrufen der Posteingangsregeln für ein Postfach im Serverspeicher.  <br/> |
|[GetPasswordExpirationDate](getpasswordexpirationdate.md) <br/> |Definiert eine Anforderung zum Abrufen des Kennwortablaufdatums eines E-Mail-Kontos.  <br/> |
|[UpdateInboxRules](updateinboxrules.md) <br/> |Definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.  <br/> |
   
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das **MailboxSmtpAddress-Element** ist ein optionales Element. Wenn das **MailboxSmtpAddress-Element** ausgelassen wird, wird die Adresse des angemeldeten Benutzers verwendet. 
  
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

