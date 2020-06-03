---
title: Vorschlag
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Suggestion
api_type:
- schema
ms.assetid: 040a5c8f-b62f-4d1d-9d2c-dc3c5e01481f
description: Das suggestion-Element stellt einen einzelnen Besprechungs Vorschlag dar.
ms.openlocfilehash: 25821abd5463ddba86a487709c8d2f8d928a94cc
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530380"
---
# <a name="suggestion"></a><span data-ttu-id="d14c8-103">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="d14c8-103">Suggestion</span></span>

<span data-ttu-id="d14c8-104">Das **Suggestion** -Element stellt einen einzelnen Besprechungs Vorschlag dar.</span><span class="sxs-lookup"><span data-stu-id="d14c8-104">The **Suggestion** element represents a single meeting suggestion.</span></span> 
  
[<span data-ttu-id="d14c8-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d14c8-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="d14c8-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="d14c8-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="d14c8-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="d14c8-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="d14c8-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="d14c8-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="d14c8-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="d14c8-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="d14c8-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="d14c8-110">Suggestion</span></span>](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 <span data-ttu-id="d14c8-111">**Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="d14c8-111">**Suggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d14c8-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d14c8-112">Attributes and elements</span></span>

<span data-ttu-id="d14c8-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d14c8-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d14c8-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="d14c8-114">Attributes</span></span>

<span data-ttu-id="d14c8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="d14c8-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d14c8-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d14c8-116">Child elements</span></span>

|<span data-ttu-id="d14c8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="d14c8-117">**Element**</span></span>|<span data-ttu-id="d14c8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d14c8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d14c8-119">Besprechungstermin</span><span class="sxs-lookup"><span data-stu-id="d14c8-119">MeetingTime</span></span>](meetingtime.md) <br/> |<span data-ttu-id="d14c8-120">Stellt eine vorgeschlagene Besprechungszeit dar.</span><span class="sxs-lookup"><span data-stu-id="d14c8-120">Represents a suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d14c8-121">Isworkzeit</span><span class="sxs-lookup"><span data-stu-id="d14c8-121">IsWorkTime</span></span>](isworktime.md) <br/> |<span data-ttu-id="d14c8-122">Stellt dar, ob die vorgeschlagene Besprechungszeit während der geplanten Arbeitsstunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="d14c8-122">Represents whether the suggested meeting time occurs during scheduled work hours.</span></span>  <br/> |
|[<span data-ttu-id="d14c8-123">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="d14c8-123">SuggestionQuality</span></span>](suggestionquality.md) <br/> |<span data-ttu-id="d14c8-124">Stellt die Qualität der vorgeschlagenen Besprechungszeit dar.</span><span class="sxs-lookup"><span data-stu-id="d14c8-124">Represents the quality of the suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="d14c8-125">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="d14c8-125">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="d14c8-126">Enthält ein Array von Informationen, die Konflikte zwischen Benutzern und Ressourcen und die vorgeschlagene Besprechungszeit beschreibt.</span><span class="sxs-lookup"><span data-stu-id="d14c8-126">Contains an array of information that describes conflicts between users and resources and the suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d14c8-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d14c8-127">Parent elements</span></span>

|<span data-ttu-id="d14c8-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="d14c8-128">**Element**</span></span>|<span data-ttu-id="d14c8-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d14c8-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d14c8-130">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="d14c8-130">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="d14c8-131">Enthält ein Array der vorgeschlagenen Besprechungszeiten.</span><span class="sxs-lookup"><span data-stu-id="d14c8-131">Contains an array of suggested meeting times.</span></span>  <br/> <span data-ttu-id="d14c8-132">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d14c8-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d14c8-133">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d14c8-133">Remarks</span></span>

<span data-ttu-id="d14c8-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d14c8-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d14c8-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d14c8-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d14c8-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="d14c8-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d14c8-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d14c8-137">Schema Name</span></span>  <br/> |<span data-ttu-id="d14c8-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d14c8-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="d14c8-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d14c8-139">Validation File</span></span>  <br/> |<span data-ttu-id="d14c8-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d14c8-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d14c8-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d14c8-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="d14c8-142">False</span><span class="sxs-lookup"><span data-stu-id="d14c8-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d14c8-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d14c8-143">See also</span></span>



[<span data-ttu-id="d14c8-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d14c8-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d14c8-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d14c8-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d14c8-146">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="d14c8-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

