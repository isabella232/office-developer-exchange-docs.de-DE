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
description: Das WorkingHours-Element stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.
ms.openlocfilehash: 9cb21e72f7024b96b4b5f252a8a3b85bb704e67c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44468341"
---
# <a name="workinghours"></a><span data-ttu-id="fd75c-103">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="fd75c-103">WorkingHours</span></span>

<span data-ttu-id="fd75c-104">Das **WorkingHours** -Element stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="fd75c-104">The **WorkingHours** element represents the time zone settings and working hours for the requested mailbox user.</span></span> 
  
[<span data-ttu-id="fd75c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fd75c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="fd75c-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="fd75c-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="fd75c-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="fd75c-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="fd75c-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="fd75c-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="fd75c-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="fd75c-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
```xml
<WorkingHours>
   <TimeZone>...</TimeZone>
   <WorkingPeriodArray>...</WorkingPeriodArray>
</WorkingHours>
```

 <span data-ttu-id="fd75c-110">**WorkingHours**</span><span class="sxs-lookup"><span data-stu-id="fd75c-110">**WorkingHours**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fd75c-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fd75c-111">Attributes and elements</span></span>

<span data-ttu-id="fd75c-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fd75c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fd75c-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="fd75c-113">Attributes</span></span>

<span data-ttu-id="fd75c-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="fd75c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fd75c-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd75c-115">Child elements</span></span>

|<span data-ttu-id="fd75c-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd75c-116">**Element**</span></span>|<span data-ttu-id="fd75c-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd75c-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd75c-118">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="fd75c-118">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> |<span data-ttu-id="fd75c-119">Enthält Elemente, die Zeitzoneninformationen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="fd75c-119">Contains elements that identify time zone information.</span></span> <span data-ttu-id="fd75c-120">Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="fd75c-120">This element also contains information about the transition between standard time and daylight saving time.</span></span> <span data-ttu-id="fd75c-121">Dieses Element ist erforderlich, wenn das **WorkingHours** -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd75c-121">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
|[<span data-ttu-id="fd75c-122">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="fd75c-122">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="fd75c-123">Enthält Informationen zum Arbeitszeitraum für den Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="fd75c-123">Contains working period information for the mailbox user.</span></span> <span data-ttu-id="fd75c-124">Dieses Element ist erforderlich, wenn das **WorkingHours** -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="fd75c-124">This element is required if the **WorkingHours** element is used.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fd75c-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fd75c-125">Parent elements</span></span>

|<span data-ttu-id="fd75c-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="fd75c-126">**Element**</span></span>|<span data-ttu-id="fd75c-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fd75c-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fd75c-128">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="fd75c-128">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="fd75c-129">Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fd75c-129">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="fd75c-130">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="fd75c-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fd75c-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="fd75c-131">Remarks</span></span>

<span data-ttu-id="fd75c-132">Alle untergeordneten Elemente werden in der Reihenfolge aufgeführt, in der Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="fd75c-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="fd75c-133">Die von diesem Element bereitgestellte Detailebene hängt von den Berechtigungen ab, die dem Requestor erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="fd75c-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="fd75c-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fd75c-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fd75c-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="fd75c-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fd75c-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="fd75c-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fd75c-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fd75c-137">Schema Name</span></span>  <br/> |<span data-ttu-id="fd75c-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fd75c-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="fd75c-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fd75c-139">Validation File</span></span>  <br/> |<span data-ttu-id="fd75c-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fd75c-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fd75c-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fd75c-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="fd75c-142">False</span><span class="sxs-lookup"><span data-stu-id="fd75c-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fd75c-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fd75c-143">See also</span></span>



[<span data-ttu-id="fd75c-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fd75c-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fd75c-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fd75c-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="fd75c-146">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="fd75c-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

