---
title: GroupAttendeeConflictData
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- GroupAttendeeConflictData
api_type:
- schema
ms.assetid: fd8bf19a-298b-4135-93e8-ead3db7e1142
description: Das GroupAttendeeConflictData-Element enthält aggregierte Konfliktinformationen über die Anzahl der Benutzer, die verfügbar sind, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die keine Informationen zur Verfügbarkeit in einer Verteilerliste für auf ein Vorgeschlagene Besprechungszeit.
ms.openlocfilehash: 382b4d866c95de98bd444cd6226d71813889d4f4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19829757"
---
# <a name="groupattendeeconflictdata"></a><span data-ttu-id="1d2b4-103">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="1d2b4-103">GroupAttendeeConflictData</span></span>

<span data-ttu-id="1d2b4-104">Das **GroupAttendeeConflictData** -Element enthält aggregierte Konfliktinformationen über die Anzahl der Benutzer, die verfügbar sind, die Anzahl der Benutzer, die Konflikte und die Anzahl der Benutzer, die keine Informationen zur Verfügbarkeit in einer Verteilerliste für einen Zeitraum vorgeschlagenen Besprechung.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-104">The **GroupAttendeeConflictData** element contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span> 
  
- [<span data-ttu-id="1d2b4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1d2b4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="1d2b4-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="1d2b4-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
- [<span data-ttu-id="1d2b4-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="1d2b4-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
- [<span data-ttu-id="1d2b4-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="1d2b4-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
- [<span data-ttu-id="1d2b4-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="1d2b4-109">SuggestionArray</span></span>](suggestionarray.md)
- [<span data-ttu-id="1d2b4-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="1d2b4-110">Suggestion</span></span>](suggestion.md)
- [<span data-ttu-id="1d2b4-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="1d2b4-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
- [<span data-ttu-id="1d2b4-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="1d2b4-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

<span data-ttu-id="1d2b4-113">**GroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="1d2b4-113">**GroupAttendeeConflictData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1d2b4-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1d2b4-114">Attributes and elements</span></span>

<span data-ttu-id="1d2b4-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1d2b4-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="1d2b4-116">Attributes</span></span>

<span data-ttu-id="1d2b4-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1d2b4-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d2b4-118">Child elements</span></span>

|<span data-ttu-id="1d2b4-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d2b4-119">**Element**</span></span>|<span data-ttu-id="1d2b4-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d2b4-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d2b4-121">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="1d2b4-121">NumberOfMembers</span></span>](numberofmembers.md) <br/> |<span data-ttu-id="1d2b4-122">Die Anzahl von Benutzern, Ressourcen und Chatrooms in einer Verteilerliste darstellt.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-122">Represents the number of users, resources, and rooms in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="1d2b4-123">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="1d2b4-123">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md) <br/> |<span data-ttu-id="1d2b4-124">Stellt die Anzahl der Mitglieder der Verteilerliste, die für einen Zeitraum vorgeschlagenen Besprechung zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-124">Represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="1d2b4-125">Dieses Element stellt Member für die der Status **frei**ist.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-125">This element represents members for whom the status is **Free**.</span></span>  <br/> |
|[<span data-ttu-id="1d2b4-126">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="1d2b4-126">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md) <br/> |<span data-ttu-id="1d2b4-127">Stellt die Anzahl der Mitglieder der Verteilerliste, die einen Konflikt mit einer vorgeschlagenen Besprechungszeit haben.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-127">Represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="1d2b4-128">Dieses Element stellt Mitglieder, die den Status **beschäftigt**, **ABWESEND**oder **mit Vorbehalt** aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-128">This element represents members who have a **Busy**, **OOF**, or **Tentative** status.</span></span>  <br/> |
|[<span data-ttu-id="1d2b4-129">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="1d2b4-129">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md) <br/> |<span data-ttu-id="1d2b4-130">Stellt die Anzahl der Mitglieder, die nicht veröffentlichte Frei/Gebucht-Daten mit einer vorgeschlagenen Besprechung Uhrzeit verglichen verfügen.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-130">Represents the number of group members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="1d2b4-131">Dieses Element stellt die Mitglieder von Verteilerlisten, die zu groß ist oder Mitglieder, die **Keine Daten** Status aufweisen.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-131">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1d2b4-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1d2b4-132">Parent elements</span></span>

|<span data-ttu-id="1d2b4-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="1d2b4-133">**Element**</span></span>|<span data-ttu-id="1d2b4-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1d2b4-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1d2b4-135">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="1d2b4-135">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="1d2b4-136">Enthält ein Array von Conflict-Daten für die abgefragte Teilnehmer bei der [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-136">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="1d2b4-137">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1d2b4-137">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1d2b4-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1d2b4-138">Remarks</span></span>

<span data-ttu-id="1d2b4-139">Das **GroupAttendeeConflictData** -Element wird in der Antwort vorhanden ist, wenn ein Teilnehmer in der [GetUserAvailabilityRequest](getuseravailabilityrequest.md) in einer Verteilerliste aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-139">The **GroupAttendeeConflictData** element is present in the response when an attendee in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) is resolved to a distribution list.</span></span> <span data-ttu-id="1d2b4-140">Das **GroupAttendeeConflictData** -Element identifiziert drei Zustände für Mitglieder von Verteilerlisten: verfügbar, Konflikt, oder keine Daten.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-140">The **GroupAttendeeConflictData** element identifies three states for members of a distribution list: available, conflicted, or no data.</span></span> <span data-ttu-id="1d2b4-141">Verteilerlistenerweiterung unterstützt bis zu 100 Elemente.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-141">Distribution list expansion will support up to 100 members.</span></span> <span data-ttu-id="1d2b4-142">Aus diesem Grund kann das [NumberOfMembers](numberofmembers.md) -Element ein Maximum von bis zu 100 Mitgliedern enthalten.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-142">Therefore, the [NumberOfMembers](numberofmembers.md) element can contain a maximum of 100 members.</span></span> <span data-ttu-id="1d2b4-143">Die Erweiterung der Verteilerliste ist rekursiv.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-143">Distribution list expansion is recursive.</span></span> <span data-ttu-id="1d2b4-144">Wenn eine Verteilerliste eine Verteilerliste untergeordneten enthält, die das mehr als 100 Mitgliedern die Mitgliedschaft insgesamt übergeordneten erweitert, die untergeordneten Verteilerliste nicht erweitert werden und wird als nur ein Eintrag für die Anzahl der [NumberOfMembersWithNoData](numberofmemberswithnodata.md) zählen.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-144">If a distribution list contains a child distribution list that expands the total parent membership to over 100 members, the child distribution list will not be expanded and will count as a single entry of the [NumberOfMembersWithNoData](numberofmemberswithnodata.md) element count.</span></span> <span data-ttu-id="1d2b4-145">Wenn eine Verteilerliste untergeordneten erweitert werden kann und die gesamte übergeordnete Mitgliedschaft wird nicht mehr als 100 Mitgliedern erweitert, deren Mitgliedschaft wird erweitert, und die untergeordneten Elemente des Elements **GroupAttendeeConflictData** die Elementanzahl hinzugefügt werden.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-145">If a child distribution list can be expanded and the total parent membership does not expand to over 100 members, its membership is expanded and the member counts are added to the child elements of the **GroupAttendeeConflictData** element.</span></span> 
  
<span data-ttu-id="1d2b4-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1d2b4-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1d2b4-147">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1d2b4-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1d2b4-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="1d2b4-148">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1d2b4-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1d2b4-149">Schema Name</span></span>  <br/> |<span data-ttu-id="1d2b4-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1d2b4-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="1d2b4-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1d2b4-151">Validation File</span></span>  <br/> |<span data-ttu-id="1d2b4-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1d2b4-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1d2b4-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1d2b4-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="1d2b4-154">False</span><span class="sxs-lookup"><span data-stu-id="1d2b4-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d2b4-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1d2b4-155">See also</span></span>

- [<span data-ttu-id="1d2b4-156">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1d2b4-156">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="1d2b4-157">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1d2b4-157">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="1d2b4-158">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="1d2b4-158">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

