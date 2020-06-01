---
title: MailboxScope
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: c9778823-f290-4827-ba19-5f391ed4f877
description: Das MailboxScope-Element gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder sowohl das primäre als auch das Archivpostfach umfassen soll.
ms.openlocfilehash: 92823c06d4fe186917c3cfb532eda821bd6a95a7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44455373"
---
# <a name="mailboxscope"></a>MailboxScope

Das **MailboxScope** -Element gibt an, ob eine Suche oder ein Abruf für eine Unterhaltung entweder das primäre Postfach, das Archivpostfach oder sowohl das primäre als auch das Archivpostfach umfassen soll. 
  
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

[FindConversation](findconversation.md)  |  [GetConversationItems](getconversationitems.md)  |  Unter [Haltung (conversationtype)](conversation-conversationtype.md)
  
## <a name="text-value"></a>Textwert

Der Textwert des **MailboxScope** -Elements ist der Bereich zum Suchen oder erhalten von Elementen in einer Unterhaltung zwischen primären Postfächern, archivpostfächern oder sowohl primären als auch archivpostfächern. Der Textwert **Switch primaryonly** gibt einen Bereich an, der auf das primäre Postfach eines Benutzers abzielt. Der Textwert **Switch archiveonly** gibt einen Bereich an, der auf das Archivpostfach für einen Benutzer abzielt. Ein Textwert von **all** gibt einen Bereich an, der sowohl auf das primäre Postfach als auch auf das Archivpostfach zielt. 
  
## <a name="remarks"></a>Bemerkungen

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zu Elementen

|||
|:-----|:-----|
|Namespace  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichtenschema  <br/> |
|Überprüfungsdatei  <br/> |Messages. xsd  <br/> |
|Kann leer sein  <br/> |false  <br/> |
   

