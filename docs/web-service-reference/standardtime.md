---
title: StandardTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StandardTime
api_type:
- schema
ms.assetid: 13084726-ab24-4009-be99-c4a4273c9e05
description: Das StandardTime-Element stellt einen Offset von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die Verschiebung (UTC) Element dargestellt wird. Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.
ms.openlocfilehash: 726c31ffba06c1c437711b88444ec5eba45b520d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831546"
---
# <a name="standardtime"></a><span data-ttu-id="f2968-104">StandardTime</span><span class="sxs-lookup"><span data-stu-id="f2968-104">StandardTime</span></span>

<span data-ttu-id="f2968-105">Das **StandardTime** -Element stellt einen Offset von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2968-105">The **StandardTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="f2968-106">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="f2968-106">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> 
  
- [<span data-ttu-id="f2968-107">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="f2968-107">TimeZone (Availability)</span></span>](timezone-availability.md)
- [<span data-ttu-id="f2968-108">StandardTime</span><span class="sxs-lookup"><span data-stu-id="f2968-108">StandardTime</span></span>](standardtime.md)
  
```xml
<StandardTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</StandardTime>
```

 <span data-ttu-id="f2968-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="f2968-109">**SerializableTimeZoneTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2968-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2968-110">Attributes and elements</span></span>

<span data-ttu-id="f2968-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2968-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2968-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2968-112">Attributes</span></span>

<span data-ttu-id="f2968-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2968-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2968-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2968-114">Child elements</span></span>

|<span data-ttu-id="f2968-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2968-115">**Element**</span></span>|<span data-ttu-id="f2968-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2968-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2968-117">Bias</span><span class="sxs-lookup"><span data-stu-id="f2968-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="f2968-118">Stellt den Offset von der UTC-Offset, der durch das Element [Bias (UTC)](bias-utc.md) für Standardzeit und Sommerzeit identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="f2968-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="f2968-119">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="f2968-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="f2968-120">Time</span><span class="sxs-lookup"><span data-stu-id="f2968-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="f2968-121">Stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="f2968-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="f2968-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="f2968-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="f2968-123">Stellt das _n_th Vorkommen des Tags, das im Element [DayOfWeek (TimeZone)](dayofweek-timezone.md) angegeben wird, die das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2968-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="f2968-124">Month</span><span class="sxs-lookup"><span data-stu-id="f2968-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="f2968-125">Stellt den Übergang Monat des Jahres zu und von Standardzeit und Sommerzeit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="f2968-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="f2968-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="f2968-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="f2968-127">Tritt für der Übergang zu und von Standardzeit und Sommerzeit Wochentag darstellt.</span><span class="sxs-lookup"><span data-stu-id="f2968-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="f2968-128">Jahr</span><span class="sxs-lookup"><span data-stu-id="f2968-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="f2968-129">Definiert eine Zeitzone, die sich je nach dem Jahr ändern.</span><span class="sxs-lookup"><span data-stu-id="f2968-129">Defines a time zone that changes depending on the year.</span></span> <span data-ttu-id="f2968-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="f2968-130">This element is optional.</span></span> <span data-ttu-id="f2968-131">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="f2968-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2968-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2968-132">Parent elements</span></span>

|<span data-ttu-id="f2968-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2968-133">**Element**</span></span>|<span data-ttu-id="f2968-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2968-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2968-135">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="f2968-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="f2968-136">Enthält Elemente, die Informationen zur Zeitzone zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="f2968-136">Contains elements that identify time zone information.</span></span> <span data-ttu-id="f2968-137">Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="f2968-137">This element also contains information about the transition between standard time and daylight saving time.</span></span> <br/><br/><span data-ttu-id="f2968-138">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="f2968-138">The following are the XPath expressions to this element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/> <br/> `/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2968-139">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f2968-139">Remarks</span></span>

<span data-ttu-id="f2968-140">Das **StandardTime** -Element stellt eine Offset Zeit, die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2968-140">The **StandardTime** element represents an offset time that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="f2968-141">Wenn das untergeordnete [Bias](bias.md) -Element gleich 0 ist, ist die Standardzeit gleich dem Bias Offset von UTC, die durch die [Verschiebung (UTC)](bias-utc.md) Element dargestellt wird.</span><span class="sxs-lookup"><span data-stu-id="f2968-141">When the child [Bias](bias.md) element equals 0, the standard time is equal to the bias offset from UTC that is represented by the [Bias (UTC)](bias-utc.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f2968-142">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f2968-142">Example</span></span>

<span data-ttu-id="f2968-143">Das folgende Beispiel zeigt einen Bereich, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="f2968-143">The following example shows a region where daylight saving time is observed.</span></span> <span data-ttu-id="f2968-144">Der Übergang von Sommerzeit auf Normalzeit wird um 2 Uhr morgens eingehalten</span><span class="sxs-lookup"><span data-stu-id="f2968-144">The transition from daylight saving time to standard time is observed at 2 A.M.</span></span> <span data-ttu-id="f2968-145">Klicken Sie auf der fünften Sonntag der zehnte Monat.</span><span class="sxs-lookup"><span data-stu-id="f2968-145">on the fifth Sunday of the tenth month.</span></span>
  
```xml
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>5</DayOrder>
    <Month>10</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>4</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## <a name="element-information"></a><span data-ttu-id="f2968-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f2968-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2968-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2968-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2968-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2968-148">Schema Name</span></span>  <br/> |<span data-ttu-id="f2968-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f2968-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2968-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2968-150">Validation File</span></span>  <br/> |<span data-ttu-id="f2968-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2968-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2968-152">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f2968-152">Can be Empty</span></span>  <br/> |<span data-ttu-id="f2968-153">False</span><span class="sxs-lookup"><span data-stu-id="f2968-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2968-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2968-154">See also</span></span>

- [<span data-ttu-id="f2968-155">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f2968-155">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="f2968-156">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="f2968-156">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

