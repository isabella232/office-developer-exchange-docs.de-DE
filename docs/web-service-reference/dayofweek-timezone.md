---
title: DayOfWeek (Zeitzone)
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
description: Das DayOfWeek-Element stellt den Wochentag dar, an dem der Zeitzonenübergang erfolgt.
ms.openlocfilehash: 7bc05f417268ccfb20adae12e2694d8360023ab2
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457844"
---
# <a name="dayofweek-timezone"></a><span data-ttu-id="d6f17-103">DayOfWeek (Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="d6f17-103">DayOfWeek (TimeZone)</span></span>

<span data-ttu-id="d6f17-104">Das **DayOfWeek** -Element stellt den Wochentag dar, an dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d6f17-104">The **DayOfWeek** element represents the day of the week on which the time zone transition occurs.</span></span> 
  
```xml
<DayOfWeek>...</DayOfWeek>
```

<span data-ttu-id="d6f17-105">**Dayofweektype**</span><span class="sxs-lookup"><span data-stu-id="d6f17-105">**DayOfWeekType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d6f17-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d6f17-106">Attributes and elements</span></span>

<span data-ttu-id="d6f17-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d6f17-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d6f17-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d6f17-108">Attributes</span></span>

<span data-ttu-id="d6f17-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6f17-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d6f17-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6f17-110">Child elements</span></span>

<span data-ttu-id="d6f17-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="d6f17-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d6f17-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d6f17-112">Parent elements</span></span>

|<span data-ttu-id="d6f17-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="d6f17-113">**Element**</span></span>|<span data-ttu-id="d6f17-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d6f17-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d6f17-115">Standard Time</span><span class="sxs-lookup"><span data-stu-id="d6f17-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="d6f17-116">Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="d6f17-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="d6f17-117">Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="d6f17-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="d6f17-118">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="d6f17-118">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="d6f17-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="d6f17-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="d6f17-120">Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="d6f17-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="d6f17-121">Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d6f17-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="d6f17-122">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="d6f17-122">The following are the XPath expressions to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
|[<span data-ttu-id="d6f17-123">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="d6f17-123">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="d6f17-124">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d6f17-124">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d6f17-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="d6f17-125">Text value</span></span>

<span data-ttu-id="d6f17-126">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d6f17-126">A text value is required.</span></span> <span data-ttu-id="d6f17-127">Der Textwert wird durch eine Aufzählung dargestellt, die die folgenden möglichen Werte aufweist:</span><span class="sxs-lookup"><span data-stu-id="d6f17-127">The text value is represented by an enumeration that has the following possible values:</span></span>
  
- <span data-ttu-id="d6f17-128">Sonntag</span><span class="sxs-lookup"><span data-stu-id="d6f17-128">Sunday</span></span>    
- <span data-ttu-id="d6f17-129">Montag</span><span class="sxs-lookup"><span data-stu-id="d6f17-129">Monday</span></span>    
- <span data-ttu-id="d6f17-130">Dienstag</span><span class="sxs-lookup"><span data-stu-id="d6f17-130">Tuesday</span></span>    
- <span data-ttu-id="d6f17-131">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="d6f17-131">Wednesday</span></span>    
- <span data-ttu-id="d6f17-132">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="d6f17-132">Thursday</span></span>    
- <span data-ttu-id="d6f17-133">Freitag</span><span class="sxs-lookup"><span data-stu-id="d6f17-133">Friday</span></span>    
- <span data-ttu-id="d6f17-134">Samstag</span><span class="sxs-lookup"><span data-stu-id="d6f17-134">Saturday</span></span>    
- <span data-ttu-id="d6f17-135">Tag</span><span class="sxs-lookup"><span data-stu-id="d6f17-135">Day</span></span>    
- <span data-ttu-id="d6f17-136">Wochentag</span><span class="sxs-lookup"><span data-stu-id="d6f17-136">Weekday</span></span>   
- <span data-ttu-id="d6f17-137">WeekendDay</span><span class="sxs-lookup"><span data-stu-id="d6f17-137">WeekendDay</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d6f17-138">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d6f17-138">Remarks</span></span>

<span data-ttu-id="d6f17-139">Ein [Standard](standardtime.md) Time-Element, das ein [DayOrder](dayorder.md) -Element mit dem Wert 5, einem [Month](month.md) -Element mit dem Wert 10 und einem **DayOfWeek** -Element mit dem Wert "Sunday" enthält, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d6f17-139">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a [Month](month.md) element that has a value of 10, and a **DayOfWeek** element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
<span data-ttu-id="d6f17-140">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d6f17-140">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d6f17-141">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d6f17-141">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d6f17-142">Namespace</span><span class="sxs-lookup"><span data-stu-id="d6f17-142">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d6f17-143">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d6f17-143">Schema Name</span></span>  <br/> |<span data-ttu-id="d6f17-144">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d6f17-144">Types schema</span></span>  <br/> |
|<span data-ttu-id="d6f17-145">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d6f17-145">Validation File</span></span>  <br/> |<span data-ttu-id="d6f17-146">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d6f17-146">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d6f17-147">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d6f17-147">Can be Empty</span></span>  <br/> |<span data-ttu-id="d6f17-148">False</span><span class="sxs-lookup"><span data-stu-id="d6f17-148">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d6f17-149">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d6f17-149">See also</span></span>

- [<span data-ttu-id="d6f17-150">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d6f17-150">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="d6f17-151">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="d6f17-151">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

