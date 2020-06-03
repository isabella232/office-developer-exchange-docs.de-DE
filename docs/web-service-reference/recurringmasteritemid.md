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
description: Das RecurringMasterItemId-Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines der zugehörigen vorkommen Elemente.
ms.openlocfilehash: 896a9ce95d619e7bb44c8158288bc4f62ce417d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529882"
---
# <a name="recurringmasteritemid"></a><span data-ttu-id="73b8d-103">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="73b8d-103">RecurringMasterItemId</span></span>

<span data-ttu-id="73b8d-104">Das **RecurringMasterItemId** -Element identifiziert ein Serienmasterelement durch Identifizieren der Bezeichner eines der zugehörigen vorkommen Elemente.</span><span class="sxs-lookup"><span data-stu-id="73b8d-104">The **RecurringMasterItemId** element identifies a recurrence master item by identifying the identifiers of one of its related occurrence items.</span></span> 
  
```XML
<RecurringMasterItemId OccurrenceId="" ChangeKey="" />
```

 <span data-ttu-id="73b8d-105">**RecurringMasterItemIdType**</span><span class="sxs-lookup"><span data-stu-id="73b8d-105">**RecurringMasterItemIdType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="73b8d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="73b8d-106">Attributes and elements</span></span>

<span data-ttu-id="73b8d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="73b8d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="73b8d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="73b8d-108">Attributes</span></span>

|<span data-ttu-id="73b8d-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="73b8d-109">**Attribute**</span></span>|<span data-ttu-id="73b8d-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73b8d-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="73b8d-111">**OccurrenceId**</span><span class="sxs-lookup"><span data-stu-id="73b8d-111">**OccurrenceId**</span></span> <br/> |<span data-ttu-id="73b8d-112">Gibt ein einzelnes Vorkommen eines wiederkehrenden Hauptelements an.</span><span class="sxs-lookup"><span data-stu-id="73b8d-112">Identifies a single occurrence of a recurring master item.</span></span> <span data-ttu-id="73b8d-113">Dieses Attribut ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="73b8d-113">This attribute is required.</span></span>  <br/> |
|<span data-ttu-id="73b8d-114">**ChangeKey**</span><span class="sxs-lookup"><span data-stu-id="73b8d-114">**ChangeKey**</span></span> <br/> |<span data-ttu-id="73b8d-115">Gibt eine bestimmte Version eines einzelnen Auftretens eines wiederkehrenden Hauptelements an.</span><span class="sxs-lookup"><span data-stu-id="73b8d-115">Identifies a specific version of a single occurrence of a recurring master item.</span></span> <span data-ttu-id="73b8d-116">Darüber hinaus wird das wiederkehrende Hauptelement ebenfalls identifiziert, da es und das einzelne Vorkommen denselben Änderungsschlüssel enthalten werden.</span><span class="sxs-lookup"><span data-stu-id="73b8d-116">Additionally, the recurring master item is also identified because it and the single occurrence will contain the same change key.</span></span> <span data-ttu-id="73b8d-117">Dieses Attribut ist optional.</span><span class="sxs-lookup"><span data-stu-id="73b8d-117">This attribute is optional.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="73b8d-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73b8d-118">Child elements</span></span>

<span data-ttu-id="73b8d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="73b8d-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="73b8d-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="73b8d-120">Parent elements</span></span>

|<span data-ttu-id="73b8d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="73b8d-121">**Element**</span></span>|<span data-ttu-id="73b8d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="73b8d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="73b8d-123">GlobalItemIds</span><span class="sxs-lookup"><span data-stu-id="73b8d-123">GlobalItemIds</span></span>](globalitemids.md) <br/> |<span data-ttu-id="73b8d-124">Enthält die Auflistung von Element-IDs für alle Unterhaltungselemente in einem Postfach.</span><span class="sxs-lookup"><span data-stu-id="73b8d-124">Contains the collection of item identifiers for all conversation items in a mailbox.</span></span>  <br/> |
|[<span data-ttu-id="73b8d-125">ItemChange</span><span class="sxs-lookup"><span data-stu-id="73b8d-125">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="73b8d-126">Enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="73b8d-126">Contains an item identifier and the updates to apply to the item.</span></span> <br/> <br/> <span data-ttu-id="73b8d-127">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="73b8d-127">The following is the XPath expression to this element:</span></span> <br/> <br/>  `/UpdateItem/ItemChanges/ItemChange[i]` <br/> |
|[<span data-ttu-id="73b8d-128">ItemIds</span><span class="sxs-lookup"><span data-stu-id="73b8d-128">ItemIds</span></span>](itemids.md) <br/> | <span data-ttu-id="73b8d-129">Enthält die eindeutigen Identitäten von Elementen, Element Elementen und wiederkehrenden Hauptelementen, die zum Löschen, senden, abrufen, verlagern oder Kopieren von Elementen in der Exchange-Informationsspeicher verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="73b8d-129">Contains the unique identities of items, occurrence items, and recurring master items that are used to delete, send, get, move, or copy items in the Exchange store.</span></span> <br/> <br/>  <span data-ttu-id="73b8d-130">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="73b8d-130">The following are the XPath expressions to this element:</span></span>  <br/><br/>  `/DeleteItem/ItemIds` <br/>  `/SendItem/ItemIds` <br/>  `/GetItem/ItemIds` <br/>  `/MoveItem/ItemIds` <br/>  `/CopyItem//ItemIds` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="73b8d-131">Textwert</span><span class="sxs-lookup"><span data-stu-id="73b8d-131">Text value</span></span>

<span data-ttu-id="73b8d-132">Keine.</span><span class="sxs-lookup"><span data-stu-id="73b8d-132">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="73b8d-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="73b8d-133">Remarks</span></span>

<span data-ttu-id="73b8d-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="73b8d-134">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="example"></a><span data-ttu-id="73b8d-135">Beispiel</span><span class="sxs-lookup"><span data-stu-id="73b8d-135">Example</span></span>

<span data-ttu-id="73b8d-136">Im folgenden Beispiel wird das wiederkehrende masterelement identifiziert, indem eines seiner vorkommen mit dem Bezeichner 56lkjh6 identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="73b8d-136">The following example identifies the recurring master item by identifying one of its occurrences with the identifier 56lkjh6.</span></span>
  
```XML
<RecurringMasterItemId OccurrenceId="56lkjh6" />
```

## <a name="element-information"></a><span data-ttu-id="73b8d-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="73b8d-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="73b8d-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="73b8d-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="73b8d-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="73b8d-139">Schema Name</span></span>  <br/> |<span data-ttu-id="73b8d-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="73b8d-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="73b8d-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="73b8d-141">Validation File</span></span>  <br/> |<span data-ttu-id="73b8d-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="73b8d-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="73b8d-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="73b8d-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="73b8d-144">False</span><span class="sxs-lookup"><span data-stu-id="73b8d-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="73b8d-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="73b8d-145">See also</span></span>

- [<span data-ttu-id="73b8d-146">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="73b8d-146">OccurrenceItemId</span></span>](occurrenceitemid.md)
- [<span data-ttu-id="73b8d-147">FindConversation-Vorgang</span><span class="sxs-lookup"><span data-stu-id="73b8d-147">FindConversation operation</span></span>](findconversation-operation.md)

