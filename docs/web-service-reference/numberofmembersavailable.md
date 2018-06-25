---
title: NumberOfMembersAvailable
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembersAvailable
api_type:
- schema
ms.assetid: e367a278-1622-4b65-955f-2d4b2fc6e4d7
description: Das Element NumberOfMembersAvailable stellt die Anzahl der Mitglieder der Verteilerliste, die für einen Zeitraum vorgeschlagenen Besprechung zur Verfügung stehen. Dieses Element stellt Member für die der Status frei ist.
ms.openlocfilehash: 8669f61fbd640c160ad54739c5a15407b3dd470a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830641"
---
# <a name="numberofmembersavailable"></a><span data-ttu-id="191ee-104">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="191ee-104">NumberOfMembersAvailable</span></span>

<span data-ttu-id="191ee-105">Das Element **NumberOfMembersAvailable** stellt die Anzahl der Mitglieder der Verteilerliste, die für einen Zeitraum vorgeschlagenen Besprechung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="191ee-105">The **NumberOfMembersAvailable** element represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="191ee-106">Dieses Element stellt Member für die der Status **frei**ist.</span><span class="sxs-lookup"><span data-stu-id="191ee-106">This element represents members for whom the status is **Free**.</span></span>
  
[<span data-ttu-id="191ee-107">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="191ee-107">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="191ee-108">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="191ee-108">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="191ee-109">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="191ee-109">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="191ee-110">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="191ee-110">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="191ee-111">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="191ee-111">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="191ee-112">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="191ee-112">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="191ee-113">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="191ee-113">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="191ee-114">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="191ee-114">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="191ee-115">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="191ee-115">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md)
  
```xml
<NumberOfMembersAvailable>...</NumberOfMembersAvailable>
```

 <span data-ttu-id="191ee-116">**int**</span><span class="sxs-lookup"><span data-stu-id="191ee-116">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="191ee-117">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="191ee-117">Attributes and elements</span></span>

<span data-ttu-id="191ee-118">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="191ee-118">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="191ee-119">Attribute</span><span class="sxs-lookup"><span data-stu-id="191ee-119">Attributes</span></span>

<span data-ttu-id="191ee-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="191ee-120">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="191ee-121">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="191ee-121">Child elements</span></span>

<span data-ttu-id="191ee-122">Keine.</span><span class="sxs-lookup"><span data-stu-id="191ee-122">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="191ee-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="191ee-123">Parent elements</span></span>

|<span data-ttu-id="191ee-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="191ee-124">**Element**</span></span>|<span data-ttu-id="191ee-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="191ee-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="191ee-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="191ee-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="191ee-127">Enthält Konfliktinformationen über die Anzahl der Benutzer, die verfügbar sind, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die nicht zu Ihrer Verfügbarkeit einsehen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit verfügen aggregierte.</span><span class="sxs-lookup"><span data-stu-id="191ee-127">Contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="191ee-128">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="191ee-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="191ee-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="191ee-129">Remarks</span></span>

<span data-ttu-id="191ee-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="191ee-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="191ee-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="191ee-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="191ee-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="191ee-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="191ee-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="191ee-133">Schema Name</span></span>  <br/> |<span data-ttu-id="191ee-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="191ee-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="191ee-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="191ee-135">Validation File</span></span>  <br/> |<span data-ttu-id="191ee-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="191ee-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="191ee-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="191ee-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="191ee-138">False</span><span class="sxs-lookup"><span data-stu-id="191ee-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="191ee-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="191ee-139">See also</span></span>



[<span data-ttu-id="191ee-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="191ee-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="191ee-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="191ee-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="191ee-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="191ee-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

