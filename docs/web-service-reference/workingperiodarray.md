---
title: WorkingPeriodArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriodArray
api_type:
- schema
ms.assetid: 3a3f6393-eacc-4734-b6c9-b67023fe2830
description: Das WorkingPeriodArray-Element enthält Informationen für den Postfachbenutzer Perioden arbeiten.
ms.openlocfilehash: 02712f05dc3373a532d769f476341b78ad25a79c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839555"
---
# <a name="workingperiodarray"></a><span data-ttu-id="e2694-103">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="e2694-103">WorkingPeriodArray</span></span>

<span data-ttu-id="e2694-104">Das **WorkingPeriodArray** -Element enthält Informationen für den Postfachbenutzer Perioden arbeiten.</span><span class="sxs-lookup"><span data-stu-id="e2694-104">The **WorkingPeriodArray** element contains working period information for the mailbox user.</span></span> 
  
[<span data-ttu-id="e2694-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e2694-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e2694-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="e2694-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="e2694-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="e2694-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="e2694-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="e2694-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="e2694-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="e2694-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="e2694-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="e2694-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
```xml
<WorkingPeriodArray>
   <WorkingPeriod>...</WorkingPeriod>
</WorkingPeriodArray>
```

 <span data-ttu-id="e2694-111">**ArrayOfWorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="e2694-111">**ArrayOfWorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2694-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e2694-112">Attributes and elements</span></span>

<span data-ttu-id="e2694-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2694-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2694-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2694-114">Attributes</span></span>

<span data-ttu-id="e2694-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2694-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2694-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2694-116">Child elements</span></span>

|<span data-ttu-id="e2694-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2694-117">**Element**</span></span>|<span data-ttu-id="e2694-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2694-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2694-119">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="e2694-119">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="e2694-120">Enthält die Arbeitswoche Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="e2694-120">Contains the work week days and hours of the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2694-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2694-121">Parent elements</span></span>

|<span data-ttu-id="e2694-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2694-122">**Element**</span></span>|<span data-ttu-id="e2694-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2694-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2694-124">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="e2694-124">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="e2694-125">Stellt die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="e2694-125">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="e2694-126">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e2694-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2694-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e2694-127">Remarks</span></span>

<span data-ttu-id="e2694-128">Dieses Element ist erforderlich, wenn das [WorkingHours](workinghours-ex15websvcsotherref.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="e2694-128">This element is required if the [WorkingHours](workinghours-ex15websvcsotherref.md) element is used.</span></span> <span data-ttu-id="e2694-129">All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen.</span><span class="sxs-lookup"><span data-stu-id="e2694-129">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="e2694-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e2694-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2694-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e2694-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2694-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2694-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2694-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e2694-133">Schema Name</span></span>  <br/> |<span data-ttu-id="e2694-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e2694-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2694-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2694-135">Validation File</span></span>  <br/> |<span data-ttu-id="e2694-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2694-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2694-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e2694-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2694-138">False</span><span class="sxs-lookup"><span data-stu-id="e2694-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2694-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2694-139">See also</span></span>



[<span data-ttu-id="e2694-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e2694-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e2694-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e2694-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e2694-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="e2694-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

