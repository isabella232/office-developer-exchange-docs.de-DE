---
title: RootFolder (FindItemResponseMessage)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RootFolder
api_type:
- schema
ms.assetid: 187e009f-efaa-42a8-8962-329a645213ab
description: Das RootFolder-Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während eines Vorgangs FindItem.
ms.openlocfilehash: ea17369ef4efc4112a738b430c8f0dbab3886341
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831254"
---
# <a name="rootfolder-finditemresponsemessage"></a><span data-ttu-id="7b6d0-103">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="7b6d0-103">RootFolder (FindItemResponseMessage)</span></span>

<span data-ttu-id="7b6d0-104">Das **RootFolder** -Element enthält die Ergebnisse der Suche in der ein einzelner Stammordner während einer [FindItem Vorgang](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="7b6d0-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 <span data-ttu-id="7b6d0-105">**FindItemParentType**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-105">**FindItemParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="7b6d0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="7b6d0-106">Attributes and elements</span></span>

<span data-ttu-id="7b6d0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="7b6d0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="7b6d0-108">Attributes</span></span>

|<span data-ttu-id="7b6d0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-109">**Attribute**</span></span>|<span data-ttu-id="7b6d0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="7b6d0-111">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-111">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="7b6d0-112">Stellt den Index, der bei Verwendung eine indizierten Paging-Ansicht für die nächste Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="7b6d0-113">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-113">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="7b6d0-114">Steht für den neuen Zähler-Wert für die nächste Anforderung verwendet werden soll, wenn Teiler Seitenansichten verwenden.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-114">Represents the new numerator value to use for the next request when using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="7b6d0-115">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-115">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="7b6d0-116">Verwenden Sie für die nächste Anforderung bei Bruchzahlen Paging die nächste Nenner darstellt.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="7b6d0-117">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-117">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="7b6d0-118">Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, so dass weitere paging nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-118">Indicates whether the current results contain the last item in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="7b6d0-119">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-119">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="7b6d0-120">Stellt die Gesamtzahl der Elemente, die die Einschränkung übergeben.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-120">Represents the total number of items that pass the restriction.</span></span> <span data-ttu-id="7b6d0-121">In einem gruppierten [FindItem Vorgang](finditem-operation.md)gibt das **TotalItemsInView** -Attribut die Gesamtanzahl der Elemente in der Ansicht plus die Gesamtzahl der Gruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-121">In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="7b6d0-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b6d0-122">Child elements</span></span>

|<span data-ttu-id="7b6d0-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-123">**Element**</span></span>|<span data-ttu-id="7b6d0-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b6d0-125">Elemente</span><span class="sxs-lookup"><span data-stu-id="7b6d0-125">Items</span></span>](items.md) <br/> |<span data-ttu-id="7b6d0-126">Enthält ein Array von Elemente gefunden, die die Suchkriterien entsprechen, die in der Anforderung [FindItem Operation](finditem-operation.md) angegeben haben.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-126">Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="7b6d0-127">Gruppen</span><span class="sxs-lookup"><span data-stu-id="7b6d0-127">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="7b6d0-128">Enthält eine Auflistung von Gruppen gefunden, die die Suche und Aggregation Kriterien, die in der Anforderung [FindItem Vorgang](finditem-operation.md) identifiziert haben.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-128">Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="7b6d0-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="7b6d0-129">Parent elements</span></span>

|<span data-ttu-id="7b6d0-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-130">**Element**</span></span>|<span data-ttu-id="7b6d0-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="7b6d0-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="7b6d0-132">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="7b6d0-132">FindItemResponseMessage</span></span>](finditemresponsemessage.md) <br/> |<span data-ttu-id="7b6d0-133">Enthält den Status und das Ergebnis einer Anforderung [FindItem Vorgang](finditem-operation.md) .</span><span class="sxs-lookup"><span data-stu-id="7b6d0-133">Contains the status and result of a [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="7b6d0-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="7b6d0-134">Remarks</span></span>

<span data-ttu-id="7b6d0-135">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, der Exchange-Server, mit die Clientzugriffs-Serverrolle installiert ausgeführt wird.</span><span class="sxs-lookup"><span data-stu-id="7b6d0-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="7b6d0-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="7b6d0-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="7b6d0-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="7b6d0-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="7b6d0-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="7b6d0-138">Schema name</span></span>  <br/> |<span data-ttu-id="7b6d0-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="7b6d0-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="7b6d0-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="7b6d0-140">Validation file</span></span>  <br/> |<span data-ttu-id="7b6d0-141">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="7b6d0-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="7b6d0-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="7b6d0-142">Can be empty</span></span>  <br/> |<span data-ttu-id="7b6d0-143">False</span><span class="sxs-lookup"><span data-stu-id="7b6d0-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7b6d0-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="7b6d0-144">See also</span></span>



[<span data-ttu-id="7b6d0-145">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="7b6d0-145">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="7b6d0-146">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="7b6d0-146">IndexedPagingOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[<span data-ttu-id="7b6d0-147">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="7b6d0-147">NumeratorOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[<span data-ttu-id="7b6d0-148">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="7b6d0-148">AbsoluteDenominator</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[<span data-ttu-id="7b6d0-149">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="7b6d0-149">IncludesLastItemInRange</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[<span data-ttu-id="7b6d0-150">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="7b6d0-150">TotalItemsInView</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[<span data-ttu-id="7b6d0-151">Finding Items</span><span class="sxs-lookup"><span data-stu-id="7b6d0-151">Finding Items</span></span>](http://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

