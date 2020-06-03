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
description: Das AttendeeConflictDataArray-Element enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im GetUserAvailability-Vorgang identifiziert wurden.
ms.openlocfilehash: 770e8c00ca248ec3562180dc9d3626fd5b58f4d9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455800"
---
# <a name="attendeeconflictdataarray"></a><span data-ttu-id="46e76-103">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="46e76-103">AttendeeConflictDataArray</span></span>

<span data-ttu-id="46e76-104">Das **AttendeeConflictDataArray** -Element enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="46e76-104">The **AttendeeConflictDataArray** element contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>
  
- [<span data-ttu-id="46e76-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="46e76-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="46e76-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="46e76-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
- [<span data-ttu-id="46e76-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="46e76-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
- [<span data-ttu-id="46e76-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="46e76-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
- [<span data-ttu-id="46e76-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="46e76-109">SuggestionArray</span></span>](suggestionarray.md)
  
- [<span data-ttu-id="46e76-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="46e76-110">Suggestion</span></span>](suggestion.md)
  
- [<span data-ttu-id="46e76-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="46e76-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
```xml
<ArrayOfAttendeeConflictData>
   <UnknownAttendeeConflictData>...</UnknownAttendeeConflictData>
   <IndividualAttendeeConflictData>...</IndividualAttendeeConflictData>
   <TooBigGroupAttendeeConflictData>...</TooBigGroupAttendeeConflictData>
   <GroupAttendeeConflictData>...</GroupAttendeeConflictData>
</ArrayOfAttendeeConflictData>
```

 <span data-ttu-id="46e76-112">**ArrayOfAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="46e76-112">**ArrayOfAttendeeConflictData**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46e76-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="46e76-113">Attributes and elements</span></span>

<span data-ttu-id="46e76-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="46e76-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46e76-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="46e76-115">Attributes</span></span>

<span data-ttu-id="46e76-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="46e76-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46e76-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46e76-117">Child elements</span></span>

|<span data-ttu-id="46e76-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="46e76-118">**Element**</span></span>|<span data-ttu-id="46e76-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46e76-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46e76-120">UnknownAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="46e76-120">UnknownAttendeeConflictData</span></span>](unknownattendeeconflictdata.md) <br/> |<span data-ttu-id="46e76-121">Stellt einen nicht auflösbaren Teilnehmer oder Teilnehmer dar, der kein Benutzer, eine Verteilerliste oder ein Kontakt ist.</span><span class="sxs-lookup"><span data-stu-id="46e76-121">Represents an unresolvable attendee or an attendee that is not a user, distribution list, or contact.</span></span>  <br/> |
|[<span data-ttu-id="46e76-122">IndividualAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="46e76-122">IndividualAttendeeConflictData</span></span>](individualattendeeconflictdata.md) <br/> |<span data-ttu-id="46e76-123">Enthält den Frei/Gebucht-Status eines Benutzers oder Kontakts für ein Zeitfenster, das gleichzeitig mit der im [Suggestion](suggestion.md) -Element identifizierten vorgeschlagenen Besprechungszeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="46e76-123">Contains a user's or contact's free/busy status for a time window that occurs at the same time as the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span>  <br/> |
|[<span data-ttu-id="46e76-124">TooBigGroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="46e76-124">TooBigGroupAttendeeConflictData</span></span>](toobiggroupattendeeconflictdata.md) <br/> |<span data-ttu-id="46e76-125">Stellt einen Teilnehmer dar, der als Verteilerliste aufgelöst wurde, der zu groß für die Erweiterung war.</span><span class="sxs-lookup"><span data-stu-id="46e76-125">Represents an attendee that resolved as a distribution list that was too large to expand.</span></span>  <br/> |
|[<span data-ttu-id="46e76-126">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="46e76-126">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="46e76-127">Enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer mit Konflikten sowie die Anzahl der Benutzer, die in einer Verteilerliste keine Verfügbarkeitsinformationen für eine vorgeschlagene Besprechungszeit haben.</span><span class="sxs-lookup"><span data-stu-id="46e76-127">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46e76-128">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46e76-128">Parent elements</span></span>

|<span data-ttu-id="46e76-129">**Element**</span><span class="sxs-lookup"><span data-stu-id="46e76-129">**Element**</span></span>|<span data-ttu-id="46e76-130">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46e76-130">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46e76-131">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="46e76-131">Suggestion</span></span>](suggestion.md) <br/> |<span data-ttu-id="46e76-132">Stellt einen einzelnen Besprechungszeit Vorschlag dar.</span><span class="sxs-lookup"><span data-stu-id="46e76-132">Represents a single meeting time suggestion.</span></span>  <br/> <span data-ttu-id="46e76-133">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="46e76-133">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46e76-134">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46e76-134">Remarks</span></span>

<span data-ttu-id="46e76-135">Die Position der einzelnen Elemente in der **AttendeeConflictDataArray** entspricht der Position der abgefragten Teilnehmer im [MailboxDataArray](mailboxdataarray.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="46e76-135">The position of each element in the **AttendeeConflictDataArray** corresponds to the position of the queried attendees in the [MailboxDataArray](mailboxdataarray.md) element.</span></span> <span data-ttu-id="46e76-136">Jeder abgefragte Teilnehmer muss einem der untergeordneten **AttendeeConflictDataArray** -Elemente entsprechen.</span><span class="sxs-lookup"><span data-stu-id="46e76-136">Each queried attendee must correspond to one of the **AttendeeConflictDataArray** child elements.</span></span> <span data-ttu-id="46e76-137">Diese Elemente stellen einen einzelnen Konflikt mit der vorgeschlagenen Besprechungszeit dar, die im [Suggestion](suggestion.md) -Element angegeben ist.</span><span class="sxs-lookup"><span data-stu-id="46e76-137">These elements represent a single conflict with the suggested meeting time identified in the [Suggestion](suggestion.md) element.</span></span> 
  
<span data-ttu-id="46e76-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="46e76-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="46e76-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="46e76-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46e76-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="46e76-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46e76-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="46e76-141">Schema Name</span></span>  <br/> |<span data-ttu-id="46e76-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="46e76-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="46e76-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="46e76-143">Validation File</span></span>  <br/> |<span data-ttu-id="46e76-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="46e76-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46e76-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="46e76-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="46e76-146">False</span><span class="sxs-lookup"><span data-stu-id="46e76-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46e76-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46e76-147">See also</span></span>

- [<span data-ttu-id="46e76-148">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="46e76-148">GetUserAvailability operation</span></span>](getuseravailability-operation.md) 
- [<span data-ttu-id="46e76-149">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="46e76-149">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="46e76-150">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="46e76-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

