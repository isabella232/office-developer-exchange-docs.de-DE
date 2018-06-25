---
title: SuggestionDayResult
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- SuggestionDayResult
api_type:
- schema
ms.assetid: 916b1cbb-f2e3-471d-84b0-e33467616652
description: Das Element SuggestionDayResult stellt einen einzelnen Tag, der vorgeschlagenen Besprechungszeiten enthält.
ms.openlocfilehash: 7b75258a9e70f1ec6feed6a0b18beb76f356c7f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839135"
---
# <a name="suggestiondayresult"></a><span data-ttu-id="3c14d-103">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="3c14d-103">SuggestionDayResult</span></span>

<span data-ttu-id="3c14d-104">Das Element **SuggestionDayResult** stellt einen einzelnen Tag, der vorgeschlagenen Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="3c14d-104">The **SuggestionDayResult** element represents a single day that contains suggested meeting times.</span></span> 
  
[<span data-ttu-id="3c14d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3c14d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="3c14d-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="3c14d-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="3c14d-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="3c14d-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="3c14d-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="3c14d-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
```xml
<SuggestionDayResult>
   <Date>...</Date>
   <DayQuality>...</DayQuality>
   <SuggestionArray>...</SuggestionArray>
</SuggestionDayResult>
```

 <span data-ttu-id="3c14d-109">**SuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="3c14d-109">**SuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3c14d-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3c14d-110">Attributes and elements</span></span>

<span data-ttu-id="3c14d-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3c14d-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3c14d-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="3c14d-112">Attributes</span></span>

<span data-ttu-id="3c14d-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="3c14d-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3c14d-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c14d-114">Child elements</span></span>

|<span data-ttu-id="3c14d-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c14d-115">**Element**</span></span>|<span data-ttu-id="3c14d-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c14d-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c14d-117">Date</span><span class="sxs-lookup"><span data-stu-id="3c14d-117">Date</span></span>](date.md) <br/> |<span data-ttu-id="3c14d-118">Stellt das Datum, das die Zeiten vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="3c14d-118">Represents the date that contains the suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="3c14d-119">DayQuality</span><span class="sxs-lookup"><span data-stu-id="3c14d-119">DayQuality</span></span>](dayquality.md) <br/> |<span data-ttu-id="3c14d-120">Stellt die Qualität des Tages für, wie oft Qualität vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="3c14d-120">Represents the quality of the day for containing quality suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="3c14d-121">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="3c14d-121">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="3c14d-122">Enthält ein Array von besprechungsvorschlägen.</span><span class="sxs-lookup"><span data-stu-id="3c14d-122">Contains an array of meeting suggestions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3c14d-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3c14d-123">Parent elements</span></span>

|<span data-ttu-id="3c14d-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="3c14d-124">**Element**</span></span>|<span data-ttu-id="3c14d-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3c14d-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3c14d-126">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="3c14d-126">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="3c14d-127">Enthält ein Array von besprechungsvorschlägen nach Datum organisiert.</span><span class="sxs-lookup"><span data-stu-id="3c14d-127">Contains an array of meeting suggestions organized by date.</span></span>  <br/> <span data-ttu-id="3c14d-128">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3c14d-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3c14d-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3c14d-129">Remarks</span></span>

<span data-ttu-id="3c14d-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3c14d-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3c14d-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3c14d-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3c14d-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="3c14d-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3c14d-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3c14d-133">Schema Name</span></span>  <br/> |<span data-ttu-id="3c14d-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3c14d-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="3c14d-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3c14d-135">Validation File</span></span>  <br/> |<span data-ttu-id="3c14d-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3c14d-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3c14d-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3c14d-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="3c14d-138">False</span><span class="sxs-lookup"><span data-stu-id="3c14d-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3c14d-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3c14d-139">See also</span></span>



[<span data-ttu-id="3c14d-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3c14d-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="3c14d-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3c14d-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="3c14d-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="3c14d-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

