---
title: IsWorkTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsWorkTime
api_type:
- schema
ms.assetid: 5243dd19-3593-4a81-bb2d-90496e04cb98
description: Das IsWorkTime-Element darstellt, ob die Uhrzeit der vorgeschlagenen Besprechung während der geplanten Arbeitsstunden auftritt.
ms.openlocfilehash: c687b29df226ebb28cdf01d3a2da62590f790924
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830135"
---
# <a name="isworktime"></a><span data-ttu-id="85cba-103">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="85cba-103">IsWorkTime</span></span>

<span data-ttu-id="85cba-104">Das **IsWorkTime** -Element darstellt, ob die Uhrzeit der vorgeschlagenen Besprechung während der geplanten Arbeitsstunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="85cba-104">The **IsWorkTime** element represents whether the suggested meeting time occurs during scheduled work hours.</span></span> 
  
[<span data-ttu-id="85cba-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="85cba-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="85cba-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="85cba-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="85cba-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="85cba-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="85cba-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="85cba-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="85cba-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="85cba-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="85cba-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="85cba-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="85cba-111">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="85cba-111">IsWorkTime</span></span>](isworktime.md)
  
```xml
<IsWorkTime>true or false</IsWorkTime>
```

 <span data-ttu-id="85cba-112">**boolean**</span><span class="sxs-lookup"><span data-stu-id="85cba-112">**boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="85cba-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="85cba-113">Attributes and elements</span></span>

<span data-ttu-id="85cba-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="85cba-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="85cba-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="85cba-115">Attributes</span></span>

<span data-ttu-id="85cba-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="85cba-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="85cba-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85cba-117">Child elements</span></span>

<span data-ttu-id="85cba-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="85cba-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="85cba-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="85cba-119">Parent elements</span></span>

|<span data-ttu-id="85cba-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="85cba-120">**Element**</span></span>|<span data-ttu-id="85cba-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="85cba-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="85cba-122">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="85cba-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="85cba-123">Stellt ein einzelnes meeting Zeit Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="85cba-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="85cba-124">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="85cba-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="85cba-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="85cba-125">Text value</span></span>

<span data-ttu-id="85cba-126">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="85cba-126">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="85cba-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="85cba-127">Remarks</span></span>

<span data-ttu-id="85cba-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="85cba-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="85cba-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="85cba-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="85cba-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="85cba-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="85cba-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="85cba-131">Schema Name</span></span>  <br/> |<span data-ttu-id="85cba-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="85cba-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="85cba-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="85cba-133">Validation File</span></span>  <br/> |<span data-ttu-id="85cba-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="85cba-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="85cba-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="85cba-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="85cba-136">False</span><span class="sxs-lookup"><span data-stu-id="85cba-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="85cba-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="85cba-137">See also</span></span>



[<span data-ttu-id="85cba-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="85cba-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="85cba-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="85cba-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="85cba-140">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="85cba-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

