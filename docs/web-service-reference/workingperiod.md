---
title: WorkingPeriod
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriod
api_type:
- schema
ms.assetid: 3b4e48af-9880-42b9-a0dc-dae7ac43c264
description: Das WorkingPeriod-Element enthält die Arbeitswoche Tage und Stunden des Postfachbenutzers.
ms.openlocfilehash: 0f2707bede5e49174ed62a35ba704e39c0c48e9f
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839556"
---
# <a name="workingperiod"></a><span data-ttu-id="1ab18-103">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="1ab18-103">WorkingPeriod</span></span>

<span data-ttu-id="1ab18-104">Das **WorkingPeriod** -Element enthält die Arbeitswoche Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="1ab18-104">The **WorkingPeriod** element contains the work week days and hours of the mailbox user.</span></span> 
  
[<span data-ttu-id="1ab18-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1ab18-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="1ab18-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="1ab18-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="1ab18-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="1ab18-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="1ab18-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="1ab18-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="1ab18-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="1ab18-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="1ab18-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="1ab18-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="1ab18-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="1ab18-111">WorkingPeriod</span></span>](workingperiod.md)
  
```xml
<WorkingPeriod>
   <DayOfWeek>...</DayOfWeek>
   <StartTimeInMinutes>...</StartTimeInMinutes>
   <EndTimeInMinutes>...</EndTimeInMinutes>
</WorkingPeriod>
```

 <span data-ttu-id="1ab18-112">**WorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="1ab18-112">**WorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1ab18-113">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1ab18-113">Attributes and elements</span></span>

<span data-ttu-id="1ab18-114">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1ab18-114">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1ab18-115">Attribute</span><span class="sxs-lookup"><span data-stu-id="1ab18-115">Attributes</span></span>

<span data-ttu-id="1ab18-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="1ab18-116">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1ab18-117">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ab18-117">Child elements</span></span>

|<span data-ttu-id="1ab18-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ab18-118">**Element**</span></span>|<span data-ttu-id="1ab18-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ab18-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ab18-120">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="1ab18-120">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md) <br/> |<span data-ttu-id="1ab18-121">Enthält die Liste von Arbeitstagen für den Postfachbenutzer geplant.</span><span class="sxs-lookup"><span data-stu-id="1ab18-121">Contains the list of working days scheduled for the mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="1ab18-122">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="1ab18-122">StartTimeInMinutes</span></span>](starttimeinminutes.md) <br/> |<span data-ttu-id="1ab18-123">Stellt den Anfang des den Arbeitstag für einen Postfachbenutzer an.</span><span class="sxs-lookup"><span data-stu-id="1ab18-123">Represents the start of the working day for a mailbox user.</span></span>  <br/> |
|[<span data-ttu-id="1ab18-124">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="1ab18-124">EndTimeInMinutes</span></span>](endtimeinminutes.md) <br/> |<span data-ttu-id="1ab18-125">Das Ende des Arbeitstags für einen Postfachbenutzer darstellt.</span><span class="sxs-lookup"><span data-stu-id="1ab18-125">Represents the end of the working day for a mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1ab18-126">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1ab18-126">Parent elements</span></span>

|<span data-ttu-id="1ab18-127">**Element**</span><span class="sxs-lookup"><span data-stu-id="1ab18-127">**Element**</span></span>|<span data-ttu-id="1ab18-128">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1ab18-128">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1ab18-129">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="1ab18-129">WorkingPeriodArray</span></span>](workingperiodarray.md) <br/> |<span data-ttu-id="1ab18-130">Enthält Informationen zu Perioden für den Postfachbenutzer arbeiten.</span><span class="sxs-lookup"><span data-stu-id="1ab18-130">Contains working period information for the mailbox user.</span></span>  <br/> <span data-ttu-id="1ab18-131">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1ab18-131">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1ab18-132">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1ab18-132">Remarks</span></span>

<span data-ttu-id="1ab18-133">All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen.</span><span class="sxs-lookup"><span data-stu-id="1ab18-133">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="1ab18-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="1ab18-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1ab18-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1ab18-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1ab18-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="1ab18-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1ab18-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1ab18-137">Schema Name</span></span>  <br/> |<span data-ttu-id="1ab18-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1ab18-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="1ab18-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1ab18-139">Validation File</span></span>  <br/> |<span data-ttu-id="1ab18-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1ab18-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1ab18-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1ab18-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="1ab18-142">False</span><span class="sxs-lookup"><span data-stu-id="1ab18-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1ab18-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1ab18-143">See also</span></span>



[<span data-ttu-id="1ab18-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1ab18-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1ab18-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="1ab18-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="1ab18-146">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="1ab18-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

