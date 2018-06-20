---
title: DayQuality
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayQuality
api_type:
- schema
ms.assetid: cd0eb239-6e7f-4a5a-b245-659f170550b7
description: Das DayQuality-Element darstellt, die Qualität des Tages für, wie oft Qualität vorgeschlagenen Besprechung enthält.
ms.openlocfilehash: 156d5bc58d481c9c812793da4722272ac76adaad
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757885"
---
# <a name="dayquality"></a><span data-ttu-id="fc27b-103">DayQuality</span><span class="sxs-lookup"><span data-stu-id="fc27b-103">DayQuality</span></span>

<span data-ttu-id="fc27b-104">Das **DayQuality** -Element darstellt, die Qualität des Tags, die Qualität vorgeschlagene Besprechungszeiten enthalten.</span><span class="sxs-lookup"><span data-stu-id="fc27b-104">The **DayQuality** element represents the quality of the day for containing quality suggested meeting times.</span></span> 
  
- [<span data-ttu-id="fc27b-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fc27b-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="fc27b-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="fc27b-106">SuggestionsResponse</span></span>](suggestionsresponse.md) 
- [<span data-ttu-id="fc27b-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="fc27b-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)  
- [<span data-ttu-id="fc27b-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="fc27b-108">SuggestionDayResult</span></span>](suggestiondayresult.md) 
- [<span data-ttu-id="fc27b-109">DayQuality</span><span class="sxs-lookup"><span data-stu-id="fc27b-109">DayQuality</span></span>](dayquality.md)
  
```xml
<DayQuality>Excellent or Good or Fair or Poor</DayQuality>
```

<span data-ttu-id="fc27b-110">**SuggestionQuality**</span><span class="sxs-lookup"><span data-stu-id="fc27b-110">**SuggestionQuality**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="fc27b-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fc27b-111">Attributes and elements</span></span>

<span data-ttu-id="fc27b-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fc27b-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fc27b-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="fc27b-113">Attributes</span></span>

<span data-ttu-id="fc27b-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc27b-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fc27b-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc27b-115">Child elements</span></span>

<span data-ttu-id="fc27b-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="fc27b-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fc27b-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fc27b-117">Parent elements</span></span>

|<span data-ttu-id="fc27b-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="fc27b-118">**Element**</span></span>|<span data-ttu-id="fc27b-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fc27b-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fc27b-120">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="fc27b-120">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="fc27b-121">Stellt einen einzelnen Tag, der Zeiten der vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="fc27b-121">Represents a single day that contains suggested meeting times.</span></span>  <br/><br/><span data-ttu-id="fc27b-122">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="fc27b-122">The following is the XPath 2.0 expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="fc27b-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="fc27b-123">Text value</span></span>

<span data-ttu-id="fc27b-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="fc27b-124">A text value is required.</span></span> <span data-ttu-id="fc27b-125">Es folgen die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="fc27b-125">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="fc27b-126">**Ausgezeichnet**</span><span class="sxs-lookup"><span data-stu-id="fc27b-126">**Excellent**</span></span>   
- <span data-ttu-id="fc27b-127">**Eine gute**</span><span class="sxs-lookup"><span data-stu-id="fc27b-127">**Good**</span></span>    
- <span data-ttu-id="fc27b-128">**Fair**</span><span class="sxs-lookup"><span data-stu-id="fc27b-128">**Fair**</span></span>    
- <span data-ttu-id="fc27b-129">**Schlechte**</span><span class="sxs-lookup"><span data-stu-id="fc27b-129">**Poor**</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fc27b-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fc27b-130">Remarks</span></span>

<span data-ttu-id="fc27b-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fc27b-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fc27b-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fc27b-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fc27b-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="fc27b-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fc27b-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fc27b-134">Schema Name</span></span>  <br/> |<span data-ttu-id="fc27b-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fc27b-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="fc27b-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fc27b-136">Validation File</span></span>  <br/> |<span data-ttu-id="fc27b-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fc27b-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fc27b-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fc27b-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="fc27b-139">False</span><span class="sxs-lookup"><span data-stu-id="fc27b-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fc27b-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fc27b-140">See also</span></span>

- [<span data-ttu-id="fc27b-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fc27b-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="fc27b-142">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fc27b-142">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="fc27b-143">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fc27b-143">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

