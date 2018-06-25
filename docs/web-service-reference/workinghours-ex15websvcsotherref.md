---
title: WorkingHours
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingHours
api_type:
- schema
ms.assetid: bbe97777-f728-46c5-b2aa-565112c24f3a
description: Das WorkingHours-Element darstellt, die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.
ms.openlocfilehash: c53779422b87adebed370a1ed88e4e91c7a2dcaf
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839544"
---
# <a name="workinghours"></a><span data-ttu-id="db002-103">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="db002-103">WorkingHours</span></span>

<span data-ttu-id="db002-104">Das **WorkingHours** -Element darstellt, die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="db002-104">The **WorkingHours** element represents the time zone settings and working hours for the requested mailbox user.</span></span> 
  
[<span data-ttu-id="db002-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="db002-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="db002-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="db002-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="db002-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="db002-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="db002-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="db002-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="db002-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="db002-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
```xml
<WorkingHours>
   <TimeZone>...</TimeZone>
   <WorkingPeriodArray>...</WorkingPeriodArray>
</WorkingHours>
```

 <span data-ttu-id="db002-110">**WorkingHours**</span><span class="sxs-lookup"><span data-stu-id="db002-110">**WorkingHours**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="db002-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="db002-111">Attributes and elements</span></span>

<span data-ttu-id="db002-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="db002-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="db002-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="db002-113">Attributes</span></span>

<span data-ttu-id="db002-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="db002-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="db002-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db002-115">Child elements</span></span>

|<span data-ttu-id="db002-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="db002-116">**Element**</span></span>|<span data-ttu-id="db002-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db002-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db002-118">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="db002-118">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="db002-119">Enthält Elemente, die Informationen zur Zeitzone zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="db002-119">Contains elements that identify time zone information.</span></span> <span data-ttu-id="db002-120">Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="db002-120">This element also contains information about the transition between standard time and daylight saving time.</span></span> <span data-ttu-id="db002-121">Dieses Element ist erforderlich, wenn das **WorkingHours** -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db002-121">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
|[<span data-ttu-id="db002-122">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="db002-122">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="db002-123">Enthält Informationen zu Perioden für den Postfachbenutzer arbeiten.</span><span class="sxs-lookup"><span data-stu-id="db002-123">Contains working period information for the mailbox user.</span></span> <span data-ttu-id="db002-124">Dieses Element ist erforderlich, wenn das **WorkingHours** -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="db002-124">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="db002-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="db002-125">Parent elements</span></span>

|<span data-ttu-id="db002-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="db002-126">**Element**</span></span>|<span data-ttu-id="db002-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="db002-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="db002-128">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="db002-128">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="db002-129">Enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="db002-129">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="db002-130">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="db002-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="db002-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="db002-131">Remarks</span></span>

<span data-ttu-id="db002-132">All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen.</span><span class="sxs-lookup"><span data-stu-id="db002-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="db002-133">Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="db002-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="db002-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="db002-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="db002-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="db002-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="db002-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="db002-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="db002-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="db002-137">Schema Name</span></span>  <br/> |<span data-ttu-id="db002-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="db002-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="db002-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="db002-139">Validation File</span></span>  <br/> |<span data-ttu-id="db002-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="db002-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="db002-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="db002-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="db002-142">False</span><span class="sxs-lookup"><span data-stu-id="db002-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="db002-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="db002-143">See also</span></span>



[<span data-ttu-id="db002-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="db002-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="db002-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="db002-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="db002-146">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="db002-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

