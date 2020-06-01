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
description: Das GroupAttendeeConflictData-Element enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer mit Konflikten sowie die Anzahl der Benutzer, die in einer Verteilerliste keine Verfügbarkeitsinformationen für eine vorgeschlagene Besprechungszeit haben.
ms.openlocfilehash: c75a4e6f8fdff7fb2514f448350fee9f1acb9775
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462929"
---
# <a name="groupattendeeconflictdata"></a><span data-ttu-id="f1d8e-103">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f1d8e-103">GroupAttendeeConflictData</span></span>

<span data-ttu-id="f1d8e-104">Das **GroupAttendeeConflictData** -Element enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer mit Konflikten sowie die Anzahl der Benutzer, die in einer Verteilerliste keine Verfügbarkeitsinformationen für eine vorgeschlagene Besprechungszeit haben.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-104">The **GroupAttendeeConflictData** element contains aggregate conflict information about the number of users who are available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span> 
  
- [<span data-ttu-id="f1d8e-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f1d8e-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="f1d8e-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="f1d8e-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
- [<span data-ttu-id="f1d8e-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="f1d8e-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
- [<span data-ttu-id="f1d8e-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="f1d8e-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
- [<span data-ttu-id="f1d8e-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="f1d8e-109">SuggestionArray</span></span>](suggestionarray.md)
- [<span data-ttu-id="f1d8e-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="f1d8e-110">Suggestion</span></span>](suggestion.md)
- [<span data-ttu-id="f1d8e-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f1d8e-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
- [<span data-ttu-id="f1d8e-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="f1d8e-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
```xml
<GroupAttendeeConflictData>
   <NumberOfMembers>...</NumberOfMembers>
   <NumberOfMembersAvailable>...</NumberOfMembersAvailable>
   <NumberOfMembersWithConflict>...</NumberOfMembersWithConflict>
   <NumberOfMembersWithNoData>...</NumberOfMembersWithNoData>
</GroupAttendeeConflictData>
```

<span data-ttu-id="f1d8e-113">**GroupAttendeeConflictData**</span><span class="sxs-lookup"><span data-stu-id="f1d8e-113">**GroupAttendeeConflictData**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f1d8e-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f1d8e-114">Attributes and elements</span></span>

<span data-ttu-id="f1d8e-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f1d8e-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="f1d8e-116">Attributes</span></span>

<span data-ttu-id="f1d8e-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f1d8e-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1d8e-118">Child elements</span></span>

|<span data-ttu-id="f1d8e-119">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1d8e-119">**Element**</span></span>|<span data-ttu-id="f1d8e-120">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1d8e-120">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1d8e-121">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="f1d8e-121">NumberOfMembers</span></span>](numberofmembers.md) <br/> |<span data-ttu-id="f1d8e-122">Stellt die Anzahl der Benutzer, Ressourcen und Räume in einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-122">Represents the number of users, resources, and rooms in a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="f1d8e-123">NumberOfMembersAvailable</span><span class="sxs-lookup"><span data-stu-id="f1d8e-123">NumberOfMembersAvailable</span></span>](numberofmembersavailable.md) <br/> |<span data-ttu-id="f1d8e-124">Stellt die Anzahl der Verteilerlistenmitglieder dar, die für eine vorgeschlagene Besprechungszeit zur Verfügung stehen.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-124">Represents the number of distribution list members who are available for a suggested meeting time.</span></span> <span data-ttu-id="f1d8e-125">Dieses Element stellt Elemente dar, für die der Status **frei**ist.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-125">This element represents members for whom the status is **Free**.</span></span>  <br/> |
|[<span data-ttu-id="f1d8e-126">NumberOfMembersWithConflict</span><span class="sxs-lookup"><span data-stu-id="f1d8e-126">NumberOfMembersWithConflict</span></span>](numberofmemberswithconflict.md) <br/> |<span data-ttu-id="f1d8e-127">Gibt die Anzahl der Verteilerlistenmitglieder an, die einen Konflikt mit einer vorgeschlagenen Besprechungszeit haben.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-127">Represents the number of distribution list members who have a conflict with a suggested meeting time.</span></span> <span data-ttu-id="f1d8e-128">Dieses Element stellt Elemente dar, die den Status " **beschäftigt**", " **Abwesend**" oder " **vorläufig** " aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-128">This element represents members who have a **Busy**, **OOF**, or **Tentative** status.</span></span>  <br/> |
|[<span data-ttu-id="f1d8e-129">NumberOfMembersWithNoData</span><span class="sxs-lookup"><span data-stu-id="f1d8e-129">NumberOfMembersWithNoData</span></span>](numberofmemberswithnodata.md) <br/> |<span data-ttu-id="f1d8e-130">Gibt die Anzahl der Gruppenmitglieder an, die keine Frei/Gebucht-Daten veröffentlicht haben, die mit einer vorgeschlagenen Besprechungszeit verglichen werden sollen.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-130">Represents the number of group members who do not have published free/busy data to compare to a suggested meeting time.</span></span> <span data-ttu-id="f1d8e-131">Dieses Element stellt Elemente einer Verteilerliste dar, die zu groß sind, oder Mitglieder, die **keinen Daten** Status aufweisen.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-131">This element represents members of a distribution list that is too large or members who have **No Data** status.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f1d8e-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f1d8e-132">Parent elements</span></span>

|<span data-ttu-id="f1d8e-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="f1d8e-133">**Element**</span></span>|<span data-ttu-id="f1d8e-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f1d8e-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f1d8e-135">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="f1d8e-135">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md) <br/> |<span data-ttu-id="f1d8e-136">Enthält ein Array von Konfliktdaten für abgefragte Teilnehmer, die im [GetUserAvailability-Vorgang](getuseravailability-operation.md)identifiziert wurden.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-136">Contains an array of conflict data for queried attendees identified in the [GetUserAvailability operation](getuseravailability-operation.md).</span></span>  <br/> <span data-ttu-id="f1d8e-137">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="f1d8e-137">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f1d8e-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f1d8e-138">Remarks</span></span>

<span data-ttu-id="f1d8e-139">Das **GroupAttendeeConflictData** -Element ist in der Antwort vorhanden, wenn ein Teilnehmer im [GetUserAvailabilityRequest](getuseravailabilityrequest.md) in eine Verteilerliste aufgelöst wird.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-139">The **GroupAttendeeConflictData** element is present in the response when an attendee in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) is resolved to a distribution list.</span></span> <span data-ttu-id="f1d8e-140">Das **GroupAttendeeConflictData** -Element identifiziert drei Zustände für Mitglieder einer Verteilerliste: verfügbar, widersprüchlich oder keine Daten.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-140">The **GroupAttendeeConflictData** element identifies three states for members of a distribution list: available, conflicted, or no data.</span></span> <span data-ttu-id="f1d8e-141">Die Erweiterung für Verteilerlisten unterstützt bis zu 100 Mitglieder.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-141">Distribution list expansion will support up to 100 members.</span></span> <span data-ttu-id="f1d8e-142">Das [NumberOfMembers](numberofmembers.md) -Element kann daher maximal 100 Mitglieder enthalten.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-142">Therefore, the [NumberOfMembers](numberofmembers.md) element can contain a maximum of 100 members.</span></span> <span data-ttu-id="f1d8e-143">Die Erweiterung der Verteilerliste ist rekursiv.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-143">Distribution list expansion is recursive.</span></span> <span data-ttu-id="f1d8e-144">Wenn eine Verteilerliste eine untergeordnete Verteilerliste enthält, die die gesamte übergeordnete Mitgliedschaft auf über 100 Mitglieder erweitert, wird die untergeordnete Verteilerliste nicht erweitert und wird als ein einzelner Eintrag der [NumberOfMembersWithNoData](numberofmemberswithnodata.md) -Elementanzahl gezählt.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-144">If a distribution list contains a child distribution list that expands the total parent membership to over 100 members, the child distribution list will not be expanded and will count as a single entry of the [NumberOfMembersWithNoData](numberofmemberswithnodata.md) element count.</span></span> <span data-ttu-id="f1d8e-145">Wenn eine untergeordnete Verteilerliste erweitert werden kann und die gesamte übergeordnete Mitgliedschaft nicht auf mehr als 100 Mitglieder erweitert wird, wird die Mitgliedschaft erweitert, und die Mitgliederanzahl wird den untergeordneten Elementen des **GroupAttendeeConflictData** -Elements hinzugefügt.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-145">If a child distribution list can be expanded and the total parent membership does not expand to over 100 members, its membership is expanded and the member counts are added to the child elements of the **GroupAttendeeConflictData** element.</span></span> 
  
<span data-ttu-id="f1d8e-146">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f1d8e-146">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f1d8e-147">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f1d8e-147">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f1d8e-148">Namespace</span><span class="sxs-lookup"><span data-stu-id="f1d8e-148">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f1d8e-149">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f1d8e-149">Schema Name</span></span>  <br/> |<span data-ttu-id="f1d8e-150">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f1d8e-150">Types schema</span></span>  <br/> |
|<span data-ttu-id="f1d8e-151">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f1d8e-151">Validation File</span></span>  <br/> |<span data-ttu-id="f1d8e-152">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f1d8e-152">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f1d8e-153">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f1d8e-153">Can be Empty</span></span>  <br/> |<span data-ttu-id="f1d8e-154">False</span><span class="sxs-lookup"><span data-stu-id="f1d8e-154">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f1d8e-155">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f1d8e-155">See also</span></span>

- [<span data-ttu-id="f1d8e-156">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f1d8e-156">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="f1d8e-157">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="f1d8e-157">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="f1d8e-158">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="f1d8e-158">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

