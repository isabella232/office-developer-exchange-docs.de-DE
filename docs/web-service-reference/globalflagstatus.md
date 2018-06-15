---
title: GlobalFlagStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalFlagStatus
api_type:
- schema
ms.assetid: 3ba300f3-3355-4cab-9e77-0dcc2902e712
description: Das GlobalFlagStatus-Element enthält den aggregierten Kennzeichnungsstatus für alle Unterhaltungselemente in einem Postfach.
ms.openlocfilehash: 0c560c065463b8b619f96ecef73d1120b216ca35
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/15/2018
ms.locfileid: "19829713"
---
# <a name="globalflagstatus"></a><span data-ttu-id="42be9-103">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="42be9-103">GlobalFlagStatus</span></span>

<span data-ttu-id="42be9-104">Das **GlobalFlagStatus** -Element enthält den aggregierten Kennzeichnungsstatus für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="42be9-104">The **GlobalFlagStatus** element contains the aggregated flag status for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="42be9-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="42be9-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="42be9-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="42be9-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="42be9-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="42be9-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="42be9-108">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="42be9-108">GlobalFlagStatus</span></span>](globalflagstatus.md)
  
```XML
<GlobalFlagStatus> NotFlagged | Flagged | Complete </GlobalFlagStatus>
```

 <span data-ttu-id="42be9-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="42be9-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="42be9-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="42be9-110">Attributes and elements</span></span>

<span data-ttu-id="42be9-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="42be9-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="42be9-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="42be9-112">Attributes</span></span>

<span data-ttu-id="42be9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="42be9-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="42be9-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42be9-114">Child elements</span></span>

<span data-ttu-id="42be9-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="42be9-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="42be9-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="42be9-116">Parent elements</span></span>

|<span data-ttu-id="42be9-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="42be9-117">**Element**</span></span>|<span data-ttu-id="42be9-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="42be9-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="42be9-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="42be9-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="42be9-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="42be9-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="42be9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="42be9-121">Text value</span></span>

<span data-ttu-id="42be9-122">Der Textwert des **GlobalFlagStatus** -Elements ist die aggregierten Kennzeichnungsstatus Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="42be9-122">The text value of the **GlobalFlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="42be9-123">Im folgenden sind die möglichen Textwerte:</span><span class="sxs-lookup"><span data-stu-id="42be9-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="42be9-124">**NotFlagged** - gibt den Status wird nicht gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="42be9-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="42be9-125">**Flagged** - gibt den gekennzeichneten Status.</span><span class="sxs-lookup"><span data-stu-id="42be9-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="42be9-126">**Complete** – gibt die vollständige Kennzeichnungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="42be9-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="42be9-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="42be9-127">Remarks</span></span>

<span data-ttu-id="42be9-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="42be9-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="42be9-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="42be9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="42be9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="42be9-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="42be9-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="42be9-131">Schema name</span></span>  <br/> |<span data-ttu-id="42be9-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="42be9-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="42be9-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="42be9-133">Validation file</span></span>  <br/> |<span data-ttu-id="42be9-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="42be9-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="42be9-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="42be9-135">Can be empty</span></span>  <br/> |<span data-ttu-id="42be9-136">False</span><span class="sxs-lookup"><span data-stu-id="42be9-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="42be9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="42be9-137">See also</span></span>



[<span data-ttu-id="42be9-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="42be9-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="42be9-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="42be9-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="42be9-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="42be9-140">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

