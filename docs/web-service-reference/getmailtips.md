---
title: GetMailTips
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
api_name:
- GetMailTips
api_type:
- schema
ms.assetid: 4a24ff79-f1ae-43a1-9ac2-49baf3eaa173
description: Das GetMailTips-Element stellt die Empfänger und Typen von E-Mail-Tipps dar, die abgerufen werden sollen.
ms.openlocfilehash: 03c416f7e60e9677d77a389ab052aa0057e278da
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59533750"
---
# <a name="getmailtips"></a>GetMailTips

Das **GetMailTips-Element** stellt die Empfänger und Typen von E-Mail-Tipps dar, die abgerufen werden sollen. 
  
```XML
<GetMailTips>
   <SendingAs/>
   <Recipients/>
   <MailTipsRequested/>
</GetMailTips>
```

 **GetMailTipsType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SendingAs](sendingas.md) <br/> |Enthält eine E-Mail-Adresse, an die ein Benutzer senden möchte.  <br/> |
|[Empfänger (ArrayOfRecipientsType)](recipients-arrayofrecipientstype.md) <br/> |Enthält eine Liste der Empfänger, die nach E-Mail-Tipps gesucht werden sollen.  <br/> |
|[MailTipsRequested](mailtipsrequested.md) <br/> |Enthält die Typen von E-Mail-Tipps, die vom Dienst angefordert werden.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

Keine
  
## <a name="text-value"></a>Textwert

Keine.
  
## <a name="remarks"></a>HinwBemerkungeneise

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

