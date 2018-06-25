---
title: DayOfWeek (WorkingPeriod)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 7a8a8cc1-392b-4db5-bb76-710477e31396
description: DayOfWeek-Element enthält die Liste von Arbeitstagen für den Postfachbenutzer geplant.
ms.openlocfilehash: a6a68017291ba13f45b3970307669222d583fcbb
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757884"
---
# <a name="dayofweek-workingperiod"></a><span data-ttu-id="3903b-103">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="3903b-103">DayOfWeek (WorkingPeriod)</span></span>

<span data-ttu-id="3903b-104">**DayOfWeek** -Element enthält die Liste von Arbeitstagen für den Postfachbenutzer geplant.</span><span class="sxs-lookup"><span data-stu-id="3903b-104">The **DayOfWeek** element contains the list of working days scheduled for the mailbox user.</span></span> 
  
- [<span data-ttu-id="3903b-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3903b-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="3903b-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="3903b-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)  
- [<span data-ttu-id="3903b-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="3903b-107">FreeBusyResponse</span></span>](freebusyresponse.md)  
- [<span data-ttu-id="3903b-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="3903b-108">FreeBusyView</span></span>](freebusyview.md)  
- [<span data-ttu-id="3903b-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="3903b-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)  
- [<span data-ttu-id="3903b-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="3903b-110">WorkingPeriodArray</span></span>](workingperiodarray.md) 
- [<span data-ttu-id="3903b-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="3903b-111">WorkingPeriod</span></span>](workingperiod.md)  
- [<span data-ttu-id="3903b-112">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="3903b-112">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

<span data-ttu-id="3903b-113">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="3903b-113">**DaysOfWeek**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="3903b-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3903b-114">Attributes and elements</span></span>

<span data-ttu-id="3903b-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3903b-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3903b-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="3903b-116">Attributes</span></span>

<span data-ttu-id="3903b-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="3903b-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3903b-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3903b-118">Child elements</span></span>

<span data-ttu-id="3903b-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="3903b-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="3903b-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3903b-120">Parent elements</span></span>

|<span data-ttu-id="3903b-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="3903b-121">**Element**</span></span>|<span data-ttu-id="3903b-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3903b-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3903b-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="3903b-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="3903b-124">Enthält die Arbeitswoche Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="3903b-124">Contains the work week days and hours of the mailbox user.</span></span><br/><br/><span data-ttu-id="3903b-125">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3903b-125">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="3903b-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="3903b-126">Text value</span></span>

<span data-ttu-id="3903b-127">Ein Textwert wird zurückgegeben, wenn der Postfachbenutzer Tage, die zur Darstellung der Arbeitswoche festgelegt hat.</span><span class="sxs-lookup"><span data-stu-id="3903b-127">A text value is returned if the mailbox user has days set to represent the work week.</span></span> <span data-ttu-id="3903b-128">Es folgen die möglichen Werte für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="3903b-128">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="3903b-129">Sonntag</span><span class="sxs-lookup"><span data-stu-id="3903b-129">Sunday</span></span>    
- <span data-ttu-id="3903b-130">Montag</span><span class="sxs-lookup"><span data-stu-id="3903b-130">Monday</span></span>    
- <span data-ttu-id="3903b-131">Dienstag</span><span class="sxs-lookup"><span data-stu-id="3903b-131">Tuesday</span></span>    
- <span data-ttu-id="3903b-132">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="3903b-132">Wednesday</span></span>    
- <span data-ttu-id="3903b-133">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="3903b-133">Thursday</span></span>    
- <span data-ttu-id="3903b-134">Freitag</span><span class="sxs-lookup"><span data-stu-id="3903b-134">Friday</span></span>    
- <span data-ttu-id="3903b-135">Samstag</span><span class="sxs-lookup"><span data-stu-id="3903b-135">Saturday</span></span> 
    
<span data-ttu-id="3903b-136">Die Textwerte werden in dieser Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="3903b-136">The text values will be returned in that order.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="3903b-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="3903b-137">Remarks</span></span>

<span data-ttu-id="3903b-138">Es ist wichtig, beachten Sie, dass der Unterschied zwischen diesem Element und der Verfügbarkeit [(TimeZone) DayOfWeek](dayofweek-timezone.md) -Element der Typ ist.</span><span class="sxs-lookup"><span data-stu-id="3903b-138">It is important to note that the difference between this element and the Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) element is the type.</span></span> 
  
<span data-ttu-id="3903b-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="3903b-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3903b-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="3903b-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3903b-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="3903b-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3903b-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3903b-142">Schema Name</span></span>  <br/> |<span data-ttu-id="3903b-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3903b-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="3903b-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3903b-144">Validation File</span></span>  <br/> |<span data-ttu-id="3903b-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3903b-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3903b-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3903b-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="3903b-147">False</span><span class="sxs-lookup"><span data-stu-id="3903b-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3903b-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3903b-148">See also</span></span>

- [<span data-ttu-id="3903b-149">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="3903b-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="3903b-150">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="3903b-150">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="3903b-151">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="3903b-151">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

