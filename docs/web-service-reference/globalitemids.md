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
description: Das GlobalItemIds-Element enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.
ms.openlocfilehash: aa656e7f2fb78dafe5bf6013c1f7ad14e2372ba1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459426"
---
# <a name="globalitemids"></a><span data-ttu-id="91200-103">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="91200-103">GlobalItemIds</span></span>

<span data-ttu-id="91200-104">Das **GlobalItemIds** -Element enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="91200-104">The **GlobalItemIds** element contains the collection of item identifiers for all conversation items in a mailbox.</span></span> 
  
[<span data-ttu-id="91200-105">FindConversationResponse</span><span class="sxs-lookup"><span data-stu-id="91200-105">FindConversationResponse</span></span>](findconversationresponse.md)
  
[<span data-ttu-id="91200-106">Conversations</span><span class="sxs-lookup"><span data-stu-id="91200-106">Conversations</span></span>](conversations-ex15websvcsotherref.md)
  
[<span data-ttu-id="91200-107">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="91200-107">Conversation (ConversationType)</span></span>](conversation-conversationtype.md)
  
[<span data-ttu-id="91200-108">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="91200-108">GlobalItemIds</span></span>](globalitemids.md)
  
```XML
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

 <span data-ttu-id="91200-109">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="91200-109">**NonEmptyArrayOfBaseItemIdsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="91200-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="91200-110">Attributes and elements</span></span>

<span data-ttu-id="91200-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="91200-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="91200-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="91200-112">Attributes</span></span>

<span data-ttu-id="91200-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="91200-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="91200-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91200-114">Child elements</span></span>

|<span data-ttu-id="91200-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="91200-115">**Element**</span></span>|<span data-ttu-id="91200-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91200-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91200-117">ItemId</span><span class="sxs-lookup"><span data-stu-id="91200-117">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="91200-118">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="91200-118">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="91200-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="91200-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="91200-120">Gibt ein einzelnes Vorkommen eines wiederkehrenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="91200-120">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="91200-121">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="91200-121">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="91200-122">Identifiziert ein Serienmasterelement durch Identifizieren eines der Bezeichner des zugehörigen vorkommen Elements.</span><span class="sxs-lookup"><span data-stu-id="91200-122">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="91200-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="91200-123">Parent elements</span></span>

|<span data-ttu-id="91200-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="91200-124">**Element**</span></span>|<span data-ttu-id="91200-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="91200-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="91200-126">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="91200-126">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="91200-127">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="91200-127">Represents a single conversation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="91200-128">Textwert</span><span class="sxs-lookup"><span data-stu-id="91200-128">Text value</span></span>

<span data-ttu-id="91200-129">Keine.</span><span class="sxs-lookup"><span data-stu-id="91200-129">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="91200-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="91200-130">Remarks</span></span>

<span data-ttu-id="91200-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.Dieses Element wurde in Exchange Server 2010 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="91200-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.This element was introduced in Exchange Server 2010 Service Pack 1 (SP1).</span></span>
  
## <a name="element-information"></a><span data-ttu-id="91200-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="91200-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="91200-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="91200-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="91200-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="91200-134">Schema name</span></span>  <br/> |<span data-ttu-id="91200-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="91200-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="91200-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="91200-136">Validation file</span></span>  <br/> |<span data-ttu-id="91200-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="91200-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="91200-138">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="91200-138">Can be empty</span></span>  <br/> |<span data-ttu-id="91200-139">False</span><span class="sxs-lookup"><span data-stu-id="91200-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="91200-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="91200-140">See also</span></span>



[<span data-ttu-id="91200-141">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="91200-141">FindConversation operation</span></span>](findconversation-operation.md)
  
[<span data-ttu-id="91200-142">ApplyConversationAction-Vorgang</span><span class="sxs-lookup"><span data-stu-id="91200-142">ApplyConversationAction operation</span></span>](applyconversationaction-operation.md)


[<span data-ttu-id="91200-143">Conversations in EWS</span><span class="sxs-lookup"><span data-stu-id="91200-143">Conversations in EWS</span></span>](https://msdn.microsoft.com/library/91e64629-db6c-4c94-9dcb-d386232e8467%28Office.15%29.aspx)

