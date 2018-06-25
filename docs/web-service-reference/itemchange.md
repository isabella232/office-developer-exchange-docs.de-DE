---
title: ItemChange
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ItemChange
api_type:
- schema
ms.assetid: 5cb43b02-d444-4d9c-9075-cdc5a4427daf
description: Das ItemChange-Element enthält eine Element-ID und die Updates auf das Element anwenden.
ms.openlocfilehash: d10ce96cacb0be7411c4e8230ebc9b2803b7a5b1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830145"
---
# <a name="itemchange"></a><span data-ttu-id="d0582-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="d0582-103">ItemChange</span></span>

<span data-ttu-id="d0582-104">Das **ItemChange** -Element enthält eine Element-ID und die Updates auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="d0582-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
[<span data-ttu-id="d0582-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="d0582-105">UpdateItem</span></span>](updateitem.md)
  
[<span data-ttu-id="d0582-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="d0582-106">ItemChanges</span></span>](itemchanges.md)
  
[<span data-ttu-id="d0582-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="d0582-107">ItemChange</span></span>](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

 <span data-ttu-id="d0582-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="d0582-108">**ItemChangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d0582-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d0582-109">Attributes and elements</span></span>

<span data-ttu-id="d0582-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d0582-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d0582-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="d0582-111">Attributes</span></span>

<span data-ttu-id="d0582-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="d0582-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d0582-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0582-113">Child elements</span></span>

|<span data-ttu-id="d0582-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0582-114">**Element**</span></span>|<span data-ttu-id="d0582-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0582-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0582-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="d0582-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="d0582-117">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="d0582-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="d0582-118">Dieses Element ist erforderlich, wenn das Element [OccurrenceItemId](occurrenceitemid.md) oder [RecurringMasterItemId](recurringmasteritemid.md) nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0582-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="d0582-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="d0582-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="d0582-120">Gibt ein einzelnes Vorkommen des eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="d0582-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="d0582-121">Dieses Element ist erforderlich, wenn verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0582-121">This element is required if used.</span></span> <span data-ttu-id="d0582-122">Dieses Element ist erforderlich, wenn das Element [RecurringMasterItemId](recurringmasteritemid.md) oder [ItemId](itemid.md) nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0582-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="d0582-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="d0582-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="d0582-124">Gibt ein Master-Shape Recurrence-Element durch das Identifizieren von seine Vorkommen verwandte Elemente-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="d0582-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="d0582-125">Dieses Element ist erforderlich, wenn verwendet.</span><span class="sxs-lookup"><span data-stu-id="d0582-125">This element is required if used.</span></span> <span data-ttu-id="d0582-126">Dieses Element ist erforderlich, wenn das Element [OccurrenceItemId](occurrenceitemid.md) oder [ItemId](itemid.md) nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="d0582-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="d0582-127">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="d0582-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="d0582-128">Enthält ein Array, definiert anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="d0582-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="d0582-129">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d0582-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d0582-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d0582-130">Parent elements</span></span>

|<span data-ttu-id="d0582-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="d0582-131">**Element**</span></span>|<span data-ttu-id="d0582-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d0582-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d0582-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="d0582-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="d0582-134">Enthält ein Array von [ItemChange](itemchange.md) -Elementen, die Elemente und die Updates auf Elemente anwenden zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="d0582-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="d0582-135">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="d0582-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d0582-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="d0582-136">Remarks</span></span>

<span data-ttu-id="d0582-137">In einem **ItemChange** -Element kann nur ein einzelnes Element [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)oder [RecurringMasterItemId](recurringmasteritemid.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="d0582-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="d0582-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d0582-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d0582-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="d0582-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d0582-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="d0582-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d0582-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d0582-141">Schema Name</span></span>  <br/> |<span data-ttu-id="d0582-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d0582-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="d0582-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d0582-143">Validation File</span></span>  <br/> |<span data-ttu-id="d0582-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d0582-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d0582-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d0582-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="d0582-146">False</span><span class="sxs-lookup"><span data-stu-id="d0582-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d0582-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d0582-147">See also</span></span>



[<span data-ttu-id="d0582-148">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="d0582-148">UpdateItem operation</span></span>](updateitem-operation.md)

