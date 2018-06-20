---
title: FlagStatus
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FlagStatus
api_type:
- schema
ms.assetid: d5907ec5-3a60-4d83-bf85-406c54f95eb7
description: Das FlagStatus-Element enthält den aggregierten Kennzeichnungsstatus Unterhaltungselementen im aktuellen Ordner.
ms.openlocfilehash: 59e071cbd402c49f4dcc4370059883f3f45409ae
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758496"
---
# <a name="flagstatus"></a><span data-ttu-id="de9b2-103">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="de9b2-103">FlagStatus</span></span>

<span data-ttu-id="de9b2-104">Das **FlagStatus** -Element enthält den aggregierten Kennzeichnungsstatus Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="de9b2-104">The **FlagStatus** element contains the aggregated flag status for conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="de9b2-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="de9b2-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="de9b2-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="de9b2-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="de9b2-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="de9b2-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="de9b2-108">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="de9b2-108">FlagStatus</span></span>](flagstatus.md)
  
```XML
<FlagStatus> NotFlagged | Flagged | Complete </FlagStatus>
```

 <span data-ttu-id="de9b2-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="de9b2-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de9b2-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="de9b2-110">Attributes and elements</span></span>

<span data-ttu-id="de9b2-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="de9b2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de9b2-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="de9b2-112">Attributes</span></span>

<span data-ttu-id="de9b2-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="de9b2-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de9b2-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de9b2-114">Child elements</span></span>

<span data-ttu-id="de9b2-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="de9b2-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="de9b2-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de9b2-116">Parent elements</span></span>

|<span data-ttu-id="de9b2-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="de9b2-117">**Element**</span></span>|<span data-ttu-id="de9b2-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de9b2-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de9b2-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="de9b2-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="de9b2-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="de9b2-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="de9b2-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="de9b2-121">Text value</span></span>

<span data-ttu-id="de9b2-122">Der Textwert des **FlagStatus** -Elements ist die aggregierten Kennzeichnungsstatus Unterhaltungselementen im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="de9b2-122">The text value of the **FlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="de9b2-123">Im folgenden sind die möglichen Textwerte:</span><span class="sxs-lookup"><span data-stu-id="de9b2-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="de9b2-124">**NotFlagged** - gibt den Status wird nicht gekennzeichnet.</span><span class="sxs-lookup"><span data-stu-id="de9b2-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="de9b2-125">**Flagged** - gibt den gekennzeichneten Status.</span><span class="sxs-lookup"><span data-stu-id="de9b2-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="de9b2-126">**Complete** – gibt die vollständige Kennzeichnungsstatus an.</span><span class="sxs-lookup"><span data-stu-id="de9b2-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="de9b2-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="de9b2-127">Remarks</span></span>

<span data-ttu-id="de9b2-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="de9b2-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de9b2-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="de9b2-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de9b2-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="de9b2-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de9b2-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="de9b2-131">Schema name</span></span>  <br/> |<span data-ttu-id="de9b2-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="de9b2-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="de9b2-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="de9b2-133">Validation file</span></span>  <br/> |<span data-ttu-id="de9b2-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de9b2-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de9b2-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="de9b2-135">Can be empty</span></span>  <br/> |<span data-ttu-id="de9b2-136">False</span><span class="sxs-lookup"><span data-stu-id="de9b2-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de9b2-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de9b2-137">See also</span></span>



[<span data-ttu-id="de9b2-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="de9b2-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="de9b2-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="de9b2-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="de9b2-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="de9b2-140">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

