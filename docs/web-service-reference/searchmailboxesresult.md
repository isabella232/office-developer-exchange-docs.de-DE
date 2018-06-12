---
title: SearchMailboxesResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: ddb276c4-6c8a-46ef-a2eb-46b6a0bfce09
description: Das SearchMailboxesResult-Element enthält das Ergebnis der Anforderung SearchMailboxes.
ms.openlocfilehash: 93e5837216ef8942b77ac2a91f5ef5f0ad001756
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831300"
---
# <a name="searchmailboxesresult"></a><span data-ttu-id="fbf17-103">SearchMailboxesResult</span><span class="sxs-lookup"><span data-stu-id="fbf17-103">SearchMailboxesResult</span></span>

<span data-ttu-id="fbf17-104">Das **SearchMailboxesResult** -Element enthält das Ergebnis der Anforderung **SearchMailboxes** .</span><span class="sxs-lookup"><span data-stu-id="fbf17-104">The **SearchMailboxesResult** element contains the result of the **SearchMailboxes** request.</span></span> 
  
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

 <span data-ttu-id="fbf17-105">**SearchMailboxesResultType**</span><span class="sxs-lookup"><span data-stu-id="fbf17-105">**SearchMailboxesResultType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbf17-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fbf17-106">Attributes and elements</span></span>

<span data-ttu-id="fbf17-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fbf17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbf17-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="fbf17-108">Attributes</span></span>

<span data-ttu-id="fbf17-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="fbf17-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbf17-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbf17-110">Child elements</span></span>

<span data-ttu-id="fbf17-111">[SearchQueries](searchqueries.md) | [ResultType-Wert](resulttype.md) | [ItemCount](itemcount.md) | [Größe (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [Elemente () ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [Einschränkungen](refiners.md) | [MailboxStats](mailboxstats.md)</span><span class="sxs-lookup"><span data-stu-id="fbf17-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [ItemCount](itemcount.md) | [Size (long)](size-long.md) | [PageItemCount](pageitemcount.md) | [PageItemSize](pageitemsize.md) | [KeywordStats](keywordstats.md) | [Items (ArrayOfSearchPreviewItemsType)](items-arrayofsearchpreviewitemstype.md) | [FailedMailboxes](failedmailboxes.md) | [Refiners](refiners.md) | [MailboxStats](mailboxstats.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fbf17-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbf17-112">Parent elements</span></span>

[<span data-ttu-id="fbf17-113">SearchMailboxesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="fbf17-113">SearchMailboxesResponseMessage</span></span>](searchmailboxesresponsemessage.md)
  
## <a name="remarks"></a><span data-ttu-id="fbf17-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbf17-114">Remarks</span></span>

<span data-ttu-id="fbf17-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="fbf17-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="fbf17-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="fbf17-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbf17-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fbf17-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbf17-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbf17-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="fbf17-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fbf17-119">Schema name</span></span>  <br/> |<span data-ttu-id="fbf17-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="fbf17-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="fbf17-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fbf17-121">Validation file</span></span>  <br/> |<span data-ttu-id="fbf17-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="fbf17-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="fbf17-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="fbf17-123">Can be empty</span></span>  <br/> |<span data-ttu-id="fbf17-124">false</span><span class="sxs-lookup"><span data-stu-id="fbf17-124">false</span></span>  <br/> |
   

