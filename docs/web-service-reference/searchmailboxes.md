---
title: SearchMailboxes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 5d8c367a-67e9-43b3-8be0-6362d2152431
description: Das SearchMailboxes-Element gibt den Anfang der SearchMailboxes Anforderung.
ms.openlocfilehash: cf8007be3201e2248f27371c2a80c960735a3ced
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831306"
---
# <a name="searchmailboxes"></a><span data-ttu-id="401ec-103">SearchMailboxes</span><span class="sxs-lookup"><span data-stu-id="401ec-103">SearchMailboxes</span></span>

<span data-ttu-id="401ec-104">Das **SearchMailboxes** -Element gibt den Anfang der **SearchMailboxes** Anforderung.</span><span class="sxs-lookup"><span data-stu-id="401ec-104">The **SearchMailboxes** element indicates the beginning of the **SearchMailboxes** request.</span></span> 
  
```XML
<SearchMailboxes>
   <SearchQueries/>
   <ResultType/>
   <PreviewItemResponseShape/>
   <SortBy/>
   <Language/>
   <Deduplication/>
   <PageSize/>
   <PageItemReference/>
   <PageDirection/>
</SearchMailboxes>
```

 <span data-ttu-id="401ec-105">**SearchMailboxesType**</span><span class="sxs-lookup"><span data-stu-id="401ec-105">**SearchMailboxesType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="401ec-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="401ec-106">Attributes and elements</span></span>

<span data-ttu-id="401ec-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="401ec-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="401ec-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="401ec-108">Attributes</span></span>

<span data-ttu-id="401ec-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="401ec-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="401ec-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="401ec-110">Child elements</span></span>

<span data-ttu-id="401ec-111">[SearchQueries](searchqueries.md) | [ResultType-Wert](resulttype.md) | [PreviewItemResponseShape](previewitemresponseshape.md) | [SortBy](sortby.md) | [Sprache](language.md) | [Deduplizierung](deduplication.md) | [PageSize](pagesize.md)  |  [ PageItemReference](pageitemreference.md) | [PageDirection](pagedirection.md)</span><span class="sxs-lookup"><span data-stu-id="401ec-111">[SearchQueries](searchqueries.md) | [ResultType](resulttype.md) | [PreviewItemResponseShape](previewitemresponseshape.md) | [SortBy](sortby.md) | [Language](language.md) | [Deduplication](deduplication.md) | [PageSize](pagesize.md) | [PageItemReference](pageitemreference.md) | [PageDirection](pagedirection.md)</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="401ec-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="401ec-112">Parent elements</span></span>

<span data-ttu-id="401ec-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="401ec-113">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="401ec-114">Hinweise</span><span class="sxs-lookup"><span data-stu-id="401ec-114">Remarks</span></span>

<span data-ttu-id="401ec-115">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="401ec-115">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="401ec-116">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="401ec-116">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="401ec-117">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="401ec-117">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="401ec-118">Namespace</span><span class="sxs-lookup"><span data-stu-id="401ec-118">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="401ec-119">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="401ec-119">Schema name</span></span>  <br/> |<span data-ttu-id="401ec-120">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="401ec-120">Messages schema</span></span>  <br/> |
|<span data-ttu-id="401ec-121">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="401ec-121">Validation file</span></span>  <br/> |<span data-ttu-id="401ec-122">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="401ec-122">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="401ec-123">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="401ec-123">Can be empty</span></span>  <br/> |<span data-ttu-id="401ec-124">false</span><span class="sxs-lookup"><span data-stu-id="401ec-124">false</span></span>  <br/> |
   

