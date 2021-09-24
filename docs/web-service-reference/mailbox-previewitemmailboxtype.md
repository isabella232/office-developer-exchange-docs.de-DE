---
title: Postfach (PreviewItemMailboxType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: e898d737-b6e4-4403-9c2c-aec52a48a83d
description: Das Postfachelement enthält den Postfachbezeichner und die primäre SMTP-Adresse (Simple Mail Transfer Protocol) des Benutzers.
ms.openlocfilehash: 1a2dcc08d3e1595aede21e6982b36a60e6efafb5
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59514298"
---
# <a name="mailbox-previewitemmailboxtype"></a>Postfach (PreviewItemMailboxType)

Das **Postfachelement** enthält den Postfachbezeichner und die primäre SMTP-Adresse (Simple Mail Transfer Protocol) des Benutzers. 
  
```XML
<Mailbox>
   <MailboxId/>
   <PrimarySmtpAddress/>
</Mailbox>
```

**PreviewItemMailboxType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[MailboxId](mailboxid.md)  |  [PrimarySmtpAddress (Zeichenfolge)](primarysmtpaddress-string.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchPreviewItem](searchpreviewitem.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

