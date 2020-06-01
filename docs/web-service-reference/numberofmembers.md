---
title: NumberOfMembers
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberOfMembers
api_type:
- schema
ms.assetid: 845fb877-de49-4e26-8885-6f026edd9ee9
description: Das NumberOfMembers-Element stellt die Anzahl der Benutzer, Ressourcen und Räume in einer Verteilerliste dar.
ms.openlocfilehash: c91087f42d806afb0a0d3d607cc84f14a1a6c1b0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462598"
---
# <a name="numberofmembers"></a><span data-ttu-id="fefdb-103">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="fefdb-103">NumberOfMembers</span></span>

<span data-ttu-id="fefdb-104">Das **NumberOfMembers** -Element stellt die Anzahl der Benutzer, Ressourcen und Räume in einer Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="fefdb-104">The **NumberOfMembers** element represents the number of users, resources, and rooms in a distribution list.</span></span> 
  
[<span data-ttu-id="fefdb-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fefdb-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="fefdb-106">SuggestionsResponse</span><span class="sxs-lookup"><span data-stu-id="fefdb-106">SuggestionsResponse</span></span>](suggestionsresponse.md)
  
[<span data-ttu-id="fefdb-107">SuggestionDayResultArray</span><span class="sxs-lookup"><span data-stu-id="fefdb-107">SuggestionDayResultArray</span></span>](suggestiondayresultarray.md)
  
[<span data-ttu-id="fefdb-108">SuggestionDayResult</span><span class="sxs-lookup"><span data-stu-id="fefdb-108">SuggestionDayResult</span></span>](suggestiondayresult.md)
  
[<span data-ttu-id="fefdb-109">SuggestionArray</span><span class="sxs-lookup"><span data-stu-id="fefdb-109">SuggestionArray</span></span>](suggestionarray.md)
  
[<span data-ttu-id="fefdb-110">Vorschlag</span><span class="sxs-lookup"><span data-stu-id="fefdb-110">Suggestion</span></span>](suggestion.md)
  
[<span data-ttu-id="fefdb-111">AttendeeConflictDataArray</span><span class="sxs-lookup"><span data-stu-id="fefdb-111">AttendeeConflictDataArray</span></span>](attendeeconflictdataarray.md)
  
[<span data-ttu-id="fefdb-112">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="fefdb-112">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md)
  
[<span data-ttu-id="fefdb-113">NumberOfMembers</span><span class="sxs-lookup"><span data-stu-id="fefdb-113">NumberOfMembers</span></span>](numberofmembers.md)
  
```xml
<NumberOfMembers>...</NumberOfMembers>
```

 <span data-ttu-id="fefdb-114">**int**</span><span class="sxs-lookup"><span data-stu-id="fefdb-114">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fefdb-115">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fefdb-115">Attributes and elements</span></span>

<span data-ttu-id="fefdb-116">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fefdb-116">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fefdb-117">Attribute</span><span class="sxs-lookup"><span data-stu-id="fefdb-117">Attributes</span></span>

<span data-ttu-id="fefdb-118">Keine.</span><span class="sxs-lookup"><span data-stu-id="fefdb-118">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fefdb-119">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fefdb-119">Child elements</span></span>

<span data-ttu-id="fefdb-120">Keine.</span><span class="sxs-lookup"><span data-stu-id="fefdb-120">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="fefdb-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fefdb-121">Parent elements</span></span>

|<span data-ttu-id="fefdb-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="fefdb-122">**Element**</span></span>|<span data-ttu-id="fefdb-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fefdb-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fefdb-124">GroupAttendeeConflictData</span><span class="sxs-lookup"><span data-stu-id="fefdb-124">GroupAttendeeConflictData</span></span>](groupattendeeconflictdata.md) <br/> |<span data-ttu-id="fefdb-125">Enthält aggregierte Konfliktinformationen über die Anzahl der verfügbaren Benutzer, die Anzahl der Benutzer mit Konflikten sowie die Anzahl der Benutzer, die in einer Verteilerliste keine Verfügbarkeitsinformationen für eine vorgeschlagene Besprechungszeit haben.</span><span class="sxs-lookup"><span data-stu-id="fefdb-125">Contains aggregate conflict information about the number of users available, the number of users who have conflicts, and the number of users who do not have availability information in a distribution list for a suggested meeting time.</span></span>  <br/> <span data-ttu-id="fefdb-126">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="fefdb-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/SuggestionsResponse/SuggestionDayResultArray/SuggestionDayResult[i]/SuggestionArray/Suggestion[i]/AttendeeConflictDataArray/GroupAttendeeConflictData` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fefdb-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fefdb-127">Remarks</span></span>

<span data-ttu-id="fefdb-128">Der maximale Wert des **NumberOfMembers** -Elements ist 100.</span><span class="sxs-lookup"><span data-stu-id="fefdb-128">The maximum value of the **NumberOfMembers** element is 100.</span></span> 
  
<span data-ttu-id="fefdb-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fefdb-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fefdb-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fefdb-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fefdb-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="fefdb-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fefdb-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fefdb-132">Schema Name</span></span>  <br/> |<span data-ttu-id="fefdb-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fefdb-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="fefdb-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fefdb-134">Validation File</span></span>  <br/> |<span data-ttu-id="fefdb-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fefdb-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fefdb-136">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fefdb-136">Can be Empty</span></span>  <br/> |<span data-ttu-id="fefdb-137">False</span><span class="sxs-lookup"><span data-stu-id="fefdb-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fefdb-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fefdb-138">See also</span></span>



[<span data-ttu-id="fefdb-139">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fefdb-139">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fefdb-140">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fefdb-140">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="fefdb-141">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="fefdb-141">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

