---
title: Updates (Element)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Updates
api_type:
- schema
ms.assetid: 5c1a855e-390d-4713-9d10-6e86ca392814
description: Updates-Element enthält eine Reihe von Elementen, die definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.
ms.openlocfilehash: 13df458c783b942e1c868853c41b6247119cf123
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839402"
---
# <a name="updates-item"></a><span data-ttu-id="e87bb-103">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="e87bb-103">Updates (Item)</span></span>

<span data-ttu-id="e87bb-104">**Updates** -Element enthält eine Reihe von Elementen, die definieren anfügen, festlegen und Löschen von Änderungen an Elementeigenschaften.</span><span class="sxs-lookup"><span data-stu-id="e87bb-104">The **Updates** element contains a set of elements that define append, set, and delete changes to item properties.</span></span> 
  
- [<span data-ttu-id="e87bb-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="e87bb-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="e87bb-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="e87bb-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="e87bb-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="e87bb-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="e87bb-108">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="e87bb-108">Updates (Item)</span></span>](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

<span data-ttu-id="e87bb-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="e87bb-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="e87bb-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e87bb-110">Attributes and elements</span></span>

<span data-ttu-id="e87bb-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e87bb-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e87bb-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e87bb-112">Attributes</span></span>

<span data-ttu-id="e87bb-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="e87bb-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e87bb-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e87bb-114">Child elements</span></span>

|<span data-ttu-id="e87bb-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="e87bb-115">**Element**</span></span>|<span data-ttu-id="e87bb-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e87bb-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e87bb-117">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="e87bb-117">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="e87bb-118">Stellt Daten anfügen an eine einzelne Eigenschaft eines Elements während einer [UpdateItem Vorgang](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="e87bb-118">Represents data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="e87bb-119">SetItemField</span><span class="sxs-lookup"><span data-stu-id="e87bb-119">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="e87bb-120">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="e87bb-120">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="e87bb-121">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="e87bb-121">DeleteItemField</span></span>](deleteitemfield.md) <br/> |<span data-ttu-id="e87bb-122">Stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während einer [UpdateItem Vorgang](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="e87bb-122">Represents an operation to delete a given property from an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e87bb-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e87bb-123">Parent elements</span></span>

|<span data-ttu-id="e87bb-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="e87bb-124">**Element**</span></span>|<span data-ttu-id="e87bb-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e87bb-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e87bb-126">ItemChange</span><span class="sxs-lookup"><span data-stu-id="e87bb-126">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="e87bb-127">Enthält eine Element-ID und die Updates auf das Element anwenden.</span><span class="sxs-lookup"><span data-stu-id="e87bb-127">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> <span data-ttu-id="e87bb-128">Es folgt der XPath-Ausdruck, der dieses Element:`/UpdateItem/ItemChanges/ItemChange[i]`</span><span class="sxs-lookup"><span data-stu-id="e87bb-128">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e87bb-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e87bb-129">Remarks</span></span>

<span data-ttu-id="e87bb-130">Die Updates, die von diesem Element definiert sind werden für das Element ausgeführt, die durch die Elemente [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md)oder [RecurringMasterItemId](recurringmasteritemid.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="e87bb-130">The updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements.</span></span> 
  
<span data-ttu-id="e87bb-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e87bb-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e87bb-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e87bb-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e87bb-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="e87bb-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e87bb-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e87bb-134">Schema Name</span></span>  <br/> |<span data-ttu-id="e87bb-135">Typen-schema</span><span class="sxs-lookup"><span data-stu-id="e87bb-135">types schema</span></span>  <br/> |
|<span data-ttu-id="e87bb-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e87bb-136">Validation File</span></span>  <br/> |<span data-ttu-id="e87bb-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e87bb-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e87bb-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e87bb-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="e87bb-139">False</span><span class="sxs-lookup"><span data-stu-id="e87bb-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e87bb-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e87bb-140">See also</span></span>

- [<span data-ttu-id="e87bb-141">UpdateItem Operation</span><span class="sxs-lookup"><span data-stu-id="e87bb-141">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="e87bb-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e87bb-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

