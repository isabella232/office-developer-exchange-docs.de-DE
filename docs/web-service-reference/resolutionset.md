---
title: ResolutionSet
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ResolutionSet
api_type:
- schema
ms.assetid: 43d5b876-0e87-4414-9b1d-bff1c1ec825c
description: Das ResolutionSet-Element enthält ein Array von Lösungen für ein mehrdeutiger Name.
ms.openlocfilehash: ad7bd31c85051e8c80aea25aa9e6f2914cf0ad01
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831160"
---
# <a name="resolutionset"></a><span data-ttu-id="e2204-103">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="e2204-103">ResolutionSet</span></span>

<span data-ttu-id="e2204-104">Das **ResolutionSet** -Element enthält ein Array von Lösungen für ein mehrdeutiger Name.</span><span class="sxs-lookup"><span data-stu-id="e2204-104">The **ResolutionSet** element contains an array of resolutions for an ambiguous name.</span></span> 
  
[<span data-ttu-id="e2204-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e2204-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="e2204-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="e2204-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="e2204-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e2204-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="e2204-108">ResolutionSet</span><span class="sxs-lookup"><span data-stu-id="e2204-108">ResolutionSet</span></span>](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 <span data-ttu-id="e2204-109">**ArrayOfResolutionType**</span><span class="sxs-lookup"><span data-stu-id="e2204-109">**ArrayOfResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2204-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e2204-110">Attributes and elements</span></span>

<span data-ttu-id="e2204-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2204-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2204-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2204-112">Attributes</span></span>

|<span data-ttu-id="e2204-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="e2204-113">**Attribute**</span></span>|<span data-ttu-id="e2204-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2204-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="e2204-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="e2204-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="e2204-116">Stellt den Index, der bei Verwendung einer indizierten Seitenansicht für die nächste Anforderung verwendet werden soll.</span><span class="sxs-lookup"><span data-stu-id="e2204-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="e2204-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="e2204-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="e2204-118">Den neue Zähler-Wert, für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2204-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="e2204-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="e2204-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="e2204-120">Die nächste Nenner für die nächste Anforderung verwendet wird, bei Verwendung der Seitenansichten Bruch darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2204-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="e2204-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="e2204-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="e2204-122">Dieses Attribut wird true, wenn die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten sein, sodass zusätzliche Paging nicht mehr benötigt wird.</span><span class="sxs-lookup"><span data-stu-id="e2204-122">This attribute will be true if the current results contain the last item in the query, so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="e2204-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="e2204-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="e2204-124">Die Gesamtanzahl der Elemente in der Ansicht darstellt.</span><span class="sxs-lookup"><span data-stu-id="e2204-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="e2204-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2204-125">Child elements</span></span>

|<span data-ttu-id="e2204-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2204-126">**Element**</span></span>|<span data-ttu-id="e2204-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2204-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2204-128">Lösung</span><span class="sxs-lookup"><span data-stu-id="e2204-128">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="e2204-129">Enthält eine einzelne aufgelöste Entität.</span><span class="sxs-lookup"><span data-stu-id="e2204-129">Contains a single resolved entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2204-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2204-130">Parent elements</span></span>

|<span data-ttu-id="e2204-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2204-131">**Element**</span></span>|<span data-ttu-id="e2204-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2204-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2204-133">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="e2204-133">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md) <br/> |<span data-ttu-id="e2204-134">Enthält den Status und das Ergebnis einer Anforderung ResolveNames.</span><span class="sxs-lookup"><span data-stu-id="e2204-134">Contains the status and result of a ResolveNames request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2204-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2204-135">Remarks</span></span>

<span data-ttu-id="e2204-136">Ein **ResolutionSet** -Element kann maximal 100 aufgelöst Entitäten enthalten.</span><span class="sxs-lookup"><span data-stu-id="e2204-136">A **ResolutionSet** element can contain a maximum of 100 resolved entities.</span></span> 
  
<span data-ttu-id="e2204-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e2204-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2204-138">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e2204-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2204-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2204-139">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="e2204-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e2204-140">Schema Name</span></span>  <br/> |<span data-ttu-id="e2204-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="e2204-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="e2204-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2204-142">Validation File</span></span>  <br/> |<span data-ttu-id="e2204-143">Messages.xsd</span><span class="sxs-lookup"><span data-stu-id="e2204-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="e2204-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e2204-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2204-145">False</span><span class="sxs-lookup"><span data-stu-id="e2204-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2204-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2204-146">See also</span></span>



[<span data-ttu-id="e2204-147">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="e2204-147">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="e2204-148">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="e2204-148">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="e2204-149">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e2204-149">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="e2204-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e2204-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

