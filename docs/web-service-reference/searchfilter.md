---
title: SearchFilter
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 1a7ee364-b7da-4197-aab2-57134537109a
description: Das SearchFilter-Element enthält die Abfragezeichenfolge zum Filtern der Postfächer aus einer GetSearchableMailboxes Anforderung zurückgegeben werden soll.
ms.openlocfilehash: b71d8dd862e9338afc145545df4cd29e8bcc3dc8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831285"
---
# <a name="searchfilter"></a><span data-ttu-id="b5feb-103">SearchFilter</span><span class="sxs-lookup"><span data-stu-id="b5feb-103">SearchFilter</span></span>

<span data-ttu-id="b5feb-104">Das **SearchFilter** -Element enthält die Abfragezeichenfolge zum Filtern der Postfächer aus einer **GetSearchableMailboxes** Anforderung zurückgegeben werden soll.</span><span class="sxs-lookup"><span data-stu-id="b5feb-104">The **SearchFilter** element contains the query string to filter the mailboxes to be returned from a **GetSearchableMailboxes** request.</span></span> 
  
```XML
<SearchFilter></SearchFilter>
```

 <span data-ttu-id="b5feb-105">**string**</span><span class="sxs-lookup"><span data-stu-id="b5feb-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b5feb-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b5feb-106">Attributes and elements</span></span>

<span data-ttu-id="b5feb-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b5feb-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b5feb-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b5feb-108">Attributes</span></span>

<span data-ttu-id="b5feb-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5feb-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b5feb-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5feb-110">Child elements</span></span>

<span data-ttu-id="b5feb-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="b5feb-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="b5feb-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b5feb-112">Parent elements</span></span>

[<span data-ttu-id="b5feb-113">GetSearchableMailboxes</span><span class="sxs-lookup"><span data-stu-id="b5feb-113">GetSearchableMailboxes</span></span>](getsearchablemailboxes.md)
  
## <a name="text-value"></a><span data-ttu-id="b5feb-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="b5feb-114">Text value</span></span>

<span data-ttu-id="b5feb-115">Der Textwert des **SearchFilter** -Elements ist eine Abfragezeichenfolge an Filter Postfächer für Discovery-Suche.</span><span class="sxs-lookup"><span data-stu-id="b5feb-115">The text value of the **SearchFilter** element is a query string to filter mailboxes for discovery search.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="b5feb-116">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b5feb-116">Remarks</span></span>

<span data-ttu-id="b5feb-117">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="b5feb-117">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="b5feb-118">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="b5feb-118">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b5feb-119">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b5feb-119">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b5feb-120">Namespace</span><span class="sxs-lookup"><span data-stu-id="b5feb-120">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="b5feb-121">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b5feb-121">Schema name</span></span>  <br/> |<span data-ttu-id="b5feb-122">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="b5feb-122">Messages schema</span></span>  <br/> |
|<span data-ttu-id="b5feb-123">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b5feb-123">Validation file</span></span>  <br/> |<span data-ttu-id="b5feb-124">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="b5feb-124">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="b5feb-125">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b5feb-125">Can be empty</span></span>  <br/> ||
   

