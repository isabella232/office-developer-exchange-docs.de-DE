---
title: ItemIds
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemIds
api_type:
- schema
ms.assetid: 6b82122b-5544-4adf-91b7-ef2db7d5046f
description: Das Artikelnummern ein.-Element enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.
ms.openlocfilehash: 1bd4d6f4593a7c3b418561269d8b29707cc6030c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830155"
---
# <a name="itemids"></a><span data-ttu-id="a9dea-103">ItemIds</span><span class="sxs-lookup"><span data-stu-id="a9dea-103">ItemIds</span></span>
  
<span data-ttu-id="a9dea-104">Das **Artikelnummern ein.** -Element enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a9dea-104">The **ItemIds** element contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span>
  
```xml
<ItemIds>
   <ItemId/>
   <OccurrenceItemId/>
   <RecurringMasterItemId/>
</ItemIds>
```

<span data-ttu-id="a9dea-105">**NonEmptyArrayOfBaseItemIdsType**</span><span class="sxs-lookup"><span data-stu-id="a9dea-105">**NonEmptyArrayOfBaseItemIdsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="a9dea-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a9dea-106">Attributes and elements</span></span>

<span data-ttu-id="a9dea-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a9dea-107">The following sections describe attributes, child elements, and parent elements.</span></span> 
  
### <a name="attributes"></a><span data-ttu-id="a9dea-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a9dea-108">Attributes</span></span>

<span data-ttu-id="a9dea-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a9dea-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a9dea-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9dea-110">Child elements</span></span>

|<span data-ttu-id="a9dea-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9dea-111">**Element**</span></span>|<span data-ttu-id="a9dea-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9dea-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9dea-113">ItemId</span><span class="sxs-lookup"><span data-stu-id="a9dea-113">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="a9dea-114">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a9dea-114">Contains the unique identifier and change key of an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a9dea-115">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="a9dea-115">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="a9dea-116">Gibt ein einzelnes Vorkommen des eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="a9dea-116">Identifies a single occurrence of a recurring item.</span></span>  <br/> |
|[<span data-ttu-id="a9dea-117">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="a9dea-117">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="a9dea-118">Gibt ein Master-Shape Recurrence-Element durch das Identifizieren von seine Vorkommen verwandte Elemente-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="a9dea-118">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a9dea-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a9dea-119">Parent elements</span></span>

|<span data-ttu-id="a9dea-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a9dea-120">**Element**</span></span>|<span data-ttu-id="a9dea-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a9dea-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a9dea-122">Unterhaltung (ConversationType)</span><span class="sxs-lookup"><span data-stu-id="a9dea-122">Conversation (ConversationType)</span></span>](conversation-conversationtype.md) <br/> |<span data-ttu-id="a9dea-123">Stellt eine einfache Unterhaltung dar.</span><span class="sxs-lookup"><span data-stu-id="a9dea-123">Represents a single conversation.</span></span>  <br/> |
|[<span data-ttu-id="a9dea-124">DeleteItem</span><span class="sxs-lookup"><span data-stu-id="a9dea-124">DeleteItem</span></span>](deleteitem.md) <br/> |<span data-ttu-id="a9dea-125">Definiert eine Anforderung zum Löschen von Elementen im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a9dea-125">Defines a request to delete items in the Exchange store.</span></span>  <br/> <span data-ttu-id="a9dea-126">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a9dea-126">The following is the XPath expression to this element:</span></span>  <br/>  `/DeleteItem` <br/> |
|[<span data-ttu-id="a9dea-127">SendItem</span><span class="sxs-lookup"><span data-stu-id="a9dea-127">SendItem</span></span>](senditem.md) <br/> |<span data-ttu-id="a9dea-128">Das Stammelement, das eine Anforderung zum Senden von Elementen im Exchange-Speicher definiert.</span><span class="sxs-lookup"><span data-stu-id="a9dea-128">The root element that defines a request to send items in the Exchange store.</span></span>  <br/> <span data-ttu-id="a9dea-129">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a9dea-129">The following is the XPath expression to this element:</span></span>  <br/>  `/SendItem` <br/> |
|[<span data-ttu-id="a9dea-130">GetItem</span><span class="sxs-lookup"><span data-stu-id="a9dea-130">GetItem</span></span>](getitem.md) <br/> |<span data-ttu-id="a9dea-131">Definiert eine Anforderung zum Abrufen von Elementen aus dem Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a9dea-131">Defines a request to get items from the Exchange store.</span></span>  <br/> <span data-ttu-id="a9dea-132">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a9dea-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetItem` <br/> |
|[<span data-ttu-id="a9dea-133">MoveItem</span><span class="sxs-lookup"><span data-stu-id="a9dea-133">MoveItem</span></span>](moveitem.md) <br/> |<span data-ttu-id="a9dea-134">Definiert eine Anforderung an die Elemente im Exchange-Speicher zu verschieben.</span><span class="sxs-lookup"><span data-stu-id="a9dea-134">Defines a request to move items in the Exchange store.</span></span>  <br/> <span data-ttu-id="a9dea-135">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a9dea-135">The following is the XPath expression to this element:</span></span>  <br/>  `/MoveItem` <br/> |
|[<span data-ttu-id="a9dea-136">CopyItem</span><span class="sxs-lookup"><span data-stu-id="a9dea-136">CopyItem</span></span>](copyitem.md) <br/> |<span data-ttu-id="a9dea-137">Definiert eine Anforderung zum Kopieren von Elementen im Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="a9dea-137">Defines a request to copy items in the Exchange store.</span></span>  <br/> <span data-ttu-id="a9dea-138">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="a9dea-138">The following is the XPath expression to this element:</span></span>  <br/>  `/CopyItem` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a9dea-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="a9dea-139">Remarks</span></span>

<span data-ttu-id="a9dea-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="a9dea-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a9dea-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="a9dea-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a9dea-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="a9dea-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a9dea-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a9dea-143">Schema Name</span></span>  <br/> |<span data-ttu-id="a9dea-144">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a9dea-144">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a9dea-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a9dea-145">Validation File</span></span>  <br/> |<span data-ttu-id="a9dea-146">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="a9dea-146">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a9dea-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a9dea-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="a9dea-148">False</span><span class="sxs-lookup"><span data-stu-id="a9dea-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a9dea-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a9dea-149">See also</span></span>

- [<span data-ttu-id="a9dea-150">DeleteItem-Operation</span><span class="sxs-lookup"><span data-stu-id="a9dea-150">DeleteItem operation</span></span>](deleteitem-operation.md)
- [<span data-ttu-id="a9dea-151">SendItem Operation</span><span class="sxs-lookup"><span data-stu-id="a9dea-151">SendItem operation</span></span>](senditem-operation.md) 
- [<span data-ttu-id="a9dea-152">GetItem Operation</span><span class="sxs-lookup"><span data-stu-id="a9dea-152">GetItem operation</span></span>](getitem-operation.md)
- [<span data-ttu-id="a9dea-153">MoveItem Operation</span><span class="sxs-lookup"><span data-stu-id="a9dea-153">MoveItem operation</span></span>](moveitem-operation.md)
- [<span data-ttu-id="a9dea-154">CopyItem Operation</span><span class="sxs-lookup"><span data-stu-id="a9dea-154">CopyItem operation</span></span>](copyitem-operation.md)
- [<span data-ttu-id="a9dea-155">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="a9dea-155">FindConversation operation</span></span>](findconversation-operation.md)

