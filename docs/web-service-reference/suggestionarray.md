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
description: Das SuggestionArray-Element enthält ein Array von Besprechungs Vorschlägen.
ms.openlocfilehash: ec982417c39569820beef82ae837eacbe316740c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44466675"
---
# <a name="suggestionarray"></a><span data-ttu-id="c8ca1-103">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="c8ca1-103">SuggestionArray</span></span>

<span data-ttu-id="c8ca1-104">Das **SuggestionArray** -Element enthält ein Array von Besprechungs Vorschlägen.</span><span class="sxs-lookup"><span data-stu-id="c8ca1-104">The **SuggestionArray** element contains an array of meeting suggestions.</span></span> 
  
[<span data-ttu-id="c8ca1-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c8ca1-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="c8ca1-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="c8ca1-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="c8ca1-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="c8ca1-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="c8ca1-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="c8ca1-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="c8ca1-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="c8ca1-109">SuggestionArray</span></span>](suggestionarray.md)
  
```xml
<SuggestionArray>
   <Suggestion>...</Suggestion>
</SuggestionArray>
```

 <span data-ttu-id="c8ca1-110">**ArrayOfSuggestion**</span><span class="sxs-lookup"><span data-stu-id="c8ca1-110">**ArrayOfSuggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c8ca1-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ca1-111">Attributes and elements</span></span>

<span data-ttu-id="c8ca1-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c8ca1-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c8ca1-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="c8ca1-113">Attributes</span></span>

<span data-ttu-id="c8ca1-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="c8ca1-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c8ca1-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ca1-115">Child elements</span></span>

|<span data-ttu-id="c8ca1-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8ca1-116">**Element**</span></span>|<span data-ttu-id="c8ca1-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8ca1-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ca1-118">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="c8ca1-118">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="c8ca1-119">Stellt einen einzelnen Besprechungs Vorschlag dar.</span><span class="sxs-lookup"><span data-stu-id="c8ca1-119">Represents a single meeting suggestion.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c8ca1-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c8ca1-120">Parent elements</span></span>

|<span data-ttu-id="c8ca1-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="c8ca1-121">**Element**</span></span>|<span data-ttu-id="c8ca1-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c8ca1-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c8ca1-123">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="c8ca1-123">SuggestionDayResult</span></span>](suggestiondayresult.md) <br/> |<span data-ttu-id="c8ca1-124">Stellt einen einzelnen Tag dar, der vorgeschlagene Besprechungszeiten enthält.</span><span class="sxs-lookup"><span data-stu-id="c8ca1-124">Represents a single day that contains suggested meeting times.</span></span>  <br/> <span data-ttu-id="c8ca1-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="c8ca1-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c8ca1-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="c8ca1-126">Remarks</span></span>

<span data-ttu-id="c8ca1-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c8ca1-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c8ca1-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="c8ca1-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c8ca1-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="c8ca1-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c8ca1-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c8ca1-130">Schema Name</span></span>  <br/> |<span data-ttu-id="c8ca1-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c8ca1-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="c8ca1-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c8ca1-132">Validation File</span></span>  <br/> |<span data-ttu-id="c8ca1-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c8ca1-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c8ca1-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="c8ca1-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="c8ca1-135">False</span><span class="sxs-lookup"><span data-stu-id="c8ca1-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c8ca1-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c8ca1-136">See also</span></span>



[<span data-ttu-id="c8ca1-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="c8ca1-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="c8ca1-138">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="c8ca1-138">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="c8ca1-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="c8ca1-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

