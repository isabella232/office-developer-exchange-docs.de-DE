---
title: DayOrder
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOrder
api_type:
- schema
ms.assetid: 3022f839-12a2-42a9-820e-3ea585ce8657
description: Das DayOrder-Element darstellt, das n-te Vorkommen des Tages im DayOfWeek (TimeZone)-Element, das das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt.
ms.openlocfilehash: 03ee678611a6cf58a7256ded67ab4d0a8a06a7ee
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757882"
---
# <a name="dayorder"></a><span data-ttu-id="8136b-103">DayOrder</span><span class="sxs-lookup"><span data-stu-id="8136b-103">DayOrder</span></span>

<span data-ttu-id="8136b-104">Das **DayOrder** -Element darstellt, das _n_th Vorkommen des Tages im [DayOfWeek (TimeZone)](dayofweek-timezone.md) -Element, das das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="8136b-104">The **DayOrder** element represents the  _n_th occurrence of the day specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span> 
  
```xml
<DayOrder>...</DayOrder>
```

<span data-ttu-id="8136b-105">**kurze**</span><span class="sxs-lookup"><span data-stu-id="8136b-105">**short**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8136b-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8136b-106">Attributes and elements</span></span>

<span data-ttu-id="8136b-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8136b-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8136b-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8136b-108">Attributes</span></span>

<span data-ttu-id="8136b-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8136b-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8136b-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8136b-110">Child elements</span></span>

<span data-ttu-id="8136b-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="8136b-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="8136b-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8136b-112">Parent elements</span></span>

|<span data-ttu-id="8136b-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="8136b-113">**Element**</span></span>|<span data-ttu-id="8136b-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8136b-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8136b-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="8136b-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="8136b-116">Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC) dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="8136b-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="8136b-117">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="8136b-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="8136b-118">Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="8136b-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="8136b-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="8136b-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="8136b-120">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="8136b-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="8136b-121">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="8136b-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="8136b-122">Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="8136b-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="8136b-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="8136b-123">Text value</span></span>

<span data-ttu-id="8136b-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="8136b-124">A text value is required.</span></span> <span data-ttu-id="8136b-125">Der Wert für das **DayOrder** -Element kann 1 bis 5 entsprechen.</span><span class="sxs-lookup"><span data-stu-id="8136b-125">The value for the **DayOrder** element can be 1 through 5.</span></span> <span data-ttu-id="8136b-126">Der maximale Wert für dieses Element kann 4 oder 5, je nach Monat und Jahr sein.</span><span class="sxs-lookup"><span data-stu-id="8136b-126">The maximum value for this element can be either 4 or 5, depending on the month and year.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="8136b-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="8136b-127">Remarks</span></span>

<span data-ttu-id="8136b-128">Ein [StandardTime](standardtime.md) -Element, enthält ein **DayOrder** -Element, das den Wert 5 hat, ein [Month](month.md) -Element, das einen Wert von 10 aufweist und ein [DayOfWeek (TimeZone)](dayofweek-timezone.md) -Element, das den Wert Sonntag hat, bedeutet, dass den Übergang vom Standardzeit Sommerzeit tritt am fünften Sonntag der zehnte Monat.</span><span class="sxs-lookup"><span data-stu-id="8136b-128">A [StandardTime](standardtime.md) element that contains a **DayOrder** element that has a value of 5, a [Month](month.md) element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="8136b-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="8136b-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8136b-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="8136b-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8136b-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8136b-131">Schema Name</span></span>  <br/> |<span data-ttu-id="8136b-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8136b-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="8136b-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8136b-133">Validation File</span></span>  <br/> |<span data-ttu-id="8136b-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8136b-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8136b-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8136b-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="8136b-136">False</span><span class="sxs-lookup"><span data-stu-id="8136b-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8136b-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8136b-137">See also</span></span>

- [<span data-ttu-id="8136b-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="8136b-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="8136b-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="8136b-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

