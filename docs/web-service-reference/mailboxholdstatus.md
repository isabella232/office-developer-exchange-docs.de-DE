---
title: MailboxHoldStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: 92608b77-8aa4-403b-a4de-01e3a60af3e0
description: Das MailboxHoldStatus-Element gibt den Aufbewahrungsstatus des Postfachs an.
ms.openlocfilehash: de63acb14862e9f8cefded7130318c7f8cbd685f
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59540769"
---
# <a name="mailboxholdstatus"></a>MailboxHoldStatus

Das **MailboxHoldStatus-Element** gibt den Aufbewahrungsstatus des Postfachs an. 
  
```XML
<MailboxHoldStatus>
   <Mailbox/>
   <Status/>
   <AdditionalInfo/>
</MailboxHoldStatus>
```

**MailboxHoldStatusType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[Postfach (Zeichenfolge)](mailbox-string.md)  |  [Status (HoldStatusType)](status-holdstatustype.md)  |  [AdditionalInfo](additionalinfo.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[MailboxHoldStatuses](mailboxholdstatuses.md)
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|Name des Schemas  <br/> |Schematypen  <br/> |
|Überprüfungsdatei  <br/> |Types.xsd  <br/> |
|Kann leer sein  <br/> ||
   

