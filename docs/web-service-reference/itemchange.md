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
description: Das ItemChange-Element enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.
ms.openlocfilehash: 916ef1ba2c7a709ec1fd80ababd72999506773c4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459917"
---
# <a name="itemchange"></a><span data-ttu-id="5bb5f-103">ItemChange</span><span class="sxs-lookup"><span data-stu-id="5bb5f-103">ItemChange</span></span>

<span data-ttu-id="5bb5f-104">Das **ItemChange** -Element enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-104">The **ItemChange** element contains an item identifier and the updates to apply to the item.</span></span> 
  
- [<span data-ttu-id="5bb5f-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="5bb5f-105">UpdateItem</span></span>](updateitem.md) 
- [<span data-ttu-id="5bb5f-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="5bb5f-106">ItemChanges</span></span>](itemchanges.md)
- [<span data-ttu-id="5bb5f-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="5bb5f-107">ItemChange</span></span>](itemchange.md)
  
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

<span data-ttu-id="5bb5f-108">**ItemChangeType**</span><span class="sxs-lookup"><span data-stu-id="5bb5f-108">**ItemChangeType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5bb5f-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5bb5f-109">Attributes and elements</span></span>

<span data-ttu-id="5bb5f-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5bb5f-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="5bb5f-111">Attributes</span></span>

<span data-ttu-id="5bb5f-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5bb5f-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5bb5f-113">Child elements</span></span>

|<span data-ttu-id="5bb5f-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="5bb5f-114">**Element**</span></span>|<span data-ttu-id="5bb5f-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bb5f-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bb5f-116">ItemId</span><span class="sxs-lookup"><span data-stu-id="5bb5f-116">ItemId</span></span>](itemid.md) <br/> |<span data-ttu-id="5bb5f-117">Enthält den eindeutigen Bezeichner und den Änderungsschlüssel eines Elements in der Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-117">Contains the unique identifier and change key of an item in the Exchange store.</span></span> <span data-ttu-id="5bb5f-118">Dieses Element ist erforderlich, wenn das [OccurrenceItemId](occurrenceitemid.md) -oder das [RecurringMasterItemId](recurringmasteritemid.md) -Element nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-118">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [RecurringMasterItemId](recurringmasteritemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="5bb5f-119">OccurrenceItemId</span><span class="sxs-lookup"><span data-stu-id="5bb5f-119">OccurrenceItemId</span></span>](occurrenceitemid.md) <br/> |<span data-ttu-id="5bb5f-120">Gibt ein einzelnes Vorkommen eines wiederkehrenden Elements an.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-120">Identifies a single occurrence of a recurring item.</span></span> <span data-ttu-id="5bb5f-121">Dieses Element ist erforderlich, wenn es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-121">This element is required if used.</span></span> <span data-ttu-id="5bb5f-122">Dieses Element ist erforderlich, wenn das [RecurringMasterItemId](recurringmasteritemid.md) -oder [ItemID](itemid.md) -Element nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-122">This element is required if the [RecurringMasterItemId](recurringmasteritemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="5bb5f-123">RecurringMasterItemId</span><span class="sxs-lookup"><span data-stu-id="5bb5f-123">RecurringMasterItemId</span></span>](recurringmasteritemid.md) <br/> |<span data-ttu-id="5bb5f-124">Identifiziert ein Serienmasterelement durch Identifizieren eines der Bezeichner des zugehörigen vorkommen Elements.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-124">Identifies a recurrence master item by identifying one of its related occurrence items' identifiers.</span></span> <span data-ttu-id="5bb5f-125">Dieses Element ist erforderlich, wenn es verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-125">This element is required if used.</span></span> <span data-ttu-id="5bb5f-126">Dieses Element ist erforderlich, wenn das [OccurrenceItemId](occurrenceitemid.md) -oder [ItemID](itemid.md) -Element nicht verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-126">This element is required if the [OccurrenceItemId](occurrenceitemid.md) or [ItemId](itemid.md) element is not used.</span></span>  <br/> |
|[<span data-ttu-id="5bb5f-127">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="5bb5f-127">Updates (Item)</span></span>](updates-item.md) <br/> |<span data-ttu-id="5bb5f-128">Enthält ein Array, das Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definiert.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-128">Contains an array that defines append, set, and delete changes to item properties.</span></span> <span data-ttu-id="5bb5f-129">Dieses Element ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-129">This element is required.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5bb5f-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5bb5f-130">Parent elements</span></span>

|<span data-ttu-id="5bb5f-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="5bb5f-131">**Element**</span></span>|<span data-ttu-id="5bb5f-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5bb5f-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5bb5f-133">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="5bb5f-133">ItemChanges</span></span>](itemchanges.md) <br/> |<span data-ttu-id="5bb5f-134">Enthält ein Array von [ItemChange](itemchange.md) -Elementen, mit denen Elemente identifiziert werden, und die Updates, die auf die Elemente angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-134">Contains an array of [ItemChange](itemchange.md) elements that identify items and the updates to apply to the items.</span></span>  <br/> <span data-ttu-id="5bb5f-135">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="5bb5f-135">The following is the XPath expression to this element:</span></span>  <br/>  `/UpdateItem/ItemChanges` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5bb5f-136">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5bb5f-136">Remarks</span></span>

<span data-ttu-id="5bb5f-137">In einem **ItemChange** -Element kann nur ein einzelnes [ItemID](itemid.md)-, [OccurrenceItemId](occurrenceitemid.md)-oder [RecurringMasterItemId](recurringmasteritemid.md) -Element verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-137">Only a single [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) element can be used in an **ItemChange** element.</span></span> 
  
<span data-ttu-id="5bb5f-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5bb5f-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5bb5f-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5bb5f-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5bb5f-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5bb5f-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5bb5f-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5bb5f-141">Schema Name</span></span>  <br/> |<span data-ttu-id="5bb5f-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5bb5f-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="5bb5f-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5bb5f-143">Validation File</span></span>  <br/> |<span data-ttu-id="5bb5f-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5bb5f-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5bb5f-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5bb5f-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="5bb5f-146">False</span><span class="sxs-lookup"><span data-stu-id="5bb5f-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5bb5f-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5bb5f-147">See also</span></span>

- [<span data-ttu-id="5bb5f-148">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5bb5f-148">UpdateItem operation</span></span>](updateitem-operation.md)

