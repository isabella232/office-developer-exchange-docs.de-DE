---
title: MinimumSuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MinimumSuggestionQuality
api_type:
- schema
ms.assetid: 3725cbd4-9bc1-4f7d-8929-b2c68cb46114
description: Das MinimumSuggestionQuality-Element definiert die Qualität von Besprechungs Vorschlägen, die in der Antwort zurückgegeben werden sollen.
ms.openlocfilehash: c85cbf65a63ac0b09408c14e01889f97a05b27b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44467480"
---
# <a name="minimumsuggestionquality"></a><span data-ttu-id="09396-103">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="09396-103">MinimumSuggestionQuality</span></span>

<span data-ttu-id="09396-104">Das **MinimumSuggestionQuality** -Element definiert die Qualität von Besprechungs Vorschlägen, die in der Antwort zurückgegeben werden sollen.</span><span class="sxs-lookup"><span data-stu-id="09396-104">The **MinimumSuggestionQuality** element defines the quality of meeting suggestions to be returned in the response.</span></span> 
  
[<span data-ttu-id="09396-105">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="09396-105">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md)
  
[<span data-ttu-id="09396-106">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="09396-106">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md)
  
[<span data-ttu-id="09396-107">MinimumSuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="09396-107">MinimumSuggestionQuality</span></span>](minimumsuggestionquality.md)
  
```xml
<MinimumSuggestionQuality>...</MinimumSuggestionQuality>
```

 <span data-ttu-id="09396-108">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="09396-108">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="09396-109">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="09396-109">Attributes and elements</span></span>

<span data-ttu-id="09396-110">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="09396-110">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="09396-111">Attribute</span><span class="sxs-lookup"><span data-stu-id="09396-111">Attributes</span></span>

<span data-ttu-id="09396-112">Keine.</span><span class="sxs-lookup"><span data-stu-id="09396-112">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="09396-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09396-113">Child elements</span></span>

<span data-ttu-id="09396-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="09396-114">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="09396-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="09396-115">Parent elements</span></span>

|<span data-ttu-id="09396-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="09396-116">**Element**</span></span>|<span data-ttu-id="09396-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09396-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="09396-118">SuggestionsViewOptions</span><span class="sxs-lookup"><span data-stu-id="09396-118">SuggestionsViewOptions</span></span>](suggestionsviewoptions.md) <br/> |<span data-ttu-id="09396-119">Enthält die Optionen zum Abrufen von Informationen zu Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="09396-119">Contains the options for obtaining meeting suggestion information.</span></span>  <br/> <span data-ttu-id="09396-120">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="09396-120">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest/SuggestionViewOptions` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="09396-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="09396-121">Text value</span></span>

<span data-ttu-id="09396-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="09396-122">A text value is required.</span></span> <span data-ttu-id="09396-123">In der folgenden Tabelle sind die möglichen Werte für dieses Element aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="09396-123">The following table lists the possible values for this element:</span></span>
  
|<span data-ttu-id="09396-124">**Wert**</span><span class="sxs-lookup"><span data-stu-id="09396-124">**Value**</span></span>|<span data-ttu-id="09396-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="09396-125">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="09396-126">**Hervorragend**</span><span class="sxs-lookup"><span data-stu-id="09396-126">**Excellent**</span></span> <br/> |<span data-ttu-id="09396-127">0% der Teilnehmer haben einen Konflikt mit der vorgeschlagenen Besprechungszeit.</span><span class="sxs-lookup"><span data-stu-id="09396-127">0% of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
|<span data-ttu-id="09396-128">**Gut**</span><span class="sxs-lookup"><span data-stu-id="09396-128">**Good**</span></span> <br/> |<span data-ttu-id="09396-129">Der Prozentsatz, der als "gut" gilt, wird mithilfe des [GoodThreshold](goodthreshold.md) -Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09396-129">The percentage that is considered good is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="09396-130">**Messe**</span><span class="sxs-lookup"><span data-stu-id="09396-130">**Fair**</span></span> <br/> |<span data-ttu-id="09396-131">Der Prozentsatz, der als fair betrachtet wird, wird mithilfe des [GoodThreshold](goodthreshold.md) -Elements festgelegt.</span><span class="sxs-lookup"><span data-stu-id="09396-131">The percentage that is considered fair is set by using the [GoodThreshold](goodthreshold.md) element.</span></span>  <br/> |
|<span data-ttu-id="09396-132">**mangelhaft**</span><span class="sxs-lookup"><span data-stu-id="09396-132">**Poor**</span></span> <br/> |<span data-ttu-id="09396-133">50% oder mehr der Teilnehmer haben einen Konflikt mit der vorgeschlagenen Besprechungszeit.</span><span class="sxs-lookup"><span data-stu-id="09396-133">50% or more of the attendees have a conflict with the suggested meeting time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="09396-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="09396-134">Remarks</span></span>

<span data-ttu-id="09396-135">Dieses Element ist erforderlich, wenn das [SuggestionsViewOptions](suggestionsviewoptions.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="09396-135">This element is required if the [SuggestionsViewOptions](suggestionsviewoptions.md) element is used.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="09396-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="09396-136">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="09396-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="09396-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="09396-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="09396-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="09396-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="09396-139">Schema Name</span></span>  <br/> |<span data-ttu-id="09396-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="09396-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="09396-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="09396-141">Validation File</span></span>  <br/> |<span data-ttu-id="09396-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="09396-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="09396-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="09396-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="09396-144">False</span><span class="sxs-lookup"><span data-stu-id="09396-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="09396-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="09396-145">See also</span></span>



[<span data-ttu-id="09396-146">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="09396-146">GetUserAvailability operation</span></span>](getuseravailability-operation.md)


[<span data-ttu-id="09396-147">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="09396-147">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

