---
title: GroupedItems
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupedItems
api_type:
- schema
ms.assetid: 53170df4-4272-4b37-b23f-cd8e2d4a7396
description: Das Element GroupedItems stellt eine Auflistung von Elementen, die das Ergebnis eines gruppierten FindItem Vorgang Anrufs sind.
ms.openlocfilehash: f8aed9b78fc54307f44b96a45e5c31a4cc76ab50
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829756"
---
# <a name="groupeditems"></a><span data-ttu-id="5fe55-103">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="5fe55-103">GroupedItems</span></span>

<span data-ttu-id="5fe55-104">Das **GroupedItems** -Element stellt eine Auflistung von Elementen, die das Ergebnis einer gruppierten [FindItem Vorgang](finditem-operation.md) sind aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5fe55-104">The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="5fe55-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="5fe55-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="5fe55-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="5fe55-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="5fe55-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="5fe55-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="5fe55-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="5fe55-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="5fe55-109">Gruppen</span><span class="sxs-lookup"><span data-stu-id="5fe55-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="5fe55-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="5fe55-110">GroupedItems</span></span>](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 <span data-ttu-id="5fe55-111">**GroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="5fe55-111">**GroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5fe55-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5fe55-112">Attributes and elements</span></span>

<span data-ttu-id="5fe55-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5fe55-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5fe55-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="5fe55-114">Attributes</span></span>

<span data-ttu-id="5fe55-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="5fe55-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5fe55-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fe55-116">Child elements</span></span>

|<span data-ttu-id="5fe55-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fe55-117">**Element**</span></span>|<span data-ttu-id="5fe55-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fe55-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fe55-119">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="5fe55-119">GroupIndex</span></span>](groupindex.md) <br/> |<span data-ttu-id="5fe55-120">Stellt den Wert der Eigenschaft, die verwendet wird zum Gruppieren von Elementen in einem gruppierten [FindItem Vorgang](finditem-operation.md) aufrufen.</span><span class="sxs-lookup"><span data-stu-id="5fe55-120">Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="5fe55-121">Elemente</span><span class="sxs-lookup"><span data-stu-id="5fe55-121">Items</span></span>](items.md) <br/> |<span data-ttu-id="5fe55-122">Ein Array von gruppierten Elemente enthält.</span><span class="sxs-lookup"><span data-stu-id="5fe55-122">Contains an array of grouped items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5fe55-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5fe55-123">Parent elements</span></span>

|<span data-ttu-id="5fe55-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="5fe55-124">**Element**</span></span>|<span data-ttu-id="5fe55-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5fe55-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5fe55-126">Gruppen</span><span class="sxs-lookup"><span data-stu-id="5fe55-126">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="5fe55-127">Enthält eine Auflistung von Gruppen, die mit den Kriterien Such- und Aggregation gefunden werden, die in der Anforderung [FindItem Vorgang](finditem-operation.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="5fe55-127">Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5fe55-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5fe55-128">Remarks</span></span>

<span data-ttu-id="5fe55-129">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5fe55-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5fe55-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5fe55-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5fe55-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="5fe55-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5fe55-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5fe55-132">Schema name</span></span>  <br/> |<span data-ttu-id="5fe55-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5fe55-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="5fe55-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5fe55-134">Validation file</span></span>  <br/> |<span data-ttu-id="5fe55-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5fe55-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5fe55-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="5fe55-136">Can be empty</span></span>  <br/> |<span data-ttu-id="5fe55-137">False</span><span class="sxs-lookup"><span data-stu-id="5fe55-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5fe55-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5fe55-138">See also</span></span>



[<span data-ttu-id="5fe55-139">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5fe55-139">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="5fe55-140">Finding Items</span><span class="sxs-lookup"><span data-stu-id="5fe55-140">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

