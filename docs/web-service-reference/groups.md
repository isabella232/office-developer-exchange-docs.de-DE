---
title: Gruppen
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Groups
api_type:
- schema
ms.assetid: 6b6b2d67-219d-4dfb-a4ed-d627b1cfb33f
description: Das Gruppen-Element enthält eine Auflistung von Gruppen, die mit den Kriterien Such- und Aggregation gefunden werden, die in der FindItem Vorgang Anforderung identifiziert wird.
ms.openlocfilehash: 406a1974899e89243f52ba7a56afcc172c4f3df6
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19829786"
---
# <a name="groups"></a><span data-ttu-id="63be2-103">Gruppen</span><span class="sxs-lookup"><span data-stu-id="63be2-103">Groups</span></span>

<span data-ttu-id="63be2-104">Das **Gruppen** -Element enthält eine Auflistung von Gruppen, die mit den Kriterien Such- und Aggregation gefunden werden, die in der Anforderung [FindItem Vorgang](finditem-operation.md) identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="63be2-104">The **Groups** element contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span> 
  
```xml
<Groups>
   <GroupedItems/>
</Groups>
```

 <span data-ttu-id="63be2-105">**ArrayOfGroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="63be2-105">**ArrayOfGroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="63be2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="63be2-106">Attributes and elements</span></span>

<span data-ttu-id="63be2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="63be2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="63be2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="63be2-108">Attributes</span></span>

<span data-ttu-id="63be2-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="63be2-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="63be2-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63be2-110">Child elements</span></span>

|<span data-ttu-id="63be2-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="63be2-111">**Element**</span></span>|<span data-ttu-id="63be2-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63be2-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63be2-113">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="63be2-113">GroupedItems</span></span>](groupeditems.md) <br/> |<span data-ttu-id="63be2-114">Stellt eine Auflistung von Elementen, die das Ergebnis einer gruppierten [FindItem Vorgang](finditem-operation.md) sind aufrufen.</span><span class="sxs-lookup"><span data-stu-id="63be2-114">Represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="63be2-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="63be2-115">Parent elements</span></span>

|<span data-ttu-id="63be2-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="63be2-116">**Element**</span></span>|<span data-ttu-id="63be2-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="63be2-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="63be2-118">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="63be2-118">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md) <br/> |<span data-ttu-id="63be2-119">Enthält die Ergebnisse einer Suche in einer einzelnen Stammordner während eines Vorgangs [FindItem Vorgang](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="63be2-119">Contains the results from a search of a single root folder during a [FindItem operation](finditem-operation.md) operation.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="63be2-120">Hinweise</span><span class="sxs-lookup"><span data-stu-id="63be2-120">Remarks</span></span>

<span data-ttu-id="63be2-121">Tritt auf, [GroupedItems](groupeditems.md) einmal für jede Gruppe unterschiedliche innerhalb der Ergebnismenge.</span><span class="sxs-lookup"><span data-stu-id="63be2-121">One [GroupedItems](groupeditems.md) instance will occur for each distinct group within the result.</span></span> 
  
<span data-ttu-id="63be2-122">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="63be2-122">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="63be2-123">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="63be2-123">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="63be2-124">Namespace</span><span class="sxs-lookup"><span data-stu-id="63be2-124">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="63be2-125">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="63be2-125">Schema name</span></span>  <br/> |<span data-ttu-id="63be2-126">Schematypen</span><span class="sxs-lookup"><span data-stu-id="63be2-126">Types schema</span></span>  <br/> |
|<span data-ttu-id="63be2-127">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="63be2-127">Validation file</span></span>  <br/> |<span data-ttu-id="63be2-128">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="63be2-128">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="63be2-129">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="63be2-129">Can be empty</span></span>  <br/> |<span data-ttu-id="63be2-130">False</span><span class="sxs-lookup"><span data-stu-id="63be2-130">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="63be2-131">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="63be2-131">See also</span></span>



[<span data-ttu-id="63be2-132">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="63be2-132">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="63be2-133">Finding Items</span><span class="sxs-lookup"><span data-stu-id="63be2-133">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

