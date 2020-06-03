---
title: UpdateInboxRules
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UpdateInboxRules
api_type:
- schema
ms.assetid: d220064f-ff4d-4537-8077-adf94f2cbdbd
description: Das UpdateInboxRules -Element definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher.
ms.openlocfilehash: d604604d582d28c07eaa75d3239082d1b6735e65
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456360"
---
# <a name="updateinboxrules"></a>UpdateInboxRules

Das **UpdateInboxRules** -Element definiert eine Anforderung zum Aktualisieren der Posteingangsregeln in einem Postfach im Serverspeicher. 
  
```XML
<UpdateInboxRules>
   <MailboxSmtpAddress/>
   <RemoveOutlookRuleBlob/>
   <Operations/>
</UpdateInboxRules>
```

 **UpdateInboxRulesRequestType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[MailboxSmtpAddress](mailboxsmtpaddress.md) <br/> |Stellt die SMTP-Adresse des Benutzers, dessen Posteingangsregeln erstellt, geändert oder gelöscht werden.  <br/> |
|[RemoveOutlookRuleBlob](removeoutlookruleblob.md) <br/> |Gibt an, ob das Microsoft Outlook-Regel Blob entfernt.  <br/> |
|[Betrieb](operations.md) <br/> |Enthält ein Array der Regelvorgänge, die für ein Postfach ausgeführt werden können.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine.
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Leer kann sein  <br/> |True  <br/> |
   
## <a name="see-also"></a>Siehe auch



[UpdateInboxRules-Vorgang](updateinboxrules-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

