---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: Das SearchItemKind-Element gibt den Typ der Elemente, die für einen Vorgang FindMailboxStatisticsByKeyword durchsucht werden.
ms.openlocfilehash: 1c099fc49ec882c1672b265ff0e3aa2c71c5f95b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831298"
---
# <a name="searchitemkind"></a><span data-ttu-id="633e3-103">SearchItemKind</span><span class="sxs-lookup"><span data-stu-id="633e3-103">SearchItemKind</span></span>

<span data-ttu-id="633e3-104">Das **SearchItemKind** -Element gibt den Typ der Elemente, die für einen Vorgang **FindMailboxStatisticsByKeyword** durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-104">The **SearchItemKind** element indicates the type of items that are searched for a **FindMailboxStatisticsByKeyword** operation.</span></span> 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 <span data-ttu-id="633e3-105">**SearchItemKindType**</span><span class="sxs-lookup"><span data-stu-id="633e3-105">**SearchItemKindType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="633e3-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="633e3-106">Attributes and elements</span></span>

<span data-ttu-id="633e3-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="633e3-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="633e3-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="633e3-108">Attributes</span></span>

<span data-ttu-id="633e3-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="633e3-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="633e3-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="633e3-110">Child elements</span></span>

<span data-ttu-id="633e3-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="633e3-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="633e3-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="633e3-112">Parent elements</span></span>

[<span data-ttu-id="633e3-113">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="633e3-113">MessageTypes</span></span>](messagetypes.md)
  
## <a name="text-value"></a><span data-ttu-id="633e3-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="633e3-114">Text value</span></span>

<span data-ttu-id="633e3-115">Der Textwert des **SearchItemKind** -Elements ist der Typ des Elements, die nach Schlüsselwörtern durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="633e3-115">The text value of the **SearchItemKind** element is the type of item that is searched for keywords.</span></span> <span data-ttu-id="633e3-116">Die folgende Liste enthält die Textwerte, die im **SearchItemKind** -Element verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="633e3-116">The following list contains the text values that can be used in the **SearchItemKind** element.</span></span> 
  
- <span data-ttu-id="633e3-117">**E-Mail** – gibt an, dass e-Mail-Nachrichten nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-117">**Email** - Indicates that email messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-118">**Besprechungen** - gibt an, dass Besprechungen nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-118">**Meetings** - Indicates that meetings are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-119">**Aufgaben** - gibt an, dass Aufgaben nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-119">**Tasks** - Indicates that tasks are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-120">**Notes** - gibt an, dass Notizen nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-120">**Notes** - Indicates that notes are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-121">**Dokumente** – gibt an, dass Dokumente nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-121">**Docs** - Indicates that documents are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-122">**Journale** - gibt an, dass Journale nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-122">**Journals** - Indicates that journals are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-123">**Kontakte** – gibt an, dass Kontakte nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-123">**Contacts** - Indicates that contacts are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-124">**Instant Messaging** - gibt an, dass Sofortnachrichten nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-124">**Im** - Indicates that instant messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-125">**Voicemail** - gibt an, dass Voicemails nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-125">**Voicemail** - Indicates that voice mails are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-126">**Faxe** - gibt an, dass Faxe nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-126">**Faxes** - Indicates that faxes are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-127">**Beiträge** – gibt an, dass Beiträge nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-127">**Posts** - Indicates that posts are searched for keywords.</span></span> 
    
- <span data-ttu-id="633e3-128">**Rssfeeds** - gibt an, dass RSS-Feeds für Schlüsselwörter durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="633e3-128">**Rssfeeds** - Indicates that RSS feeds are searched for keywords.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="633e3-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="633e3-129">Remarks</span></span>

<span data-ttu-id="633e3-130">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="633e3-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="633e3-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="633e3-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="633e3-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="633e3-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="633e3-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="633e3-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="633e3-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="633e3-134">Schema name</span></span>  <br/> |<span data-ttu-id="633e3-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="633e3-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="633e3-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="633e3-136">Validation file</span></span>  <br/> |<span data-ttu-id="633e3-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="633e3-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="633e3-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="633e3-138">Can be empty</span></span>  <br/> ||
   

