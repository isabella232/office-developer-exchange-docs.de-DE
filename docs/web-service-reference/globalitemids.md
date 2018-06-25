---
title: GlobalItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GlobalItemIds
api_type:
- schema
ms.assetid: b0f03ce0-a4c3-47de-9360-a880a3606e42
description: Das GlobalItemIds-Element enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach.
ms.openlocfilehash: 064ebc4c612aaf569eafa56e57a27cf7153f2130
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829737"
---
# <a name="globalitemids"></a><span data-ttu-id="1a484-103">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="1a484-103">GlobalItemIds</span></span>

<span data-ttu-id="1a484-104">Das **GlobalItemIds** -Element enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="1a484-104">The **GlobalItemIds** element contains the collection of item identifiers for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="1a484-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="1a484-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="1a484-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="1a484-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="1a484-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="1a484-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="1a484-108">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="1a484-108">GlobalItemIds</span></span>](globalitemids.md)
  
```XML
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

 <span data-ttu-id="1a484-109">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="1a484-109">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1a484-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1a484-110">Attributes and elements</span></span>

<span data-ttu-id="1a484-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1a484-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1a484-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="1a484-112">Attributes</span></span>

<span data-ttu-id="1a484-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a484-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1a484-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a484-114">Child elements</span></span>

|<span data-ttu-id="1a484-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a484-115">**Element**</span></span>|<span data-ttu-id="1a484-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a484-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a484-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="1a484-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="1a484-118">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="1a484-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="1a484-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="1a484-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="1a484-120">Gibt ein einzelnes Vorkommen des eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="1a484-120">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="1a484-121">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="1a484-121">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="1a484-122">Gibt ein Master-Shape Recurrence-Element durch das Identifizieren von seine Vorkommen verwandte Elemente-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="1a484-122">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1a484-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1a484-123">Parent elements</span></span>

|<span data-ttu-id="1a484-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="1a484-124">**Element**</span></span>|<span data-ttu-id="1a484-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1a484-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1a484-126">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="1a484-126">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="1a484-127">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="1a484-127">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1a484-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="1a484-128">Text value</span></span>

<span data-ttu-id="1a484-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="1a484-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="1a484-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1a484-130">Remarks</span></span>

<span data-ttu-id="1a484-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="1a484-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1a484-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1a484-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1a484-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="1a484-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1a484-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1a484-134">Schema name</span></span>  <br/> |<span data-ttu-id="1a484-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1a484-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="1a484-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1a484-136">Validation file</span></span>  <br/> |<span data-ttu-id="1a484-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1a484-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1a484-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="1a484-138">Can be empty</span></span>  <br/> |<span data-ttu-id="1a484-139">False</span><span class="sxs-lookup"><span data-stu-id="1a484-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1a484-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1a484-140">See also</span></span>



[<span data-ttu-id="1a484-141">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="1a484-141">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="1a484-142">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1a484-142">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="1a484-143">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="1a484-143">Conversations in EWS</span></span>](http://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

