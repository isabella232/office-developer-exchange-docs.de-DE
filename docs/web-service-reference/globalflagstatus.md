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
description: Das GlobalFlagStatus-Element enthält den aggregierten Kennzeichen Status für alle Unterhaltungselemente in einem Postfach.
ms.openlocfilehash: f9984a1bb7e8205a98dd3ef91f841b48a7ab9389
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459504"
---
# <a name="globalflagstatus"></a><span data-ttu-id="01087-103">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="01087-103">GlobalFlagStatus</span></span>

<span data-ttu-id="01087-104">Das **GlobalFlagStatus** -Element enthält den aggregierten Kennzeichen Status für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="01087-104">The **GlobalFlagStatus** element contains the aggregated flag status for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="01087-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="01087-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="01087-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="01087-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="01087-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="01087-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="01087-108">GlobalFlagStatus</span><span class="sxs-lookup"><span data-stu-id="01087-108">GlobalFlagStatus</span></span>](globalflagstatus.md)
  
```XML
<GlobalFlagStatus> NotFlagged | Flagged | Complete </GlobalFlagStatus>
```

 <span data-ttu-id="01087-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="01087-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="01087-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="01087-110">Attributes and elements</span></span>

<span data-ttu-id="01087-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="01087-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="01087-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="01087-112">Attributes</span></span>

<span data-ttu-id="01087-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="01087-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="01087-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01087-114">Child elements</span></span>

<span data-ttu-id="01087-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="01087-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="01087-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="01087-116">Parent elements</span></span>

|<span data-ttu-id="01087-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="01087-117">**Element**</span></span>|<span data-ttu-id="01087-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="01087-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="01087-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="01087-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="01087-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="01087-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="01087-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="01087-121">Text value</span></span>

<span data-ttu-id="01087-122">Der Textwert des **GlobalFlagStatus** -Elements ist der aggregierte Kennzeichnungsstatus für Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="01087-122">The text value of the **GlobalFlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="01087-123">Im folgenden sind die möglichen Text Werte zu finden:</span><span class="sxs-lookup"><span data-stu-id="01087-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="01087-124">**NotFlagged** – gibt den Status nicht gekennzeichnet an.</span><span class="sxs-lookup"><span data-stu-id="01087-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="01087-125">**Gekennzeichnet** – gibt den gekennzeichneten Status an.</span><span class="sxs-lookup"><span data-stu-id="01087-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="01087-126">**Complete** – gibt den vollständigen Kennzeichen Status an.</span><span class="sxs-lookup"><span data-stu-id="01087-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="01087-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="01087-127">Remarks</span></span>

<span data-ttu-id="01087-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="01087-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="01087-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="01087-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="01087-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="01087-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="01087-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="01087-131">Schema name</span></span>  <br/> |<span data-ttu-id="01087-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="01087-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="01087-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="01087-133">Validation file</span></span>  <br/> |<span data-ttu-id="01087-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="01087-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="01087-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="01087-135">Can be empty</span></span>  <br/> |<span data-ttu-id="01087-136">False</span><span class="sxs-lookup"><span data-stu-id="01087-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="01087-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="01087-137">See also</span></span>



[<span data-ttu-id="01087-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="01087-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="01087-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="01087-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="01087-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="01087-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

