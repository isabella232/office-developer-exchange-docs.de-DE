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
description: Das RootFolder-Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines FindItem-Vorgangs.
ms.openlocfilehash: 3bbab325dff26139739c50ef519b215aea620a0b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457130"
---
# <a name="rootfolder-finditemresponsemessage"></a><span data-ttu-id="78264-103">RootFolder (FindItemResponseMessage)</span><span class="sxs-lookup"><span data-stu-id="78264-103">RootFolder (FindItemResponseMessage)</span></span>

<span data-ttu-id="78264-104">Das **RootFolder** -Element enthält die Ergebnisse einer Suche eines einzelnen Stammordners während eines [FindItem-Vorgangs](finditem-operation.md).</span><span class="sxs-lookup"><span data-stu-id="78264-104">The **RootFolder** element contains the results of a search of a single root folder during a [FindItem operation](finditem-operation.md).</span></span>
  
```xml
<RootFolder IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Items/>
   <Groups/>
</RootFolder>
```

 <span data-ttu-id="78264-105">**FindItemParentType**</span><span class="sxs-lookup"><span data-stu-id="78264-105">**FindItemParentType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78264-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78264-106">Attributes and elements</span></span>

<span data-ttu-id="78264-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78264-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78264-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78264-108">Attributes</span></span>

|<span data-ttu-id="78264-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="78264-109">**Attribute**</span></span>|<span data-ttu-id="78264-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78264-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="78264-111">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="78264-111">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="78264-112">Stellt den nächsten Index dar, der bei der Verwendung einer indizierten Auslagerungs Ansicht für die nächste Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="78264-112">Represents the next index that should be used for the next request when using an indexed paging view.</span></span>  <br/> |
|<span data-ttu-id="78264-113">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="78264-113">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="78264-114">Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Bruch Seitenansichten verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="78264-114">Represents the new numerator value to use for the next request when using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="78264-115">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="78264-115">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="78264-116">Stellt den nächsten Nenner dar, der für die nächste Anforderung bei Bruchzahlen verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78264-116">Represents the next denominator to use for the next request when doing fractional paging.</span></span>  <br/> |
|<span data-ttu-id="78264-117">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="78264-117">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="78264-118">Gibt an, ob die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass kein weiteres Paging erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="78264-118">Indicates whether the current results contain the last item in the query, such that further paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="78264-119">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="78264-119">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="78264-120">Stellt die Gesamtzahl der Elemente dar, die die Einschränkung übergeben.</span><span class="sxs-lookup"><span data-stu-id="78264-120">Represents the total number of items that pass the restriction.</span></span> <span data-ttu-id="78264-121">In einem gruppierten [FindItem-Vorgang](finditem-operation.md)gibt das **TotalItemsInView** -Attribut die Gesamtanzahl der Elemente in der Ansicht sowie die Gesamtzahl der Gruppen zurück.</span><span class="sxs-lookup"><span data-stu-id="78264-121">In a grouped [FindItem operation](finditem-operation.md), the **TotalItemsInView** attribute returns the total number of items in the view plus the total number of groups.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="78264-122">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78264-122">Child elements</span></span>

|<span data-ttu-id="78264-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="78264-123">**Element**</span></span>|<span data-ttu-id="78264-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78264-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78264-125">Items</span><span class="sxs-lookup"><span data-stu-id="78264-125">Items</span></span>](items.md) <br/> |<span data-ttu-id="78264-126">Enthält ein Array mit gefundenen Elementen, die die in der FindItem- [Vorgangs](finditem-operation.md) Anforderung angegebenen Suchkriterien aufweisen.</span><span class="sxs-lookup"><span data-stu-id="78264-126">Contains an array of items found that have the search criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
|[<span data-ttu-id="78264-127">Groups</span><span class="sxs-lookup"><span data-stu-id="78264-127">Groups</span></span>](groups.md) <br/> |<span data-ttu-id="78264-128">Enthält eine Auflistung von Gruppen, die die Such-und Aggregations Kriterien aufweisen, die in der [FindItem-Vorgangs](finditem-operation.md) Anforderung angegeben sind.</span><span class="sxs-lookup"><span data-stu-id="78264-128">Contains a collection of groups found that have the search and aggregation criteria identified in the [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="78264-129">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78264-129">Parent elements</span></span>

|<span data-ttu-id="78264-130">**Element**</span><span class="sxs-lookup"><span data-stu-id="78264-130">**Element**</span></span>|<span data-ttu-id="78264-131">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78264-131">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78264-132">FindItemResponseMessage</span><span class="sxs-lookup"><span data-stu-id="78264-132">FindItemResponseMessage</span></span>](finditemresponsemessage.md) <br/> |<span data-ttu-id="78264-133">Enthält den Status und das Ergebnis einer [FindItem-Vorgangs](finditem-operation.md) Anforderung.</span><span class="sxs-lookup"><span data-stu-id="78264-133">Contains the status and result of a [FindItem operation](finditem-operation.md) request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78264-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="78264-134">Remarks</span></span>

<span data-ttu-id="78264-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server mit installierter Client Zugriffs-Server Rolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="78264-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running Exchange Server with the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78264-136">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="78264-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78264-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="78264-137">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="78264-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78264-138">Schema name</span></span>  <br/> |<span data-ttu-id="78264-139">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="78264-139">Messages schema</span></span>  <br/> |
|<span data-ttu-id="78264-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78264-140">Validation file</span></span>  <br/> |<span data-ttu-id="78264-141">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="78264-141">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="78264-142">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="78264-142">Can be empty</span></span>  <br/> |<span data-ttu-id="78264-143">False</span><span class="sxs-lookup"><span data-stu-id="78264-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78264-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78264-144">See also</span></span>



[<span data-ttu-id="78264-145">FindItem-Vorgang</span><span class="sxs-lookup"><span data-stu-id="78264-145">FindItem operation</span></span>](finditem-operation.md)
  
[<span data-ttu-id="78264-146">IndexedPagingOffset</span><span class="sxs-lookup"><span data-stu-id="78264-146">IndexedPagingOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IndexedPagingOffset.aspx)
  
[<span data-ttu-id="78264-147">NumeratorOffset</span><span class="sxs-lookup"><span data-stu-id="78264-147">NumeratorOffset</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.NumeratorOffset.aspx)
  
[<span data-ttu-id="78264-148">AbsoluteDenominator</span><span class="sxs-lookup"><span data-stu-id="78264-148">AbsoluteDenominator</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.AbsoluteDenominator.aspx)
  
[<span data-ttu-id="78264-149">IncludesLastItemInRange</span><span class="sxs-lookup"><span data-stu-id="78264-149">IncludesLastItemInRange</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.IncludesLastItemInRange.aspx)
  
[<span data-ttu-id="78264-150">TotalItemsInView</span><span class="sxs-lookup"><span data-stu-id="78264-150">TotalItemsInView</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.FindItemParentType.TotalItemsInView.aspx)


[<span data-ttu-id="78264-151">Finding Items</span><span class="sxs-lookup"><span data-stu-id="78264-151">Finding Items</span></span>](https://msdn.microsoft.com/library/63af1f9c-464b-4fca-9ae3-3d60f24ca93c%28Office.15%29.aspx)

