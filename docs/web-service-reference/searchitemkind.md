---
title: SearchItemKind
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 89513c26-b751-4619-a300-0ed8f55b0102
description: Das SearchItemKind-Element gibt den Typ der Elemente an, die nach einer FindMailboxStatisticsByKeyword-Operation durchsucht werden.
ms.openlocfilehash: e0625ac169c3083702494c094da15d38d220fe67
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44464000"
---
# <a name="searchitemkind"></a><span data-ttu-id="f9f4c-103">SearchItemKind</span><span class="sxs-lookup"><span data-stu-id="f9f4c-103">SearchItemKind</span></span>

<span data-ttu-id="f9f4c-104">Das **SearchItemKind** -Element gibt den Typ der Elemente an, die nach einer **FindMailboxStatisticsByKeyword** -Operation durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-104">The **SearchItemKind** element indicates the type of items that are searched for a **FindMailboxStatisticsByKeyword** operation.</span></span> 
  
```XML
<SearchItemKind>Email | Meetings | Tasks | Notes | Docs | Journals | Contacts | Im | Voicemail | Faxes | Posts | Rssfeeds</SearchItemKind>
```

 <span data-ttu-id="f9f4c-105">**SearchItemKindType**</span><span class="sxs-lookup"><span data-stu-id="f9f4c-105">**SearchItemKindType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f9f4c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f9f4c-106">Attributes and elements</span></span>

<span data-ttu-id="f9f4c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f9f4c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f9f4c-108">Attributes</span></span>

<span data-ttu-id="f9f4c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f9f4c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9f4c-110">Child elements</span></span>

<span data-ttu-id="f9f4c-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f9f4c-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f9f4c-112">Parent elements</span></span>

[<span data-ttu-id="f9f4c-113">MessageTypes</span><span class="sxs-lookup"><span data-stu-id="f9f4c-113">MessageTypes</span></span>](messagetypes.md)
  
## <a name="text-value"></a><span data-ttu-id="f9f4c-114">Textwert</span><span class="sxs-lookup"><span data-stu-id="f9f4c-114">Text value</span></span>

<span data-ttu-id="f9f4c-115">Der Textwert des **SearchItemKind** -Elements ist der Typ des Elements, das nach Schlüsselwörtern durchsucht wird.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-115">The text value of the **SearchItemKind** element is the type of item that is searched for keywords.</span></span> <span data-ttu-id="f9f4c-116">Die folgende Liste enthält die Text Werte, die im **SearchItemKind** -Element verwendet werden können.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-116">The following list contains the text values that can be used in the **SearchItemKind** element.</span></span> 
  
- <span data-ttu-id="f9f4c-117">**E-Mail** : gibt an, dass e-Mail-Nachrichten nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-117">**Email** - Indicates that email messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-118">**Besprechungen** – gibt an, dass Besprechungen nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-118">**Meetings** - Indicates that meetings are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-119">**Aufgaben** : gibt an, dass Aufgaben nach Schlüsselwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-119">**Tasks** - Indicates that tasks are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-120">**Hinweise** : gibt an, dass Notizen nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-120">**Notes** - Indicates that notes are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-121">**Docs** : gibt an, dass Dokumente nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-121">**Docs** - Indicates that documents are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-122">**Journals** – gibt an, dass Journale nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-122">**Journals** - Indicates that journals are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-123">**Kontakte** : gibt an, dass Kontakte nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-123">**Contacts** - Indicates that contacts are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-124">**Sofortnachrichten – gibt** an, dass Nachrichten nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-124">**Im** - Indicates that instant messages are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-125">**Voicemail** : gibt an, dass Voicemails nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-125">**Voicemail** - Indicates that voice mails are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-126">**Faxnachrichten** – gibt an, dass Faxnachrichten nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-126">**Faxes** - Indicates that faxes are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-127">**Beiträge** : gibt an, dass Beiträge nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-127">**Posts** - Indicates that posts are searched for keywords.</span></span> 
    
- <span data-ttu-id="f9f4c-128">**RSSfeeds** – gibt an, dass RSS-Feeds nach Stichwörtern durchsucht werden.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-128">**Rssfeeds** - Indicates that RSS feeds are searched for keywords.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f9f4c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f9f4c-129">Remarks</span></span>

<span data-ttu-id="f9f4c-130">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-130">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="f9f4c-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="f9f4c-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f9f4c-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f9f4c-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f9f4c-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="f9f4c-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f9f4c-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f9f4c-134">Schema name</span></span>  <br/> |<span data-ttu-id="f9f4c-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f9f4c-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="f9f4c-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f9f4c-136">Validation file</span></span>  <br/> |<span data-ttu-id="f9f4c-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f9f4c-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f9f4c-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f9f4c-138">Can be empty</span></span>  <br/> ||
   

