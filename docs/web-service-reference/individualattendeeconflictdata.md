---
title: IndividualAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IndividualAttendeeConflictData
api_type:
- schema
ms.assetid: d45d3c34-abe1-40da-afd3-23bc5c3ef474
description: Das IndividualAttendeeConflictData-Element enthält eines Benutzers oder Frei/Gebucht-Status für ein Time-Fenster, das zur selben Zeit als die Uhrzeit der vorgeschlagenen Besprechung auftritt, des Kontakts im Vorschlag-Element identifiziert.
ms.openlocfilehash: 0bd164e08a6f3685415452b7c82a4220cf69d792
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829930"
---
# <a name="individualattendeeconflictdata"></a><span data-ttu-id="41b86-103">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="41b86-103">IndividualAttendeeConflictData</span></span>

<span data-ttu-id="41b86-104">Das **IndividualAttendeeConflictData** -Element enthält eines Benutzers oder Frei/Gebucht-Status für ein Time-Fenster, das zur selben Zeit als die Uhrzeit der vorgeschlagenen Besprechung auftritt, des Kontakts im [Vorschlag](suggestion.md) -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="41b86-104">The **IndividualAttendeeConflictData** element contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
[<span data-ttu-id="41b86-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="41b86-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="41b86-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="41b86-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="41b86-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="41b86-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="41b86-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="41b86-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="41b86-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="41b86-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="41b86-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="41b86-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="41b86-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="41b86-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="41b86-112">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="41b86-112">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md)
  
```xml
<IndividualAttendeeConflictData>
   <BusyType>...</BusyType>
</IndividualAttendeeConflictData>
```

 <span data-ttu-id="41b86-113">**IndividualAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="41b86-113">**IndividualAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="41b86-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="41b86-114">Attributes and elements</span></span>

<span data-ttu-id="41b86-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="41b86-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="41b86-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="41b86-116">Attributes</span></span>

<span data-ttu-id="41b86-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="41b86-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="41b86-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41b86-118">Child elements</span></span>

|<span data-ttu-id="41b86-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="41b86-119">**Element**</span></span>|<span data-ttu-id="41b86-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41b86-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41b86-121">BusyType</span><span class="sxs-lookup"><span data-stu-id="41b86-121">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="41b86-122">Stellt den Frei/Gebucht-Status eines Benutzers für einen Zeitraum für die vorgeschlagene Besprechung dar.</span><span class="sxs-lookup"><span data-stu-id="41b86-122">Represents the free/busy status of a user for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="41b86-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="41b86-123">Parent elements</span></span>

|<span data-ttu-id="41b86-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="41b86-124">**Element**</span></span>|<span data-ttu-id="41b86-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="41b86-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="41b86-126">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="41b86-126">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="41b86-127">Enthält ein Array von Conflict-Daten für die Teilnehmer in der [GetUserAvailabilityRequest](getuseravailabilityrequest.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="41b86-127">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="41b86-128">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="41b86-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="41b86-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="41b86-129">Remarks</span></span>

<span data-ttu-id="41b86-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="41b86-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="41b86-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="41b86-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="41b86-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="41b86-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="41b86-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="41b86-133">Schema Name</span></span>  <br/> |<span data-ttu-id="41b86-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="41b86-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="41b86-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="41b86-135">Validation File</span></span>  <br/> |<span data-ttu-id="41b86-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="41b86-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="41b86-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="41b86-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="41b86-138">False</span><span class="sxs-lookup"><span data-stu-id="41b86-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="41b86-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="41b86-139">See also</span></span>



[<span data-ttu-id="41b86-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="41b86-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="41b86-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="41b86-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="41b86-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="41b86-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

