---
title: DayOfWeek (TimeZone)
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
ms.assetid: 416e8892-ebb1-4fac-82cf-e27549a6c175
description: Des DayOfWeek-Elements darstellt, auf dem die Zeitzone Übergangs, Wochentag.
ms.openlocfilehash: 7816b90000be36cf3a3354d26d978684bfdcfe40
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757877"
---
# <a name="dayofweek-timezone"></a><span data-ttu-id="1e573-103">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="1e573-103">DayOfWeek (TimeZone)</span></span>

<span data-ttu-id="1e573-104">Des **DayOfWeek** -Elements darstellt, auf dem die Zeitzone Übergangs, Wochentag.</span><span class="sxs-lookup"><span data-stu-id="1e573-104">The **DayOfWeek** element represents the day of the week on which the time zone transition occurs.</span></span> 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

<span data-ttu-id="1e573-105">**DayOfWeekType**</span><span class="sxs-lookup"><span data-stu-id="1e573-105">**DayOfWeekType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1e573-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1e573-106">Attributes and elements</span></span>

<span data-ttu-id="1e573-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1e573-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1e573-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1e573-108">Attributes</span></span>

<span data-ttu-id="1e573-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e573-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1e573-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e573-110">Child elements</span></span>

<span data-ttu-id="1e573-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1e573-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="1e573-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1e573-112">Parent elements</span></span>

|<span data-ttu-id="1e573-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1e573-113">**Element**</span></span>|<span data-ttu-id="1e573-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1e573-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1e573-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="1e573-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="1e573-116">Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC) dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="1e573-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="1e573-117">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="1e573-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="1e573-118">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="1e573-118">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="1e573-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="1e573-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="1e573-120">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="1e573-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="1e573-121">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="1e573-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="1e573-122">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="1e573-122">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[<span data-ttu-id="1e573-123">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="1e573-123">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="1e573-124">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="1e573-124">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="1e573-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="1e573-125">Text value</span></span>

<span data-ttu-id="1e573-126">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1e573-126">A text value is required.</span></span> <span data-ttu-id="1e573-127">Der Textwert wird durch eine Enumeration dargestellt, die die folgenden möglichen Werte hat:</span><span class="sxs-lookup"><span data-stu-id="1e573-127">The text value is represented by an enumeration that has the following possible values:</span></span>
  
- <span data-ttu-id="1e573-128">Sonntag</span><span class="sxs-lookup"><span data-stu-id="1e573-128">Sunday</span></span>    
- <span data-ttu-id="1e573-129">Montag</span><span class="sxs-lookup"><span data-stu-id="1e573-129">Monday</span></span>    
- <span data-ttu-id="1e573-130">Dienstag</span><span class="sxs-lookup"><span data-stu-id="1e573-130">Tuesday</span></span>    
- <span data-ttu-id="1e573-131">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="1e573-131">Wednesday</span></span>    
- <span data-ttu-id="1e573-132">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="1e573-132">Thursday</span></span>    
- <span data-ttu-id="1e573-133">Freitag</span><span class="sxs-lookup"><span data-stu-id="1e573-133">Friday</span></span>    
- <span data-ttu-id="1e573-134">Samstag</span><span class="sxs-lookup"><span data-stu-id="1e573-134">Saturday</span></span>    
- <span data-ttu-id="1e573-135">Tag</span><span class="sxs-lookup"><span data-stu-id="1e573-135">Day</span></span>    
- <span data-ttu-id="1e573-136">Wochentag</span><span class="sxs-lookup"><span data-stu-id="1e573-136">Weekday</span></span>   
- <span data-ttu-id="1e573-137">WeekendDay</span><span class="sxs-lookup"><span data-stu-id="1e573-137">WeekendDay</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1e573-138">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1e573-138">Remarks</span></span>

<span data-ttu-id="1e573-139">Ein [StandardTime](standardtime.md) -Element, enthält ein [DayOrder](dayorder.md) -Element, das den Wert 5 hat, ein [Month](month.md) -Element, das einen Wert von 10 aufweist und ein **DayOfWeek** -Element, das den Wert Sonntag hat, bedeutet, dass den Übergang von Normalzeit zu Sommerzeit sparen Sie Zeit tritt am fünften Sonntag der zehnte Monat.</span><span class="sxs-lookup"><span data-stu-id="1e573-139">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a [Month](month.md) element that has a value of 10, and a **DayOfWeek** element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
<span data-ttu-id="1e573-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="1e573-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1e573-141">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1e573-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1e573-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="1e573-142">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1e573-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1e573-143">Schema Name</span></span>  <br/> |<span data-ttu-id="1e573-144">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1e573-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="1e573-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1e573-145">Validation File</span></span>  <br/> |<span data-ttu-id="1e573-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1e573-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1e573-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1e573-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="1e573-148">False</span><span class="sxs-lookup"><span data-stu-id="1e573-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1e573-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1e573-149">See also</span></span>

- [<span data-ttu-id="1e573-150">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1e573-150">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="1e573-151">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="1e573-151">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

