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
description: Das SuggestionDayResult-Element stellt einen einzelnen Tag dar, der vorgeschlagene Besprechungszeiten enthält.
ms.openlocfilehash: af907b62acefb4913814907722b98d326bd0535b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457991"
---
# <a name="suggestiondayresult"></a><span data-ttu-id="a25ce-103">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="a25ce-103">SuggestionDayResult</span></span>

<span data-ttu-id="a25ce-104">Das **SuggestionDayResult** -Element stellt einen einzelnen Tag dar, der vorgeschlagene Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="a25ce-104">The **SuggestionDayResult** element represents a single day that contains suggested meeting times.</span></span> 
  
[<span data-ttu-id="a25ce-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a25ce-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="a25ce-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="a25ce-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="a25ce-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="a25ce-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="a25ce-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="a25ce-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
```xml
<SuggestionDayResult>
   <Date>...</Date>
   <DayQuality>...</DayQuality>
   <SuggestionArray>...</SuggestionArray>
</SuggestionDayResult>
```

 <span data-ttu-id="a25ce-109">**SuggestionDayResult**</span><span class="sxs-lookup"><span data-stu-id="a25ce-109">**SuggestionDayResult**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a25ce-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a25ce-110">Attributes and elements</span></span>

<span data-ttu-id="a25ce-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a25ce-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a25ce-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="a25ce-112">Attributes</span></span>

<span data-ttu-id="a25ce-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a25ce-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a25ce-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a25ce-114">Child elements</span></span>

|<span data-ttu-id="a25ce-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a25ce-115">**Element**</span></span>|<span data-ttu-id="a25ce-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a25ce-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a25ce-117">Date</span><span class="sxs-lookup"><span data-stu-id="a25ce-117">Date</span></span>](date.md) <br/> |<span data-ttu-id="a25ce-118">Stellt das Datum dar, das die vorgeschlagenen Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="a25ce-118">Represents the date that contains the suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="a25ce-119">DayQuality</span><span class="sxs-lookup"><span data-stu-id="a25ce-119">DayQuality</span></span>](dayquality.md) <br/> |<span data-ttu-id="a25ce-120">Stellt die Qualität des Tages für das enthalten von Qualität vorgeschlagene Besprechungszeiten dar.</span><span class="sxs-lookup"><span data-stu-id="a25ce-120">Represents the quality of the day for containing quality suggested meeting times.</span></span>  <br/> |
|[<span data-ttu-id="a25ce-121">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="a25ce-121">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="a25ce-122">Enthält ein Array von Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="a25ce-122">Contains an array of meeting suggestions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a25ce-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a25ce-123">Parent elements</span></span>

|<span data-ttu-id="a25ce-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="a25ce-124">**Element**</span></span>|<span data-ttu-id="a25ce-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a25ce-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a25ce-126">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="a25ce-126">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md) <br/> |<span data-ttu-id="a25ce-127">Enthält ein Array von Besprechungs Vorschlägen nach Datum organisiert.</span><span class="sxs-lookup"><span data-stu-id="a25ce-127">Contains an array of meeting suggestions organized by date.</span></span>  <br/> <span data-ttu-id="a25ce-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="a25ce-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a25ce-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a25ce-129">Remarks</span></span>

<span data-ttu-id="a25ce-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a25ce-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a25ce-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a25ce-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a25ce-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="a25ce-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a25ce-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a25ce-133">Schema Name</span></span>  <br/> |<span data-ttu-id="a25ce-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a25ce-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="a25ce-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a25ce-135">Validation File</span></span>  <br/> |<span data-ttu-id="a25ce-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a25ce-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a25ce-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a25ce-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="a25ce-138">False</span><span class="sxs-lookup"><span data-stu-id="a25ce-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a25ce-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a25ce-139">See also</span></span>



[<span data-ttu-id="a25ce-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a25ce-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="a25ce-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="a25ce-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="a25ce-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="a25ce-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

