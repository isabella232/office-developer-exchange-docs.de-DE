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
description: Vorschlag-Element stellt ein einzelnes besprechungsvorschlag.
ms.openlocfilehash: 24e2db1e0eabe35f7c971b0f1dbcbd333358f171
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839133"
---
# <a name="suggestion"></a><span data-ttu-id="76941-103">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="76941-103">Suggestion</span></span>

<span data-ttu-id="76941-104">**Vorschlag** -Element stellt ein einzelnes besprechungsvorschlag.</span><span class="sxs-lookup"><span data-stu-id="76941-104">The **Suggestion** element represents a single meeting suggestion.</span></span> 
  
[<span data-ttu-id="76941-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="76941-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="76941-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="76941-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="76941-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="76941-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="76941-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="76941-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="76941-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="76941-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="76941-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="76941-110">Suggestion</span></span>](suggestion.md)
  
```xml
<Suggestion>
   <MeetingTime>...</MeetingTime>
   <IsWorkTime>...</IsWorkTime>
   <SuggestionQuality>...</SuggestionQuality>
   <AttendeeConflictDataArray>...</AttendeeConflictDataArray>
</Suggestion>
```

 <span data-ttu-id="76941-111">**Vorschlag**</span><span class="sxs-lookup"><span data-stu-id="76941-111">**Suggestion**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="76941-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="76941-112">Attributes and elements</span></span>

<span data-ttu-id="76941-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="76941-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="76941-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="76941-114">Attributes</span></span>

<span data-ttu-id="76941-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="76941-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="76941-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76941-116">Child elements</span></span>

|<span data-ttu-id="76941-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="76941-117">**Element**</span></span>|<span data-ttu-id="76941-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76941-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76941-119">MeetingTime</span><span class="sxs-lookup"><span data-stu-id="76941-119">MeetingTime</span></span>](meetingtime.md) <br/> |<span data-ttu-id="76941-120">Stellt eine vorgeschlagene Besprechungszeitraum dar.</span><span class="sxs-lookup"><span data-stu-id="76941-120">Represents a suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="76941-121">IsWorkTime</span><span class="sxs-lookup"><span data-stu-id="76941-121">IsWorkTime</span></span>](isworktime.md) <br/> |<span data-ttu-id="76941-122">Stellt dar, ob die Uhrzeit der vorgeschlagenen Besprechung während der geplanten Arbeitsstunden auftritt.</span><span class="sxs-lookup"><span data-stu-id="76941-122">Represents whether the suggested meeting time occurs during scheduled work hours.</span></span>  <br/> |
|[<span data-ttu-id="76941-123">SuggestionQuality</span><span class="sxs-lookup"><span data-stu-id="76941-123">SuggestionQuality</span></span>](suggestionquality.md) <br/> |<span data-ttu-id="76941-124">Die Qualität der vorgeschlagenen Besprechungszeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="76941-124">Represents the quality of the suggested meeting time.</span></span>  <br/> |
|[<span data-ttu-id="76941-125">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="76941-125">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="76941-126">Ein Array von Informationen über Konflikte zwischen Benutzern und Ressourcen und die Uhrzeit der vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="76941-126">Contains an array of information that describes conflicts between users and resources and the suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="76941-127">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="76941-127">Parent elements</span></span>

|<span data-ttu-id="76941-128">**Element**</span><span class="sxs-lookup"><span data-stu-id="76941-128">**Element**</span></span>|<span data-ttu-id="76941-129">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="76941-129">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="76941-130">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="76941-130">SuggestionArray</span></span>](suggestionarray.md) <br/> |<span data-ttu-id="76941-131">Ein Array von Zeiten der vorgeschlagenen Besprechung enthält.</span><span class="sxs-lookup"><span data-stu-id="76941-131">Contains an array of suggested meeting times.</span></span>  <br/> <span data-ttu-id="76941-132">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="76941-132">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="76941-133">Hinweise</span><span class="sxs-lookup"><span data-stu-id="76941-133">Remarks</span></span>

<span data-ttu-id="76941-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="76941-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="76941-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="76941-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="76941-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="76941-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="76941-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="76941-137">Schema Name</span></span>  <br/> |<span data-ttu-id="76941-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="76941-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="76941-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="76941-139">Validation File</span></span>  <br/> |<span data-ttu-id="76941-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="76941-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="76941-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="76941-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="76941-142">False</span><span class="sxs-lookup"><span data-stu-id="76941-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="76941-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="76941-143">See also</span></span>



[<span data-ttu-id="76941-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="76941-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="76941-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="76941-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="76941-146">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="76941-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

