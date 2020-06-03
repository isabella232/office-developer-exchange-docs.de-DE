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
description: Das Time-Element stellt die Übergangszeit von Tag zu und von Standardzeit und Sommerzeit dar.
ms.openlocfilehash: 97c89fbcbdb85fcdd4d32a1d44075ac42adef053
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460295"
---
# <a name="time"></a><span data-ttu-id="5579d-103">Time</span><span class="sxs-lookup"><span data-stu-id="5579d-103">Time</span></span>

<span data-ttu-id="5579d-104">Das **time** -Element stellt die Übergangszeit von Tag zu und von Standardzeit und Sommerzeit dar.</span><span class="sxs-lookup"><span data-stu-id="5579d-104">The **Time** element represents the transition time of day to and from standard time and daylight saving time.</span></span> 
  
```xml
<Time>...</Time>
```

 <span data-ttu-id="5579d-105">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="5579d-105">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5579d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5579d-106">Attributes and elements</span></span>

<span data-ttu-id="5579d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5579d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5579d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5579d-108">Attributes</span></span>

<span data-ttu-id="5579d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5579d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5579d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5579d-110">Child elements</span></span>

<span data-ttu-id="5579d-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5579d-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5579d-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5579d-112">Parent elements</span></span>

|<span data-ttu-id="5579d-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5579d-113">**Element**</span></span>|<span data-ttu-id="5579d-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5579d-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5579d-115">Standard Time</span><span class="sxs-lookup"><span data-stu-id="5579d-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="5579d-116">Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="5579d-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="5579d-117">Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="5579d-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/><br/>  <span data-ttu-id="5579d-118">Im folgenden finden Sie die XPath-Ausdrücke für das [Standard](standardtime.md) Time-Element:</span><span class="sxs-lookup"><span data-stu-id="5579d-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/> <br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="5579d-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="5579d-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="5579d-120">Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="5579d-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="5579d-121">Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5579d-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="5579d-122">Im folgenden finden Sie die XPath-Ausdrücke für das [Daylight](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="5579d-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/><br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5579d-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="5579d-123">Text value</span></span>

<span data-ttu-id="5579d-124">Der Wert Text stellt Stunden, Minuten und Sekunden im folgenden Format dar: hh: mm: SS.</span><span class="sxs-lookup"><span data-stu-id="5579d-124">The text value represents hours, minutes, and seconds in the following format: hh:mm:ss.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="5579d-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5579d-125">Remarks</span></span>

<span data-ttu-id="5579d-126">Wenn das **time** -Element im [Sommer](daylighttime.md) Zeitelement auftritt, stellt dies die Tageszeit dar, zu der der Übergang von Sommerzeit zu Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5579d-126">When the **Time** element occurs in the [DaylightTime](daylighttime.md) element, it represents the time of day that the transition from daylight saving time to standard time occurs.</span></span> <span data-ttu-id="5579d-127">Wenn das [time](time.md) -Element im [Standard](standardtime.md) Time-Element auftritt, stellt dies die Tageszeit dar, zu der der Übergang von Standardzeit zu Sommerzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="5579d-127">When the [Time](time.md) element occurs in the [StandardTime](standardtime.md) element, it represents the time of day that the transition from standard time to daylight saving time occurs.</span></span> 
  
<span data-ttu-id="5579d-128">Dieses Element hat ein Mindestvorkommen von 0 (null) und ein Maximum des Auftretens von 1.</span><span class="sxs-lookup"><span data-stu-id="5579d-128">This element has a minimum occurrence of zero and a maximum occurrence of one.</span></span>
  
## <a name="example"></a><span data-ttu-id="5579d-129">Beispiel</span><span class="sxs-lookup"><span data-stu-id="5579d-129">Example</span></span>

<span data-ttu-id="5579d-130">Der folgende Teil einer Anforderung stellt eine Übergangszeit von 2 Uhr dar.</span><span class="sxs-lookup"><span data-stu-id="5579d-130">The following part of a request represents a transition time of 2 A.M.</span></span> <span data-ttu-id="5579d-131">von Standardzeit zu Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="5579d-131">from standard time to daylight saving time.</span></span>
  
```xml
<StandardTime>
   <Bias>0</Bias>
   <Time>02:00:00</Time>
   <DayOrder>5</DayOrder>
   <Month>10</Month>
   <DayOfWeek>Sunday</DayOfWeek>
</StandardTime
```

## <a name="element-information"></a><span data-ttu-id="5579d-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5579d-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5579d-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="5579d-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5579d-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5579d-134">Schema Name</span></span>  <br/> |<span data-ttu-id="5579d-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5579d-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="5579d-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5579d-136">Validation File</span></span>  <br/> |<span data-ttu-id="5579d-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5579d-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5579d-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5579d-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="5579d-139">False</span><span class="sxs-lookup"><span data-stu-id="5579d-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5579d-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5579d-140">See also</span></span>

- [<span data-ttu-id="5579d-141">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5579d-141">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="5579d-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="5579d-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

