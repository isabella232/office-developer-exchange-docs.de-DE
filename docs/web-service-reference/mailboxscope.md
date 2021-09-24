---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: Das MailboxScope-Element gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder das primäre postfach und das Archivpostfach umfassen soll.
ms.openlocfilehash: 705c72ae2aefbb16599f392eb712d080668490b0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59522880"
---
# <a name="mailboxscope"></a>MailboxScope

Das **MailboxScope-Element** gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder das primäre postfach und das Archivpostfach umfassen soll. 
  
```XML
<MailboxScope> PrimaryOnly | ArchiveOnly | All </MailboxScope>
```

**MailboxSearchLocationType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

Keine.
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindConversation](findconversation.md)  |  [GetConversationItems](getconversationitems.md)  |  [Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **MailboxScope-Elements** ist der Bereich zum Suchen oder Abrufen von Elementen in einer Unterhaltung über primäre Postfächer, Archivpostfächer oder sowohl primäre als auch Archivpostfächer hinweg. Der Textwert **"PrimaryOnly"** gibt einen Bereich an, der auf das primäre Postfach eines Benutzers ausgerichtet ist. Der Textwert **ArchiveOnly** gibt einen Bereich an, der auf das Archivpostfach für einen Benutzer ausgerichtet ist. Der Textwert **"Alle"** gibt einen Bereich an, der sowohl auf das primäre Postfach als auch auf das Archivpostfach ausgerichtet ist. 
  
## <a name="remarks"></a>HinwBemerkungeneise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

