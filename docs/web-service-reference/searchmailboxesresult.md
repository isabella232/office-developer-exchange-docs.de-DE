---
title: SearchMailboxesResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
ms.localizationpriority: medium
ms.assetid: ddb276c4-6c8a-46ef-a2eb-46b6a0bfce09
description: Das SearchMailboxesResult-Element enthält das Ergebnis der SearchMailboxes-Anforderung.
ms.openlocfilehash: dee1e12a6d083ca3f8d3ddb509775b454e3e8fc0
ms.sourcegitcommit: 54f6cd5a704b36b76d110ee53a6d6c1c3e15f5a9
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 09/24/2021
ms.locfileid: "59534405"
---
# <a name="searchmailboxesresult"></a>SearchMailboxesResult

Das **SearchMailboxesResult-Element** enthält das Ergebnis der **SearchMailboxes-Anforderung.** 
  
```XML
<SearchMailboxesResult>
   <SearchQueries/>
   <ResultType/>
   <ItemCount/>
   <Size/>
   <PageItemCount/>
   <PageItemSize/>
   <KeywordStats/>
   <Items/>
   <FailedMailboxes/>
   <Refiners/>
   <MailboxStats/>
</SearchMailboxesResult>
```

 **SearchMailboxesResultType**
## <a name="attributes-and-elements"></a>Attribute und Elemente

In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.
  
### <a name="attributes"></a>Attribute

Keine.
  
### <a name="child-elements"></a>Untergeordnete Elemente

[SearchQueries](searchqueries.md)  |  [ResultType](resulttype.md)  |  [ItemCount](itemcount.md)  |  [Größe (lang)](size-long.md)  |  [PageItemCount](pageitemcount.md)  |  [PageItemSize](pageitemsize.md)  |  [KeywordStats](keywordstats.md)  |  [Elemente (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md)  |  [FailedMailboxes](failedmailboxes.md)  |  [Einschränkungen](refiners.md)  |  [MailboxStats](mailboxstats.md)
  
### <a name="parent-elements"></a>Übergeordnete Elemente

[SearchMailboxesResponseMessage](searchmailboxesresponsemessage.md)
  
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
   

