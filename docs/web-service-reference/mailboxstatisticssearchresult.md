---
title: MailboxStatisticsSearchResult
manager: sethgros
ms.date: 03/9/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 73499df7-3d50-4e39-895d-6e15dd8b2777
description: Das MailboxStatisticsSearchResult-Element enthält die Ergebnisse einer Schlüsselwortsuche.
ms.openlocfilehash: 5b40622cf15596d7ab8a7fa09c9a1998092c3ee7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830302"
---
# <a name="mailboxstatisticssearchresult"></a>MailboxStatisticsSearchResult

Das **MailboxStatisticsSearchResult** -Element enthält die Ergebnisse einer Schlüsselwortsuche. 
  
```XML
<MailboxStatisticsSearchResult>
   <UserMailbox/>
   <KeywordStatisticsSearchResult/>
</MailboxStatisticsSearchResult>
```

**MailboxStatisticsSearchResultType**

## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[UserMailbox](usermailbox.md) | [KeywordStatisticsSearchResult](keywordstatisticssearchresult.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[FindMailboxStatisticsByKeywordsResponseMessage](findmailboxstatisticsbykeywordsresponsemessage.md)
  
## <a name="remarks"></a>Hinweise

Dieses Element wurde in Exchange Server 2013 eingeführt.
  
Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.
  
## <a name="element-information"></a>Informationen zum Element

|||
|:-----|:-----|
|Namespace  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|Name des Schemas  <br/> |Nachrichten-schema  <br/> |
|Überprüfungsdatei  <br/> |Messages.xsd  <br/> |
|Kann leer sein  <br/> ||
   

