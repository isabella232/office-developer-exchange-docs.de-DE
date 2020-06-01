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
description: Das Updates-Element enthält eine Reihe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definieren.
ms.openlocfilehash: 6902ea4d3d3d9adc074745d5642cdfa6d91a9163
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456353"
---
# <a name="updates-item"></a><span data-ttu-id="17cc5-103">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="17cc5-103">Updates (Item)</span></span>

<span data-ttu-id="17cc5-104">Das **Updates** -Element enthält eine Reihe von Elementen, die Append-, festlegen-und DELETE-Änderungen an Elementeigenschaften definieren.</span><span class="sxs-lookup"><span data-stu-id="17cc5-104">The **Updates** element contains a set of elements that define append, set, and delete changes to item properties.</span></span> 
  
- [<span data-ttu-id="17cc5-105">UpdateItem</span><span class="sxs-lookup"><span data-stu-id="17cc5-105">UpdateItem</span></span>](updateitem.md)
  
- [<span data-ttu-id="17cc5-106">ItemChanges</span><span class="sxs-lookup"><span data-stu-id="17cc5-106">ItemChanges</span></span>](itemchanges.md)
  
- [<span data-ttu-id="17cc5-107">ItemChange</span><span class="sxs-lookup"><span data-stu-id="17cc5-107">ItemChange</span></span>](itemchange.md)
  
- [<span data-ttu-id="17cc5-108">Updates (Element)</span><span class="sxs-lookup"><span data-stu-id="17cc5-108">Updates (Item)</span></span>](updates-item.md)
  
```xml
<Updates>
   <AppendToItemField/>
   <SetItemField/>
   <DeleteItemField/>
</Updates>
```

<span data-ttu-id="17cc5-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span><span class="sxs-lookup"><span data-stu-id="17cc5-109">**NonEmptyArrayOfItemChangeDescriptionsType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="17cc5-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="17cc5-110">Attributes and elements</span></span>

<span data-ttu-id="17cc5-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="17cc5-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17cc5-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="17cc5-112">Attributes</span></span>

<span data-ttu-id="17cc5-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="17cc5-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17cc5-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17cc5-114">Child elements</span></span>

|<span data-ttu-id="17cc5-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="17cc5-115">**Element**</span></span>|<span data-ttu-id="17cc5-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17cc5-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17cc5-117">AppendToItemField</span><span class="sxs-lookup"><span data-stu-id="17cc5-117">AppendToItemField</span></span>](appendtoitemfield.md) <br/> |<span data-ttu-id="17cc5-118">Stellt Daten dar, die während eines [UpdateItem-Vorgangs](updateitem-operation.md)an eine einzelne Eigenschaft eines Elements angefügt werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17cc5-118">Represents data to append to a single property of an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="17cc5-119">SetItemField</span><span class="sxs-lookup"><span data-stu-id="17cc5-119">SetItemField</span></span>](setitemfield.md) <br/> |<span data-ttu-id="17cc5-120">Stellt eine Aktualisierung auf eine einzelne Eigenschaft eines Elements in einer [UpdateItem Operation](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="17cc5-120">Represents an update to a single property of an item in an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
|[<span data-ttu-id="17cc5-121">DeleteItemField</span><span class="sxs-lookup"><span data-stu-id="17cc5-121">DeleteItemField</span></span>](deleteitemfield.md) <br/> |<span data-ttu-id="17cc5-122">Stellt einen Vorgang zum Löschen einer bestimmten Eigenschaft aus einem Element während eines [UpdateItem-Vorgangs](updateitem-operation.md)dar.</span><span class="sxs-lookup"><span data-stu-id="17cc5-122">Represents an operation to delete a given property from an item during an [UpdateItem operation](updateitem-operation.md).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17cc5-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17cc5-123">Parent elements</span></span>

|<span data-ttu-id="17cc5-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="17cc5-124">**Element**</span></span>|<span data-ttu-id="17cc5-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17cc5-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17cc5-126">ItemChange</span><span class="sxs-lookup"><span data-stu-id="17cc5-126">ItemChange</span></span>](itemchange.md) <br/> |<span data-ttu-id="17cc5-127">Enthält eine Element-ID und die Updates, die auf das Element angewendet werden sollen.</span><span class="sxs-lookup"><span data-stu-id="17cc5-127">Contains an item identifier and the updates to apply to the item.</span></span>  <br/> <span data-ttu-id="17cc5-128">Im folgenden finden Sie den XPath-Ausdruck für dieses Element:`/UpdateItem/ItemChanges/ItemChange[i]`</span><span class="sxs-lookup"><span data-stu-id="17cc5-128">The following is the XPath expression to this element:  `/UpdateItem/ItemChanges/ItemChange[i]`</span></span> <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17cc5-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17cc5-129">Remarks</span></span>

<span data-ttu-id="17cc5-130">Die durch dieses Element definierten Updates werden für das Element ausgeführt, das durch die Elemente [ItemID](itemid.md), [OccurrenceItemId](occurrenceitemid.md)oder [RecurringMasterItemId](recurringmasteritemid.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="17cc5-130">The updates that are defined by this element are performed on the item that is identified by the [ItemId](itemid.md), [OccurrenceItemId](occurrenceitemid.md), or [RecurringMasterItemId](recurringmasteritemid.md) elements.</span></span> 
  
<span data-ttu-id="17cc5-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="17cc5-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17cc5-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="17cc5-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17cc5-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="17cc5-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17cc5-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="17cc5-134">Schema Name</span></span>  <br/> |<span data-ttu-id="17cc5-135">Typenschema</span><span class="sxs-lookup"><span data-stu-id="17cc5-135">types schema</span></span>  <br/> |
|<span data-ttu-id="17cc5-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="17cc5-136">Validation File</span></span>  <br/> |<span data-ttu-id="17cc5-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="17cc5-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="17cc5-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="17cc5-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="17cc5-139">False</span><span class="sxs-lookup"><span data-stu-id="17cc5-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17cc5-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17cc5-140">See also</span></span>

- [<span data-ttu-id="17cc5-141">UpdateItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="17cc5-141">UpdateItem operation</span></span>](updateitem-operation.md)
- [<span data-ttu-id="17cc5-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="17cc5-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

