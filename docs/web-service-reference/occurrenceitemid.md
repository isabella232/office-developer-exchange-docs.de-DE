---
title: OccurrenceItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- OccurrenceItemId
api_type:
- schema
ms.assetid: 4a15bbc3-5b93-4193-b9ec-da32f0a9a552
description: Das OccurrenceItemId-Element gibt ein einzelnes Vorkommen des eine Terminserie.
ms.openlocfilehash: e3d7b6efc49775f54219ce0dc0ec39a34a95f8fd
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830639"
---
# <a name="occurrenceitemid"></a><span data-ttu-id="266a7-103">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="266a7-103">OccurrenceItemId</span></span>

<span data-ttu-id="266a7-104">Das **OccurrenceItemId** -Element gibt ein einzelnes Vorkommen des eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="266a7-104">The **OccurrenceItemId** element identifies a single occurrence of a recurring item.</span></span> 
  
```XML
<OccurrenceItemId RecurringMasterId="" ChangeKey="" InstanceIndex=""/>
```

<span data-ttu-id="266a7-105">**OccurrenceItemIdType**</span><span class="sxs-lookup"><span data-stu-id="266a7-105">**OccurrenceItemIdType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="266a7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="266a7-106">Attributes and elements</span></span>

<span data-ttu-id="266a7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="266a7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="266a7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="266a7-108">Attributes</span></span>

|<span data-ttu-id="266a7-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="266a7-109">**Attribute**</span></span>|<span data-ttu-id="266a7-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="266a7-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="266a7-111">**RecurringMasterId**</span><span class="sxs-lookup"><span data-stu-id="266a7-111">**RecurringMasterId**</span></span> <br/> |<span data-ttu-id="266a7-112">Identifiziert den wiederkehrenden Master-Objekt vom eine Terminserie.</span><span class="sxs-lookup"><span data-stu-id="266a7-112">Identifies the recurring master of a recurring item.</span></span> <span data-ttu-id="266a7-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="266a7-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="266a7-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="266a7-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="266a7-115">Identifiziert eine bestimmte Version von sich wiederholenden Master oder ein Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="266a7-115">Identifies a specific version of the recurring master or an item occurrence.</span></span> <span data-ttu-id="266a7-116">Wenn das wiederkehrende Master-Shape oder eine der Vorkommen ändern, ändert sich der **ChangeKey** .</span><span class="sxs-lookup"><span data-stu-id="266a7-116">If either the recurring master or any of its occurrences change, the **ChangeKey** changes.</span></span> <span data-ttu-id="266a7-117">Die **ChangeKey** entspricht der Vorgehensweise für das wiederkehrende Master-Shape und alle Vorkommen.</span><span class="sxs-lookup"><span data-stu-id="266a7-117">The **ChangeKey** is the same for the recurring master and all occurrences.</span></span>  <br/> |
|<span data-ttu-id="266a7-118">**InstanceIndex**</span><span class="sxs-lookup"><span data-stu-id="266a7-118">**InstanceIndex**</span></span> <br/> |<span data-ttu-id="266a7-119">Den Index des Vorkommens Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="266a7-119">Identifies the index of the item occurrence.</span></span> <span data-ttu-id="266a7-120">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="266a7-120">This attribute is required.</span></span> <span data-ttu-id="266a7-121">Dieser Wert gibt eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="266a7-121">This value represents an integer.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="266a7-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="266a7-122">Child elements</span></span>

<span data-ttu-id="266a7-123">Keine.</span><span class="sxs-lookup"><span data-stu-id="266a7-123">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="266a7-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="266a7-124">Parent elements</span></span>

|<span data-ttu-id="266a7-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="266a7-125">**Element**</span></span>|<span data-ttu-id="266a7-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="266a7-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="266a7-127">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="266a7-127">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="266a7-128">Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="266a7-128">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="266a7-129">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="266a7-129">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="266a7-130">Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="266a7-130">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/><br/><span data-ttu-id="266a7-131">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="266a7-131">The following are the XPath expressions to this element:</span></span> <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/><br/><span data-ttu-id="266a7-132">**Hinweis**: [MoveItem-Vorgang](moveitem-operation.md) und einen optimalen [Betrieb CopyItem](copyitem-operation.md) nur arbeiten mit einzelnen Kalenderelemente und Terminserien Master-Shape.</span><span class="sxs-lookup"><span data-stu-id="266a7-132">**Note**:  [MoveItem operation](moveitem-operation.md) and [CopyItem operation](copyitem-operation.md) only work with single calendar items and recurring master items.</span></span> <span data-ttu-id="266a7-133">Element vorkommen sind mit diesen Verfahren ungültig.</span><span class="sxs-lookup"><span data-stu-id="266a7-133">Item occurrences are invalid with these operations.</span></span>           |
|[<span data-ttu-id="266a7-134">ItemChange</span><span class="sxs-lookup"><span data-stu-id="266a7-134">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="266a7-135">Enthält eine Element-ID und die Updates auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="266a7-135">Contains an item identifier and the updates to apply to the item.</span></span><br/><br/> <span data-ttu-id="266a7-136">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="266a7-136">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="266a7-137">Textwert</span><span class="sxs-lookup"><span data-stu-id="266a7-137">Text value</span></span>

<span data-ttu-id="266a7-138">Keine.</span><span class="sxs-lookup"><span data-stu-id="266a7-138">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="266a7-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="266a7-139">Remarks</span></span>

<span data-ttu-id="266a7-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="266a7-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="266a7-141">Beispiel</span><span class="sxs-lookup"><span data-stu-id="266a7-141">Example</span></span>

<span data-ttu-id="266a7-142">Das folgende Beispiel identifiziert das vierte Vorkommen eines sich wiederholenden-Elements, das die Identität 34vswe4 verfügt.</span><span class="sxs-lookup"><span data-stu-id="266a7-142">The following example identifies the fourth occurrence of a recurring item that has the identity 34vswe4.</span></span>
  
```XML
<OccurrenceItemId RecurringMasterId="34vswe4" InstanceIndex="4" />
```

## <a name="element-information"></a><span data-ttu-id="266a7-143">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="266a7-143">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="266a7-144">Namespace</span><span class="sxs-lookup"><span data-stu-id="266a7-144">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="266a7-145">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="266a7-145">Schema Name</span></span>  <br/> |<span data-ttu-id="266a7-146">Schematypen</span><span class="sxs-lookup"><span data-stu-id="266a7-146">Types schema</span></span>  <br/> |
|<span data-ttu-id="266a7-147">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="266a7-147">Validation File</span></span>  <br/> |<span data-ttu-id="266a7-148">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="266a7-148">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="266a7-149">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="266a7-149">Can be Empty</span></span>  <br/> |<span data-ttu-id="266a7-150">False</span><span class="sxs-lookup"><span data-stu-id="266a7-150">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="266a7-151">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="266a7-151">See also</span></span>

- [<span data-ttu-id="266a7-152">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="266a7-152">RecurringMasterItemId</span></span>](recurringmasteritemid.md)
- [<span data-ttu-id="266a7-153">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="266a7-153">FindConversation operation</span></span>](findconversation-operation.md)
- [<span data-ttu-id="266a7-154">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="266a7-154">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

