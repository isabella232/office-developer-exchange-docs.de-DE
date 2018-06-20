---
title: TooBigGroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TooBigGroupAttendeeConflictData
api_type:
- schema
ms.assetid: 1512428d-ce22-4da9-b1c1-446b4bcd0a21
description: Das TooBigGroupAttendeeConflictData-Element stellt einen Teilnehmer, der als Verteilerliste aufgelöst wurde, aber die Verteilerliste war zu groß, um zu erweitern.
ms.openlocfilehash: 1137368d13cb5b88fd2a7866cadc6d69b783c75b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839252"
---
# <a name="toobiggroupattendeeconflictdata"></a><span data-ttu-id="25245-103">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="25245-103">TooBigGroupAttendeeConflictData</span></span>

<span data-ttu-id="25245-104">Das **TooBigGroupAttendeeConflictData** -Element stellt einen Teilnehmer, der als Verteilerliste aufgelöst wurde, aber die Verteilerliste war zu groß, um zu erweitern.</span><span class="sxs-lookup"><span data-stu-id="25245-104">The **TooBigGroupAttendeeConflictData** element represents an attendee that was resolved as a distribution list but the distribution list was too large to expand.</span></span> 
  
[<span data-ttu-id="25245-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="25245-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="25245-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="25245-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="25245-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="25245-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="25245-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="25245-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="25245-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="25245-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="25245-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="25245-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="25245-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="25245-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="25245-112">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="25245-112">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md)
  
```xml
<TooBigGroupAttendeeConflictData/>
```

 <span data-ttu-id="25245-113">**TooBigGroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="25245-113">**TooBigGroupAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="25245-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="25245-114">Attributes and elements</span></span>

<span data-ttu-id="25245-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="25245-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="25245-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="25245-116">Attributes</span></span>

<span data-ttu-id="25245-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="25245-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="25245-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25245-118">Child elements</span></span>

<span data-ttu-id="25245-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="25245-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="25245-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="25245-120">Parent elements</span></span>

|<span data-ttu-id="25245-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="25245-121">**Element**</span></span>|<span data-ttu-id="25245-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="25245-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="25245-123">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="25245-123">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="25245-124">Enthält ein Array von Conflict-Daten für die Teilnehmer in der [GetUserAvailabilityRequest](getuseravailabilityrequest.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="25245-124">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="25245-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="25245-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="25245-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="25245-126">Remarks</span></span>

<span data-ttu-id="25245-127">Verteilerlisten mit mehr als 100 Mitgliedern können nicht erweitert werden.</span><span class="sxs-lookup"><span data-stu-id="25245-127">Distribution lists that contain more than 100 members cannot be expanded.</span></span>
  
<span data-ttu-id="25245-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="25245-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="25245-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="25245-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="25245-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="25245-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="25245-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="25245-131">Schema Name</span></span>  <br/> |<span data-ttu-id="25245-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="25245-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="25245-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="25245-133">Validation File</span></span>  <br/> |<span data-ttu-id="25245-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="25245-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="25245-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="25245-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="25245-136">False</span><span class="sxs-lookup"><span data-stu-id="25245-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="25245-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="25245-137">See also</span></span>



[<span data-ttu-id="25245-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="25245-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="25245-139">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="25245-139">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="25245-140">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="25245-140">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

