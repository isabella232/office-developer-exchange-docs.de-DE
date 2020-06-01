---
title: Resolutionset
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
description: Das resolutionset-Element enthält ein Array von Auflösungen für einen eindeutigen Namen.
ms.openlocfilehash: 483a096a7fcedbabe25758ebcaa31c83405a0ad4
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467172"
---
# <a name="resolutionset"></a><span data-ttu-id="a0dd2-103">Resolutionset</span><span class="sxs-lookup"><span data-stu-id="a0dd2-103">ResolutionSet</span></span>

<span data-ttu-id="a0dd2-104">Das **resolutionset** -Element enthält ein Array von Auflösungen für einen eindeutigen Namen.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-104">The **ResolutionSet** element contains an array of resolutions for an ambiguous name.</span></span> 
  
[<span data-ttu-id="a0dd2-105">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="a0dd2-105">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="a0dd2-106">ResponseMessages</span><span class="sxs-lookup"><span data-stu-id="a0dd2-106">ResponseMessages</span></span>](responsemessages.md)
  
[<span data-ttu-id="a0dd2-107">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a0dd2-107">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md)
  
[<span data-ttu-id="a0dd2-108">Resolutionset</span><span class="sxs-lookup"><span data-stu-id="a0dd2-108">ResolutionSet</span></span>](resolutionset.md)
  
```xml
<ResolutionSet IndexedPagingOffset="" NumeratorOffset="" AbsoluteDenominator="" IncludesLastItemInRange="" TotalItemsInView="">
   <Resolution/>
</ResolutionSet>
```

 <span data-ttu-id="a0dd2-109">**ArrayOfResolutionType**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-109">**ArrayOfResolutionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a0dd2-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a0dd2-110">Attributes and elements</span></span>

<span data-ttu-id="a0dd2-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a0dd2-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a0dd2-112">Attributes</span></span>

|<span data-ttu-id="a0dd2-113">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-113">**Attribute**</span></span>|<span data-ttu-id="a0dd2-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-114">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a0dd2-115">**IndexedPagingOffset**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-115">**IndexedPagingOffset**</span></span> <br/> |<span data-ttu-id="a0dd2-116">Stellt den nächsten Index dar, der für die nächste Anforderung verwendet werden soll, wenn Sie eine indizierte Seitenansicht verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-116">Represents the next index that should be used for the next request when you are using an indexed page view.</span></span>  <br/> |
|<span data-ttu-id="a0dd2-117">**NumeratorOffset**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-117">**NumeratorOffset**</span></span> <br/> |<span data-ttu-id="a0dd2-118">Stellt den neuen Zählerwert dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Ansichten mit Bruch Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-118">Represents the new numerator value to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="a0dd2-119">**AbsoluteDenominator**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-119">**AbsoluteDenominator**</span></span> <br/> |<span data-ttu-id="a0dd2-120">Stellt den nächsten Nenner dar, der für die nächste Anforderung verwendet werden soll, wenn Sie Ansichten mit Bruch Seiten verwenden.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-120">Represents the next denominator to use for the next request when you are using fraction page views.</span></span>  <br/> |
|<span data-ttu-id="a0dd2-121">**IncludesLastItemInRange**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-121">**IncludesLastItemInRange**</span></span> <br/> |<span data-ttu-id="a0dd2-122">Dieses Attribut ist true, wenn die aktuellen Ergebnisse das letzte Element in der Abfrage enthalten, sodass kein zusätzliches Paging erforderlich ist.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-122">This attribute will be true if the current results contain the last item in the query, so that additional paging is not needed.</span></span>  <br/> |
|<span data-ttu-id="a0dd2-123">**TotalItemsInView**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-123">**TotalItemsInView**</span></span> <br/> |<span data-ttu-id="a0dd2-124">Stellt die Gesamtzahl der Elemente in der Ansicht dar.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-124">Represents the total number of items in the view.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="a0dd2-125">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0dd2-125">Child elements</span></span>

|<span data-ttu-id="a0dd2-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-126">**Element**</span></span>|<span data-ttu-id="a0dd2-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0dd2-128">Lösung</span><span class="sxs-lookup"><span data-stu-id="a0dd2-128">Resolution</span></span>](resolution.md) <br/> |<span data-ttu-id="a0dd2-129">Enthält eine einzelne aufgelöste Entität.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-129">Contains a single resolved entity.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a0dd2-130">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a0dd2-130">Parent elements</span></span>

|<span data-ttu-id="a0dd2-131">**Element**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-131">**Element**</span></span>|<span data-ttu-id="a0dd2-132">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a0dd2-132">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a0dd2-133">ResolveNamesResponseMessage</span><span class="sxs-lookup"><span data-stu-id="a0dd2-133">ResolveNamesResponseMessage</span></span>](resolvenamesresponsemessage.md) <br/> |<span data-ttu-id="a0dd2-134">Enthält den Status und das Ergebnis einer ResolveNames-Anforderung.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-134">Contains the status and result of a ResolveNames request.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a0dd2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a0dd2-135">Remarks</span></span>

<span data-ttu-id="a0dd2-136">Ein **resolutionset** -Element kann maximal 100 aufgelöste Entitäten enthalten.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-136">A **ResolutionSet** element can contain a maximum of 100 resolved entities.</span></span> 
  
<span data-ttu-id="a0dd2-137">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a0dd2-137">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a0dd2-138">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a0dd2-138">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a0dd2-139">Namespace</span><span class="sxs-lookup"><span data-stu-id="a0dd2-139">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/messages  <br/> |
|<span data-ttu-id="a0dd2-140">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a0dd2-140">Schema Name</span></span>  <br/> |<span data-ttu-id="a0dd2-141">Nachrichtenschema</span><span class="sxs-lookup"><span data-stu-id="a0dd2-141">Messages schema</span></span>  <br/> |
|<span data-ttu-id="a0dd2-142">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a0dd2-142">Validation File</span></span>  <br/> |<span data-ttu-id="a0dd2-143">Messages. xsd</span><span class="sxs-lookup"><span data-stu-id="a0dd2-143">Messages.xsd</span></span>  <br/> |
|<span data-ttu-id="a0dd2-144">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a0dd2-144">Can be Empty</span></span>  <br/> |<span data-ttu-id="a0dd2-145">False</span><span class="sxs-lookup"><span data-stu-id="a0dd2-145">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a0dd2-146">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a0dd2-146">See also</span></span>



[<span data-ttu-id="a0dd2-147">ResolveNames</span><span class="sxs-lookup"><span data-stu-id="a0dd2-147">ResolveNames</span></span>](resolvenames.md)
  
[<span data-ttu-id="a0dd2-148">ResolveNamesResponse</span><span class="sxs-lookup"><span data-stu-id="a0dd2-148">ResolveNamesResponse</span></span>](resolvenamesresponse.md)
  
[<span data-ttu-id="a0dd2-149">ResolveNames-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a0dd2-149">ResolveNames operation</span></span>](resolvenames-operation.md)


- [<span data-ttu-id="a0dd2-150">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a0dd2-150">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

