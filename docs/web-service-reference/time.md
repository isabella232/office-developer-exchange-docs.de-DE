---
title: Zeit
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Time
api_type:
- schema
ms.assetid: c4b98be7-141c-4ba8-97ef-9ad1ed19f61f
description: Time-Element stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone.
ms.openlocfilehash: 716487fb7ed64dbaa6fa97caf1ea608e4673d2ef
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839188"
---
# <a name="time"></a><span data-ttu-id="deb6f-103">Zeit</span><span class="sxs-lookup"><span data-stu-id="deb6f-103">Time</span></span>

<span data-ttu-id="deb6f-104">**Time** -Element stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="deb6f-104">The **Time** element represents the transition time of day to and from standard time and daylight saving time.</span></span> 
  
```xml
<Time>...</Time>
```

 <span data-ttu-id="deb6f-105">**string**</span><span class="sxs-lookup"><span data-stu-id="deb6f-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="deb6f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="deb6f-106">Attributes and elements</span></span>

<span data-ttu-id="deb6f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="deb6f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="deb6f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="deb6f-108">Attributes</span></span>

<span data-ttu-id="deb6f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="deb6f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="deb6f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="deb6f-110">Child elements</span></span>

<span data-ttu-id="deb6f-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="deb6f-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="deb6f-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="deb6f-112">Parent elements</span></span>

|<span data-ttu-id="deb6f-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="deb6f-113">**Element**</span></span>|<span data-ttu-id="deb6f-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="deb6f-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="deb6f-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="deb6f-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="deb6f-116">Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC) dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="deb6f-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="deb6f-117">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="deb6f-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/><br/>  <span data-ttu-id="deb6f-118">Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="deb6f-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="deb6f-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="deb6f-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="deb6f-120">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="deb6f-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="deb6f-121">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="deb6f-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="deb6f-122">Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="deb6f-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="deb6f-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="deb6f-123">Text value</span></span>

<span data-ttu-id="deb6f-124">Der Textwert darstellt, Stunden, Minuten und Sekunden im folgenden Format: hh: mm:.</span><span class="sxs-lookup"><span data-stu-id="deb6f-124">The text value represents hours, minutes, and seconds in the following format: hh:mm:ss.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="deb6f-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="deb6f-125">Remarks</span></span>

<span data-ttu-id="deb6f-126">**Time** -Element im [DaylightTime](daylighttime.md) -Element auftritt, stellt die Tageszeit des Übergangs von Sommerzeit auf Normalzeit dar.</span><span class="sxs-lookup"><span data-stu-id="deb6f-126">When the **Time** element occurs in the [DaylightTime](daylighttime.md) element, it represents the time of day that the transition from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="deb6f-127">[Time](time.md) -Element im [StandardTime](standardtime.md) -Element auftritt, stellt die Tageszeit des Übergangs von der Standardzeit zur Sommerzeit dar.</span><span class="sxs-lookup"><span data-stu-id="deb6f-127">When the [Time](time.md) element occurs in the [StandardTime](standardtime.md) element, it represents the time of day that the transition from standard time to daylight saving time occurs.</span></span> 
  
<span data-ttu-id="deb6f-128">Dieses Element hat eine minimale Vorkommen von 0 (null) und eine maximale Vorkommen eines.</span><span class="sxs-lookup"><span data-stu-id="deb6f-128">This element has a minimum occurrence of zero and a maximum occurrence of one.</span></span>
  
## <a name="example"></a><span data-ttu-id="deb6f-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="deb6f-129">Example</span></span>

<span data-ttu-id="deb6f-130">Der folgende Teil einer Anforderung stellt eine Übergangszeit 2 Uhr</span><span class="sxs-lookup"><span data-stu-id="deb6f-130">The following part of a request represents a transition time of 2 A.M.</span></span> <span data-ttu-id="deb6f-131">von der Standardzeit zur Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="deb6f-131">from standard time to daylight saving time.</span></span>
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a><span data-ttu-id="deb6f-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="deb6f-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="deb6f-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="deb6f-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="deb6f-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="deb6f-134">Schema Name</span></span>  <br/> |<span data-ttu-id="deb6f-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="deb6f-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="deb6f-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="deb6f-136">Validation File</span></span>  <br/> |<span data-ttu-id="deb6f-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="deb6f-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="deb6f-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="deb6f-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="deb6f-139">False</span><span class="sxs-lookup"><span data-stu-id="deb6f-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="deb6f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="deb6f-140">See also</span></span>

- [<span data-ttu-id="deb6f-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="deb6f-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="deb6f-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="deb6f-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

