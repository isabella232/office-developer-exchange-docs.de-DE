---
title: SuggestionArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionArray
api_type:
- schema
ms.assetid: c1c26008-7b14-4563-8db5-bceb0f475b1b
description: Das SuggestionArray-Element enthält ein Array von besprechungsvorschlägen.
ms.openlocfilehash: d595ae77de293a1975e15102f3f2c3395e6da633
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839134"
---
# <a name="suggestionarray"></a><span data-ttu-id="3e3d1-103">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="3e3d1-103">SuggestionArray</span></span>

<span data-ttu-id="3e3d1-104">Das **SuggestionArray** -Element enthält ein Array von besprechungsvorschlägen.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-104">The **SuggestionArray** element contains an array of meeting suggestions.</span></span> 
  
[<span data-ttu-id="3e3d1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3e3d1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="3e3d1-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="3e3d1-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="3e3d1-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="3e3d1-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="3e3d1-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="3e3d1-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="3e3d1-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="3e3d1-109">SuggestionArray</span></span>](suggestionarray.md)
  
```xml
<SuggestionArray>
   <Suggestion>...</Suggestion>
</SuggestionArray>
```

 <span data-ttu-id="3e3d1-110">**ArrayOfSuggestion**</span><span class="sxs-lookup"><span data-stu-id="3e3d1-110">**ArrayOfSuggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3e3d1-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3e3d1-111">Attributes and elements</span></span>

<span data-ttu-id="3e3d1-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3e3d1-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="3e3d1-113">Attributes</span></span>

<span data-ttu-id="3e3d1-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3e3d1-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e3d1-115">Child elements</span></span>

|<span data-ttu-id="3e3d1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e3d1-116">**Element**</span></span>|<span data-ttu-id="3e3d1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e3d1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e3d1-118">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="3e3d1-118">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="3e3d1-119">Stellt eine einzelne besprechungsvorschlag dar.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-119">Represents a single meeting suggestion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3e3d1-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3e3d1-120">Parent elements</span></span>

|<span data-ttu-id="3e3d1-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="3e3d1-121">**Element**</span></span>|<span data-ttu-id="3e3d1-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3e3d1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3e3d1-123">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="3e3d1-123">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="3e3d1-124">Stellt einen einzelnen Tag, der Zeiten der vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-124">Represents a single day that contains suggested meeting times.</span></span>  <br/> <span data-ttu-id="3e3d1-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3e3d1-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3e3d1-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3e3d1-126">Remarks</span></span>

<span data-ttu-id="3e3d1-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3e3d1-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3e3d1-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3e3d1-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3e3d1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="3e3d1-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3e3d1-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3e3d1-130">Schema Name</span></span>  <br/> |<span data-ttu-id="3e3d1-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3e3d1-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="3e3d1-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3e3d1-132">Validation File</span></span>  <br/> |<span data-ttu-id="3e3d1-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3e3d1-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3e3d1-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3e3d1-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="3e3d1-135">False</span><span class="sxs-lookup"><span data-stu-id="3e3d1-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3e3d1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3e3d1-136">See also</span></span>



[<span data-ttu-id="3e3d1-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3e3d1-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3e3d1-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3e3d1-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3e3d1-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="3e3d1-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

