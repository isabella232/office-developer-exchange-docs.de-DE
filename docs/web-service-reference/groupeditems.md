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
description: Das GroupedItems-Element stellt eine Auflistung von Elementen dar, die das Ergebnis eines zusammengefassten FindItem-Vorgangsaufrufs sind.
ms.openlocfilehash: 0ee1ca3c6d0cf98e2daefa60a1cb1fd096cda478
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530811"
---
# <a name="groupeditems"></a><span data-ttu-id="411f1-103">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="411f1-103">GroupedItems</span></span>

<span data-ttu-id="411f1-104">Das **GroupedItems** -Element stellt eine Auflistung von Elementen dar, die das Ergebnis eines zusammengefassten [FindItem-Vorgangs](finditem-operation.md) Aufrufs sind.</span><span class="sxs-lookup"><span data-stu-id="411f1-104">The **GroupedItems** element represents a collection of items that are the result of a grouped [FindItem operation](finditem-operation.md) call.</span></span> 
  
[<span data-ttu-id="411f1-105">FindItemResponse</span><span class="sxs-lookup"><span data-stu-id="411f1-105">FindItemResponse</span></span>](finditemresponse.md)
  
[<span data-ttu-id="411f1-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="411f1-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="411f1-107">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="411f1-107">FindItemResponseMessage</span></span>](finditemresponsemessage.md)
  
[<span data-ttu-id="411f1-108">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="411f1-108">RootFolder (FindItemResponseMessage)</span></span>](rootfolder-finditemresponsemessage.md)
  
[<span data-ttu-id="411f1-109">Groups</span><span class="sxs-lookup"><span data-stu-id="411f1-109">Groups</span></span>](groups.md)
  
[<span data-ttu-id="411f1-110">GroupedItems</span><span class="sxs-lookup"><span data-stu-id="411f1-110">GroupedItems</span></span>](groupeditems.md)
  
```xml
<GroupedItems>
   <GroupIndex/>
   <Items/>
</GroupedItems>
```

 <span data-ttu-id="411f1-111">**GroupedItemsType**</span><span class="sxs-lookup"><span data-stu-id="411f1-111">**GroupedItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="411f1-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="411f1-112">Attributes and elements</span></span>

<span data-ttu-id="411f1-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="411f1-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="411f1-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="411f1-114">Attributes</span></span>

<span data-ttu-id="411f1-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="411f1-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="411f1-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="411f1-116">Child elements</span></span>

|<span data-ttu-id="411f1-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="411f1-117">**Element**</span></span>|<span data-ttu-id="411f1-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="411f1-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="411f1-119">GroupIndex</span><span class="sxs-lookup"><span data-stu-id="411f1-119">GroupIndex</span></span>](groupindex.md) <br/> |<span data-ttu-id="411f1-120">Stellt den Eigenschaftswert dar, der zum Gruppieren von Elementen in einem gruppierten [FindItem-Vorgangs](finditem-operation.md) Aufruf verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="411f1-120">Represents the property value that is used to group items in a grouped [FindItem operation](finditem-operation.md) call.</span></span>  <br/> |
|[<span data-ttu-id="411f1-121">Elemente</span><span class="sxs-lookup"><span data-stu-id="411f1-121">Items</span></span>](items.md) <br/> |<span data-ttu-id="411f1-122">Enthält ein Array von gruppierten Elementen.</span><span class="sxs-lookup"><span data-stu-id="411f1-122">Contains an array of grouped items.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="411f1-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="411f1-123">Parent elements</span></span>

|<span data-ttu-id="411f1-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="411f1-124">**Element**</span></span>|<span data-ttu-id="411f1-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="411f1-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="411f1-126">Groups</span><span class="sxs-lookup"><span data-stu-id="411f1-126">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="411f1-127">Enthält eine Auflistung von Gruppen, die mit den Such-und Aggregations Kriterien gefunden werden, die in der [FindItem-Vorgangs](finditem-operation.md) Anforderung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="411f1-127">Contains a collection of groups that are found with the search and aggregation criteria that is identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="411f1-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="411f1-128">Remarks</span></span>

<span data-ttu-id="411f1-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="411f1-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="411f1-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="411f1-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="411f1-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="411f1-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="411f1-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="411f1-132">Schema name</span></span>  <br/> |<span data-ttu-id="411f1-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="411f1-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="411f1-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="411f1-134">Validation file</span></span>  <br/> |<span data-ttu-id="411f1-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="411f1-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="411f1-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="411f1-136">Can be empty</span></span>  <br/> |<span data-ttu-id="411f1-137">False</span><span class="sxs-lookup"><span data-stu-id="411f1-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="411f1-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="411f1-138">See also</span></span>



[<span data-ttu-id="411f1-139">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="411f1-139">FindItem operation</span></span>](finditem-operation.md)


[<span data-ttu-id="411f1-140">Suchen von Elementen</span><span class="sxs-lookup"><span data-stu-id="411f1-140">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

