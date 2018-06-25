---
title: RecurringMasterItemId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringMasterItemId
api_type:
- schema
ms.assetid: 5800b58c-f3d7-4d8f-acc0-d13e02f4e258
description: Das RecurringMasterItemId-Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen.
ms.openlocfilehash: ae59e33ece55d85435ece4c9030ccda32eb62eab
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831015"
---
# <a name="recurringmasteritemid"></a><span data-ttu-id="00750-103">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="00750-103">RecurringMasterItemId</span></span>

<span data-ttu-id="00750-104">Das **RecurringMasterItemId** -Element identifiziert ein Master-Shape Recurrence-Element durch das Identifizieren von Bezeichner eines seiner Elemente verwandte vorkommen.</span><span class="sxs-lookup"><span data-stu-id="00750-104">The **RecurringMasterItemId** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 <span data-ttu-id="00750-105">**RecurringMasterItemIdType**</span><span class="sxs-lookup"><span data-stu-id="00750-105">**RecurringMasterItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="00750-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="00750-106">Attributes and elements</span></span>

<span data-ttu-id="00750-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="00750-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="00750-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="00750-108">Attributes</span></span>

|<span data-ttu-id="00750-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="00750-109">**Attribute**</span></span>|<span data-ttu-id="00750-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00750-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00750-111">**OccurrenceId**</span><span class="sxs-lookup"><span data-stu-id="00750-111">**OccurrenceId**</span></span> <br/> |<span data-ttu-id="00750-112">Gibt ein einzelnes Vorkommen des ein wiederkehrendes master-Objekt.</span><span class="sxs-lookup"><span data-stu-id="00750-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="00750-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="00750-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="00750-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="00750-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="00750-115">Identifiziert eine bestimmte Version für ein einzelnes Auftreten eines sich wiederholenden master-Elements an.</span><span class="sxs-lookup"><span data-stu-id="00750-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="00750-116">Darüber hinaus wird wiederkehrenden master-Objekts auch identifiziert, da es und die einzelnen Vorkommen der gleichen Änderungsschlüssel enthalten.</span><span class="sxs-lookup"><span data-stu-id="00750-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="00750-117">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="00750-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="00750-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00750-118">Child elements</span></span>

<span data-ttu-id="00750-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="00750-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="00750-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="00750-120">Parent elements</span></span>

|<span data-ttu-id="00750-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="00750-121">**Element**</span></span>|<span data-ttu-id="00750-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="00750-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="00750-123">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="00750-123">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="00750-124">Enthält die Auflistung der Element-IDs für alle Unterhaltungselemente in einem Postfach an.</span><span class="sxs-lookup"><span data-stu-id="00750-124">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="00750-125">ItemChange</span><span class="sxs-lookup"><span data-stu-id="00750-125">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="00750-126">Enthält eine Element-ID und die Updates auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="00750-126">Contains an item identifier and the updates to apply to the item.</span></span> <br/> <br/> <span data-ttu-id="00750-127">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="00750-127">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="00750-128">Artikelnummern ein.</span><span class="sxs-lookup"><span data-stu-id="00750-128">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="00750-129">Enthält die eindeutigen Identitäten der Elemente, Vorkommen Elemente und Terminserien der Master-Shape, mit denen löschen, senden, abrufen, verschieben oder Kopieren von Elementen in der Exchange-Speicher.</span><span class="sxs-lookup"><span data-stu-id="00750-129">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="00750-130">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="00750-130">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="00750-131">Textwert</span><span class="sxs-lookup"><span data-stu-id="00750-131">Text value</span></span>

<span data-ttu-id="00750-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="00750-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="00750-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="00750-133">Remarks</span></span>

<span data-ttu-id="00750-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="00750-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="00750-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="00750-135">Example</span></span>

<span data-ttu-id="00750-136">Das folgende Beispiel identifiziert die wiederkehrenden master-Objekts durch das Identifizieren von eine der Vorkommen mit der ID 56lkjh6.</span><span class="sxs-lookup"><span data-stu-id="00750-136">The following example identifies the recurring master item by identifying one of its occurrences with the identifier 56lkjh6.</span></span>
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a><span data-ttu-id="00750-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="00750-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00750-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="00750-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="00750-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="00750-139">Schema Name</span></span>  <br/> |<span data-ttu-id="00750-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="00750-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="00750-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="00750-141">Validation File</span></span>  <br/> |<span data-ttu-id="00750-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="00750-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="00750-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="00750-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="00750-144">False</span><span class="sxs-lookup"><span data-stu-id="00750-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="00750-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="00750-145">See also</span></span>

- [<span data-ttu-id="00750-146">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="00750-146">OccurrenceItemId</span></span>](occurrenceitemid.md)
- [<span data-ttu-id="00750-147">FindConversation Operation</span><span class="sxs-lookup"><span data-stu-id="00750-147">FindConversation operation</span></span>](findconversation-operation.md)

