---
title: InvalidRecipient
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- InvalidRecipient
api_type:
- schema
ms.assetid: 9e2d3433-22d7-444b-9883-e5649297d8fe
description: Das InvalidRecipient-Element enthält die SMTP-Adresse des ungültigen Empfängers sowie Informationen dazu, warum der Empfänger ungültig ist.
ms.openlocfilehash: f301b31c1054625151ce90e41fca5e3efc21f473
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526550"
---
# <a name="invalidrecipient"></a>InvalidRecipient

Das **InvalidRecipient** -Element enthält die SMTP-Adresse des ungültigen Empfängers sowie Informationen dazu, warum der Empfänger ungültig ist. 
  
```XML
<InvalidRecipient>
   <SmtpAddress/>
   <ResponseCode/>
   <MessageText/>
</InvalidRecipient>

```

 **InvalidRecipientType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[SmtpAddress](smtpaddress.md) <br/> |Enthält die SMTP-Adresse des ungültigen Empfängers. Dieses Element ist erforderlich.  <br/> |
|[Response Code (InvalidRecipientResponseCodeType)](responsecode-invalidrecipientresponsecodetype.md) <br/> |Stellt einen Fehlercode bereit, der den spezifischen Fehler identifiziert, der bei der Anforderung aufgetreten ist. Dieses Element ist erforderlich.  <br/> |
|[MessageText](messagetext.md) <br/> |Enthält eine Textbeschreibung des Status der Antwort. Dieses Element ist optional.  <br/> |
   
### <a name="parent-elements"></a>Übergeordnete Elemente

|**Element**|**Beschreibung**|
|:-----|:-----|
|[InvalidRecipients](invalidrecipients.md) <br/> |Stellt die Empfänger einer Anforderung für eine Ordnerfreigabe dar, die ungültig sind.  <br/> |
   
## <a name="remarks"></a>Bemerkungen

Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Leer kann sein  <br/> |False  <br/> |
   
## <a name="see-also"></a>Siehe auch



[GetSharingMetadata-Vorgang](getsharingmetadata-operation.md)


- [EWS-XML-Elemente in Exchange](ews-xml-elements-in-exchange.md)

