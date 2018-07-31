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
ms.openlocfilehash: 42484c8deecb106e05023215342af3c7d996d852
ms.sourcegitcommit: 9061fcf40c218ebe88911783f357b7df278846db
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 07/28/2018
ms.locfileid: "21353511"
---
# <a name="itemchange"></a><span data-ttu-id="baffd-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="baffd-103">ItemChange</span></span>

<span data-ttu-id="baffd-104">Das **ItemChange** -Element enthält eine Element-ID und die Updates auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="baffd-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
- [<span data-ttu-id="baffd-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="baffd-105">UpdateItem</span></span>](updateitem.md) 
- [<span data-ttu-id="baffd-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="baffd-106">ItemChanges</span></span>](itemchanges.md)
- [<span data-ttu-id="baffd-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="baffd-107">ItemChange</span></span>](itemchange.md)
  
```xml
<ItemChange>
   <ItemId/>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <OccurrenceItemId>...</OccurrenceItemId>
   <Updates>...</Updates>
</ItemChange>
```

```xml
<ItemChange>
   <RecurringMasterItemId>...</RecurringMasterItemId>
   <Updates>...</Updates>
</ItemChange>
```

<span data-ttu-id="baffd-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="baffd-108">**ItemChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="baffd-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="baffd-109">Attributes and elements</span></span>

<span data-ttu-id="baffd-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="baffd-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="baffd-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="baffd-111">Attributes</span></span>

<span data-ttu-id="baffd-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="baffd-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="baffd-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="baffd-113">Child elements</span></span>

|<span data-ttu-id="baffd-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="baffd-114">**Element**</span></span>|<span data-ttu-id="baffd-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="baffd-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baffd-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="baffd-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="baffd-117">Enthält den eindeutigen Bezeichner und Ändern eines Elements in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="baffd-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="baffd-118">Dieses Element ist erforderlich, wenn das Element [OccurrenceItemId](occurrenceitemid.md) oder [RecurringMasterItemId](recurringmasteritemid.md) nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="baffd-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="baffd-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="baffd-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="baffd-120">Gibt ein einzelnes Vorkommen des eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="baffd-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="baffd-121">Dieses Element ist erforderlich, wenn verwendet.</span><span class="sxs-lookup"><span data-stu-id="baffd-121">This element is required if used.</span></span> <span data-ttu-id="baffd-122">Dieses Element ist erforderlich, wenn das Element [RecurringMasterItemId](recurringmasteritemid.md) oder [ItemId](itemid.md) nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="baffd-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="baffd-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="baffd-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="baffd-124">Gibt ein Master-Shape Recurrence-Element durch das Identifizieren von seine Vorkommen verwandte Elemente-Bezeichner.</span><span class="sxs-lookup"><span data-stu-id="baffd-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="baffd-125">Dieses Element ist erforderlich, wenn verwendet.</span><span class="sxs-lookup"><span data-stu-id="baffd-125">This element is required if used.</span></span> <span data-ttu-id="baffd-126">Dieses Element ist erforderlich, wenn das Element [OccurrenceItemId](occurrenceitemid.md) oder [ItemId](itemid.md) nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="baffd-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="baffd-127">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="baffd-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="baffd-128">Enthält ein Array, definiert anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="baffd-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="baffd-129">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="baffd-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="baffd-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="baffd-130">Parent elements</span></span>

|<span data-ttu-id="baffd-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="baffd-131">**Element**</span></span>|<span data-ttu-id="baffd-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="baffd-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="baffd-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="baffd-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="baffd-134">Enthält ein Array von [ItemChange](itemchange.md) -Elementen, die Elemente und die Updates auf Elemente anwenden zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="baffd-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="baffd-135">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="baffd-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="baffd-136">Hinweise</span><span class="sxs-lookup"><span data-stu-id="baffd-136">Remarks</span></span>

<span data-ttu-id="baffd-137">In einem **ItemChange** -Element kann nur ein einzelnes Element [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)oder [RecurringMasterItemId](recurringmasteritemid.md) verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="baffd-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="baffd-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="baffd-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="baffd-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="baffd-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="baffd-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="baffd-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="baffd-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="baffd-141">Schema Name</span></span>  <br/> |<span data-ttu-id="baffd-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="baffd-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="baffd-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="baffd-143">Validation File</span></span>  <br/> |<span data-ttu-id="baffd-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="baffd-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="baffd-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="baffd-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="baffd-146">False</span><span class="sxs-lookup"><span data-stu-id="baffd-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="baffd-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="baffd-147">See also</span></span>

- [<span data-ttu-id="baffd-148">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="baffd-148">UpdateItem operation</span></span>](updateitem-operation.md)

