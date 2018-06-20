---
title: MeetingTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingTime
api_type:
- schema
ms.assetid: 6e6d2d8b-e8a2-43e6-a715-0fc7d6dd44b9
description: Das MeetingTime-Element stellt eine vorgeschlagene Besprechungszeitraum dar.
ms.openlocfilehash: 1ea79be394124431aa1279ee94d5e5c6331d377b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830435"
---
# <a name="meetingtime"></a><span data-ttu-id="dbc24-103">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="dbc24-103">MeetingTime</span></span>

<span data-ttu-id="dbc24-104">Das **MeetingTime** -Element stellt eine vorgeschlagene Besprechungszeitraum dar.</span><span class="sxs-lookup"><span data-stu-id="dbc24-104">The **MeetingTime** element represents a suggested meeting time.</span></span> 
  
[<span data-ttu-id="dbc24-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dbc24-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="dbc24-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="dbc24-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="dbc24-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="dbc24-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="dbc24-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="dbc24-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="dbc24-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="dbc24-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="dbc24-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="dbc24-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="dbc24-111">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="dbc24-111">MeetingTime</span></span>](meetingtime.md)
  
```xml
<MeetingTime>...</MeetingTime
```

 <span data-ttu-id="dbc24-112">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="dbc24-112">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="dbc24-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="dbc24-113">Attributes and elements</span></span>

<span data-ttu-id="dbc24-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="dbc24-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="dbc24-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="dbc24-115">Attributes</span></span>

<span data-ttu-id="dbc24-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="dbc24-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="dbc24-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbc24-117">Child elements</span></span>

<span data-ttu-id="dbc24-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="dbc24-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="dbc24-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="dbc24-119">Parent elements</span></span>

|<span data-ttu-id="dbc24-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="dbc24-120">**Element**</span></span>|<span data-ttu-id="dbc24-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="dbc24-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="dbc24-122">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="dbc24-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="dbc24-123">Stellt ein einzelnes meeting Zeit Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="dbc24-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="dbc24-124">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="dbc24-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="dbc24-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="dbc24-125">Text value</span></span>

<span data-ttu-id="dbc24-126">Ein Textwert, der einen **DateTime** -Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="dbc24-126">A text value that represents a **dateTime** value is required.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="dbc24-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="dbc24-127">Remarks</span></span>

<span data-ttu-id="dbc24-128">Das [MeetingTime](meetingtime.md) -Element ist ein erforderliches untergeordnetes Element des Elements [Vorschlag](suggestion.md) .</span><span class="sxs-lookup"><span data-stu-id="dbc24-128">The [MeetingTime](meetingtime.md) element is a required child element of the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="dbc24-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="dbc24-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="dbc24-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="dbc24-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="dbc24-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="dbc24-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="dbc24-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="dbc24-132">Schema Name</span></span>  <br/> |<span data-ttu-id="dbc24-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="dbc24-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="dbc24-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="dbc24-134">Validation File</span></span>  <br/> |<span data-ttu-id="dbc24-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="dbc24-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="dbc24-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="dbc24-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="dbc24-137">False</span><span class="sxs-lookup"><span data-stu-id="dbc24-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="dbc24-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="dbc24-138">See also</span></span>



[<span data-ttu-id="dbc24-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="dbc24-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="dbc24-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="dbc24-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="dbc24-141">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="dbc24-141">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

