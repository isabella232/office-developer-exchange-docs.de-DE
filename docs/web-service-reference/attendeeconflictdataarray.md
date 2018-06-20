---
title: AttendeeConflictDataArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AttendeeConflictDataArray
api_type:
- schema
ms.assetid: 1d758547-28c5-4649-8334-427480c282d6
description: Das AttendeeConflictDataArray-Element enthält ein Array von Conflict-Daten für die abgefragte Teilnehmer bei der Konflikte GetUserAvailability identifiziert.
ms.openlocfilehash: 169312b8a3d37c014ba58fbfe094d786b134fc90
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757401"
---
# <a name="attendeeconflictdataarray"></a><span data-ttu-id="5d081-103">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="5d081-103">AttendeeConflictDataArray</span></span>

<span data-ttu-id="5d081-104">Das **AttendeeConflictDataArray** -Element enthält ein Array von Conflict-Daten für die abgefragte Teilnehmer bei der [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d081-104">The **AttendeeConflictDataArray** element contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>
  
- [<span data-ttu-id="5d081-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5d081-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="5d081-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="5d081-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
- [<span data-ttu-id="5d081-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="5d081-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
- [<span data-ttu-id="5d081-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="5d081-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
- [<span data-ttu-id="5d081-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="5d081-109">SuggestionArray</span></span>](suggestionarray.md)
  
- [<span data-ttu-id="5d081-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="5d081-110">Suggestion</span></span>](suggestion.md)
  
- [<span data-ttu-id="5d081-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="5d081-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 <span data-ttu-id="5d081-112">**ArrayOfAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="5d081-112">**ArrayOfAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5d081-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5d081-113">Attributes and elements</span></span>

<span data-ttu-id="5d081-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5d081-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5d081-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="5d081-115">Attributes</span></span>

<span data-ttu-id="5d081-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="5d081-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5d081-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5d081-117">Child elements</span></span>

|<span data-ttu-id="5d081-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="5d081-118">**Element**</span></span>|<span data-ttu-id="5d081-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5d081-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d081-120">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="5d081-120">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md) <br/> |<span data-ttu-id="5d081-121">Stellt einen Teilnehmer nicht aufgelöst werden oder einen Teilnehmer, der nicht auf einen Benutzer, der Verteilerliste oder der Kontakt ist dar.</span><span class="sxs-lookup"><span data-stu-id="5d081-121">Represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span>  <br/> |
|[<span data-ttu-id="5d081-122">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="5d081-122">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="5d081-123">Enthält eines Benutzers oder Kontakts Frei/Gebucht-Status für ein Time-Fenster, das zur selben Zeit als die vorgeschlagenen auftritt, Besprechungszeit im [Vorschlag](suggestion.md) -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d081-123">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span>  <br/> |
|[<span data-ttu-id="5d081-124">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="5d081-124">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md) <br/> |<span data-ttu-id="5d081-125">Stellt einen Teilnehmer, die als Verteilerliste aufgelöst, die aufgrund ihrer Größe erweitern.</span><span class="sxs-lookup"><span data-stu-id="5d081-125">Represents an attendee that resolved as a distribution list that was too large to expand.</span></span>  <br/> |
|[<span data-ttu-id="5d081-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="5d081-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="5d081-127">Enthält Konfliktinformationen über die Anzahl von Benutzern zur Verfügung, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die nicht zu Ihrer Verfügbarkeit einsehen in einer Verteilerliste für eine vorgeschlagene Besprechungszeit verfügen aggregierte.</span><span class="sxs-lookup"><span data-stu-id="5d081-127">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5d081-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5d081-128">Parent elements</span></span>

|<span data-ttu-id="5d081-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="5d081-129">**Element**</span></span>|<span data-ttu-id="5d081-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5d081-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5d081-131">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="5d081-131">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="5d081-132">Stellt ein einzelnes meeting Zeit Vorschlag.</span><span class="sxs-lookup"><span data-stu-id="5d081-132">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="5d081-133">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="5d081-133">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5d081-134">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5d081-134">Remarks</span></span>

<span data-ttu-id="5d081-135">Die Position jedes Elements in der **AttendeeConflictDataArray** entspricht der Position der abgefragten Teilnehmer im [MailboxDataArray](mailboxdataarray.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="5d081-135">The position of each element in the **AttendeeConflictDataArray** corresponds to the position of the queried attendees in the [MailboxDataArray](mailboxdataarray.md) element.</span></span> <span data-ttu-id="5d081-136">Jeden abgefragte Teilnehmer muss eines der untergeordneten Elemente **AttendeeConflictDataArray** entsprechen.</span><span class="sxs-lookup"><span data-stu-id="5d081-136">Each queried attendee must correspond to one of the **AttendeeConflictDataArray** child elements.</span></span> <span data-ttu-id="5d081-137">Diese Elemente darstellen einen einzelnen Konflikt mit der vorgeschlagenen Besprechungszeit im [Vorschlag](suggestion.md) -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5d081-137">These elements represent a single conflict with the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="5d081-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5d081-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5d081-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5d081-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5d081-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5d081-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5d081-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5d081-141">Schema Name</span></span>  <br/> |<span data-ttu-id="5d081-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5d081-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="5d081-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5d081-143">Validation File</span></span>  <br/> |<span data-ttu-id="5d081-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5d081-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5d081-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5d081-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="5d081-146">False</span><span class="sxs-lookup"><span data-stu-id="5d081-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5d081-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5d081-147">See also</span></span>

- [<span data-ttu-id="5d081-148">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5d081-148">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="5d081-149">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5d081-149">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="5d081-150">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="5d081-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

