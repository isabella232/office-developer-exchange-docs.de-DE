---
title: SuggestionQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionQuality
api_type:
- schema
ms.assetid: 734f1a58-adda-4830-973e-e84bf7b870d5
description: Das SuggestionQuality-Element darstellt, die Qualität der vorgeschlagenen Besprechungszeit.
ms.openlocfilehash: e67e0149226b36c22cdd00acd78f6582f826dd3e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839136"
---
# <a name="suggestionquality"></a><span data-ttu-id="0a5f8-103">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="0a5f8-103">SuggestionQuality</span></span>

<span data-ttu-id="0a5f8-104">Das **SuggestionQuality** -Element darstellt, die Qualität der vorgeschlagenen Besprechungszeit.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-104">The **SuggestionQuality** element represents the quality of the suggested meeting time.</span></span> 
  
[<span data-ttu-id="0a5f8-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0a5f8-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="0a5f8-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="0a5f8-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="0a5f8-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="0a5f8-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="0a5f8-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="0a5f8-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="0a5f8-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="0a5f8-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="0a5f8-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="0a5f8-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="0a5f8-111">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="0a5f8-111">SuggestionQuality</span></span>](suggestionquality.md)
  
```xml
<SuggestionQuality>Excellent or Good or Fair or Poor</SuggestionQuality>
```

 <span data-ttu-id="0a5f8-112">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="0a5f8-112">**SuggestionQuality**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="0a5f8-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0a5f8-113">Attributes and elements</span></span>

<span data-ttu-id="0a5f8-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0a5f8-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="0a5f8-115">Attributes</span></span>

<span data-ttu-id="0a5f8-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0a5f8-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a5f8-117">Child elements</span></span>

<span data-ttu-id="0a5f8-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-118">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0a5f8-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0a5f8-119">Parent elements</span></span>

|<span data-ttu-id="0a5f8-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="0a5f8-120">**Element**</span></span>|<span data-ttu-id="0a5f8-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0a5f8-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0a5f8-122">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="0a5f8-122">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="0a5f8-123">Stellt ein einzelnes meeting Zeit Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-123">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="0a5f8-124">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="0a5f8-124">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0a5f8-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="0a5f8-125">Text value</span></span>

<span data-ttu-id="0a5f8-126">Ein Textwert, der einen **SuggestionQuality** Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-126">A text value that represents a **SuggestionQuality** value is required.</span></span> <span data-ttu-id="0a5f8-127">Im Folgenden sind die möglichen Werte aufgeführt:</span><span class="sxs-lookup"><span data-stu-id="0a5f8-127">The following are the possible values:</span></span> 
  
- <span data-ttu-id="0a5f8-128">**Hervorragend** 100 Prozent der Benutzer und Ressourcen stehen für die Uhrzeit der vorgeschlagenen Besprechung.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-128">**Excellent** 100 percent of users and resources are available for the suggested meeting time.</span></span> 
    
- <span data-ttu-id="0a5f8-129">**Eine gute** Der minimale Prozentsatz der Benutzer und Ressourcen verfügbar ist gleich oder größer als die [GoodThreshold](goodthreshold.md) -Elementwert plus 50.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-129">**Good** The minimum percentage of users and resources available is equal to or greater than the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> 
    
- <span data-ttu-id="0a5f8-130">**Fair** Der maximale Prozentsatz von Benutzern und Ressourcen für einen Zeitraum vorgeschlagenen Besprechung zur Verfügung entspricht dem Elementwert [GoodThreshold](goodthreshold.md) plus 50.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-130">**Fair** The maximum percentage of users and resources available for a suggested meeting time is equal to the [GoodThreshold](goodthreshold.md) element value plus 50.</span></span> <span data-ttu-id="0a5f8-131">Der Mindestwert für eine **angemessene** Qualität Besprechungszeit ist 50 Prozent.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-131">The minimum value for a **Fair** quality meeting time is 50 percent.</span></span> 
    
- <span data-ttu-id="0a5f8-132">**Schlechte** Weniger als 50 Prozent der Benutzer und Ressourcen stehen für die Uhrzeit der vorgeschlagenen Besprechung zur Verfügung.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-132">**Poor** Less than 50 percent of the users and resources are available for the suggested meeting time.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0a5f8-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0a5f8-133">Remarks</span></span>

<span data-ttu-id="0a5f8-134">Die **SuggestionQuality** ist auch der Typ für die [DayQuality](dayquality.md) und die [MinimumSuggestionQuality](minimumsuggestionquality.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-134">The **SuggestionQuality** type is also the type for the [DayQuality](dayquality.md) and the [MinimumSuggestionQuality](minimumsuggestionquality.md) elements.</span></span> 
  
<span data-ttu-id="0a5f8-135">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="0a5f8-135">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="0a5f8-136">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0a5f8-136">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0a5f8-137">Namespace</span><span class="sxs-lookup"><span data-stu-id="0a5f8-137">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0a5f8-138">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0a5f8-138">Schema Name</span></span>  <br/> |<span data-ttu-id="0a5f8-139">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0a5f8-139">Types schema</span></span>  <br/> |
|<span data-ttu-id="0a5f8-140">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0a5f8-140">Validation File</span></span>  <br/> |<span data-ttu-id="0a5f8-141">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0a5f8-141">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0a5f8-142">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0a5f8-142">Can be Empty</span></span>  <br/> |<span data-ttu-id="0a5f8-143">False</span><span class="sxs-lookup"><span data-stu-id="0a5f8-143">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0a5f8-144">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0a5f8-144">See also</span></span>



[<span data-ttu-id="0a5f8-145">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0a5f8-145">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="0a5f8-146">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="0a5f8-146">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="0a5f8-147">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="0a5f8-147">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

