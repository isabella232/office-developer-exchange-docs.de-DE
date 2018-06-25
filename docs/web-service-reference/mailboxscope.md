---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: Das Element MailboxScope bestimmt, ob eine Suche oder Fetch für eine Unterhaltung sollten und das primäre Postfach, Archivpostfach oder sowohl die primäre umfassen Postfach zu archivieren.
ms.openlocfilehash: 89c9776079d686b114d6b744150f1c6df3711eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830293"
---
# <a name="mailboxscope"></a>MailboxScope

Das Element **MailboxScope** bestimmt, ob eine Suche oder Fetch für eine Unterhaltung sollten und das primäre Postfach, Archivpostfach oder sowohl die primäre umfassen Postfach zu archivieren. 
  
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

[FindConversation](findconversation.md) | [GetConversationItems](getconversationitems.md) | [Unterhaltung (ConversationType)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Textwert

Der Textwert der **MailboxScope** -Element entspricht der Bereich zum Suchen oder Abrufen von Elementen in einer Unterhaltung über entweder primären Postfächern, archivieren Postfächer oder Primär- und von archivpostfächern. Der Textwert **PrimaryOnly** gibt an, einen Bereich, der das primäre Postfach für einen Benutzer abzielt. Der Textwert **ArchiveOnly** gibt an, einen Bereich, der das Archivpostfach für einen Benutzer abzielt. Der Textwert **aller** gibt an, einen Bereich, der das primäre Postfach und Archivpostfach beruht. 
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

