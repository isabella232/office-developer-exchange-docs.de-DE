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
description: Das FlagStatus-Element enthält den aggregierten Kennzeichen Status für Unterhaltungselemente im aktuellen Ordner.
ms.openlocfilehash: e65849c4909292c07450f8578fe7a7065c98ab44
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466213"
---
# <a name="flagstatus"></a><span data-ttu-id="40551-103">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="40551-103">FlagStatus</span></span>

<span data-ttu-id="40551-104">Das **FlagStatus** -Element enthält den aggregierten Kennzeichen Status für Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="40551-104">The **FlagStatus** element contains the aggregated flag status for conversation items in the current folder.</span></span> 
  
[<span data-ttu-id="40551-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="40551-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="40551-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="40551-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="40551-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="40551-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="40551-108">FlagStatus</span><span class="sxs-lookup"><span data-stu-id="40551-108">FlagStatus</span></span>](flagstatus.md)
  
```XML
<FlagStatus> NotFlagged | Flagged | Complete </FlagStatus>
```

 <span data-ttu-id="40551-109">**FlagStatusType**</span><span class="sxs-lookup"><span data-stu-id="40551-109">**FlagStatusType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="40551-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="40551-110">Attributes and elements</span></span>

<span data-ttu-id="40551-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="40551-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="40551-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="40551-112">Attributes</span></span>

<span data-ttu-id="40551-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="40551-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="40551-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40551-114">Child elements</span></span>

<span data-ttu-id="40551-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="40551-115">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="40551-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="40551-116">Parent elements</span></span>

|<span data-ttu-id="40551-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="40551-117">**Element**</span></span>|<span data-ttu-id="40551-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="40551-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="40551-119">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="40551-119">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="40551-120">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="40551-120">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="40551-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="40551-121">Text value</span></span>

<span data-ttu-id="40551-122">Der Textwert des **FlagStatus** -Elements ist der aggregierte Kennzeichnungsstatus für Unterhaltungselemente im aktuellen Ordner.</span><span class="sxs-lookup"><span data-stu-id="40551-122">The text value of the **FlagStatus** element is the aggregated flag status for conversation items in the current folder.</span></span> <span data-ttu-id="40551-123">Im folgenden sind die möglichen Text Werte zu finden:</span><span class="sxs-lookup"><span data-stu-id="40551-123">The following are the possible text values:</span></span> 
  
- <span data-ttu-id="40551-124">**NotFlagged** – gibt den Status nicht gekennzeichnet an.</span><span class="sxs-lookup"><span data-stu-id="40551-124">**NotFlagged** - Indicates the not-flagged status.</span></span> 
    
- <span data-ttu-id="40551-125">**Gekennzeichnet** – gibt den gekennzeichneten Status an.</span><span class="sxs-lookup"><span data-stu-id="40551-125">**Flagged** - Indicates the flagged status.</span></span> 
    
- <span data-ttu-id="40551-126">**Complete** – gibt den vollständigen Kennzeichen Status an.</span><span class="sxs-lookup"><span data-stu-id="40551-126">**Complete** - Indicates the complete flag status.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="40551-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="40551-127">Remarks</span></span>

<span data-ttu-id="40551-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="40551-128">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="40551-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="40551-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="40551-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="40551-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="40551-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="40551-131">Schema name</span></span>  <br/> |<span data-ttu-id="40551-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="40551-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="40551-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="40551-133">Validation file</span></span>  <br/> |<span data-ttu-id="40551-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="40551-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="40551-135">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="40551-135">Can be empty</span></span>  <br/> |<span data-ttu-id="40551-136">False</span><span class="sxs-lookup"><span data-stu-id="40551-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="40551-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="40551-137">See also</span></span>



[<span data-ttu-id="40551-138">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="40551-138">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="40551-139">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="40551-139">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="40551-140">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="40551-140">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

