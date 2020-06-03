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
description: Das IndividualAttendeeConflictData-Element enthält den Frei/Gebucht-Status eines Benutzers oder Kontakts für ein Zeitfenster, das gleichzeitig mit der im suggestion-Element identifizierten vorgeschlagenen Besprechungszeit auftritt.
ms.openlocfilehash: 55210230259b78e5ed9c4f0744aae003cf2e7ae5
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44459314"
---
# <a name="individualattendeeconflictdata"></a><span data-ttu-id="f234e-103">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f234e-103">IndividualAttendeeConflictData</span></span>

<span data-ttu-id="f234e-104">Das **IndividualAttendeeConflictData** -Element enthält den Frei/Gebucht-Status eines Benutzers oder Kontakts für ein Zeitfenster, das gleichzeitig mit der im [Suggestion](suggestion.md) -Element identifizierten vorgeschlagenen Besprechungszeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="f234e-104">The **IndividualAttendeeConflictData** element contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
[<span data-ttu-id="f234e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f234e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="f234e-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f234e-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="f234e-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="f234e-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="f234e-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f234e-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="f234e-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="f234e-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="f234e-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="f234e-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="f234e-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f234e-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="f234e-112">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f234e-112">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md)
  
```xml
<IndividualAttendeeConflictData>
   <BusyType>...</BusyType>
</IndividualAttendeeConflictData>
```

 <span data-ttu-id="f234e-113">**IndividualAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="f234e-113">**IndividualAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f234e-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f234e-114">Attributes and elements</span></span>

<span data-ttu-id="f234e-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f234e-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f234e-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="f234e-116">Attributes</span></span>

<span data-ttu-id="f234e-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="f234e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f234e-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f234e-118">Child elements</span></span>

|<span data-ttu-id="f234e-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f234e-119">**Element**</span></span>|<span data-ttu-id="f234e-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f234e-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f234e-121">Busytype</span><span class="sxs-lookup"><span data-stu-id="f234e-121">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="f234e-122">Stellt den Frei/Gebucht-Status eines Benutzers für eine vorgeschlagene Besprechungszeit dar.</span><span class="sxs-lookup"><span data-stu-id="f234e-122">Represents the free/busy status of a user for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f234e-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f234e-123">Parent elements</span></span>

|<span data-ttu-id="f234e-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="f234e-124">**Element**</span></span>|<span data-ttu-id="f234e-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f234e-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f234e-126">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f234e-126">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="f234e-127">Enthält ein Array von Konfliktdaten für Teilnehmer, die in der [GetUserAvailabilityRequest](getuseravailabilityrequest.md)identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="f234e-127">Contains an array of conflict data for attendees identified in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md).</span></span>  <br/> <span data-ttu-id="f234e-128">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="f234e-128">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f234e-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f234e-129">Remarks</span></span>

<span data-ttu-id="f234e-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f234e-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f234e-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f234e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f234e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="f234e-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f234e-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f234e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="f234e-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f234e-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="f234e-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f234e-135">Validation File</span></span>  <br/> |<span data-ttu-id="f234e-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f234e-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f234e-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f234e-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="f234e-138">False</span><span class="sxs-lookup"><span data-stu-id="f234e-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f234e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f234e-139">See also</span></span>



[<span data-ttu-id="f234e-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f234e-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="f234e-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f234e-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="f234e-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="f234e-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

