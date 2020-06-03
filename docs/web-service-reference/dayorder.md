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
description: Das DayOrder-Element stellt das n-te Vorkommen des im DayOfWeek-Element (TimeZone) angegebenen Tags dar, das das Datum des Übergangs von und zur Standardzeit und zur Sommerzeit darstellt.
ms.openlocfilehash: 53a8cb979bdb7aefead5623b4680f4c1a4ef5509
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526963"
---
# <a name="dayorder"></a><span data-ttu-id="046c9-103">DayOrder</span><span class="sxs-lookup"><span data-stu-id="046c9-103">DayOrder</span></span>

<span data-ttu-id="046c9-104">Das **DayOrder** -Element stellt das _n_th Vorkommen des Tags dar, der im [DayOfWeek-Element (TimeZone)](dayofweek-timezone.md) angegeben ist, das das Datum des Übergangs von und zur Standardzeit und zur Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="046c9-104">The **DayOrder** element represents the  _n_th occurrence of the day specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span> 
  
```xml
<DayOrder>...</DayOrder>
```

<span data-ttu-id="046c9-105">**kurz**</span><span class="sxs-lookup"><span data-stu-id="046c9-105">**short**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="046c9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="046c9-106">Attributes and elements</span></span>

<span data-ttu-id="046c9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="046c9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="046c9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="046c9-108">Attributes</span></span>

<span data-ttu-id="046c9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="046c9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="046c9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="046c9-110">Child elements</span></span>

<span data-ttu-id="046c9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="046c9-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="046c9-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="046c9-112">Parent elements</span></span>

|<span data-ttu-id="046c9-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="046c9-113">**Element**</span></span>|<span data-ttu-id="046c9-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="046c9-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="046c9-115">Standard Time</span><span class="sxs-lookup"><span data-stu-id="046c9-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="046c9-116">Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="046c9-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span><br/><br/><span data-ttu-id="046c9-117">Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="046c9-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="046c9-118">Im folgenden finden Sie die XPath-Ausdrücke für das [Standard](standardtime.md) Time-Element:</span><span class="sxs-lookup"><span data-stu-id="046c9-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="046c9-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="046c9-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="046c9-120">Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="046c9-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="046c9-121">Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="046c9-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span><br/><br/><span data-ttu-id="046c9-122">Im folgenden finden Sie die XPath-Ausdrücke für das [Daylight](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="046c9-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime`<br/><br/>`/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="046c9-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="046c9-123">Text value</span></span>

<span data-ttu-id="046c9-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="046c9-124">A text value is required.</span></span> <span data-ttu-id="046c9-125">Der Wert für das **DayOrder** -Element kann 1 bis 5 sein.</span><span class="sxs-lookup"><span data-stu-id="046c9-125">The value for the **DayOrder** element can be 1 through 5.</span></span> <span data-ttu-id="046c9-126">Der maximale Wert für dieses Element kann entweder 4 oder 5 sein, je nach Monat und Jahr.</span><span class="sxs-lookup"><span data-stu-id="046c9-126">The maximum value for this element can be either 4 or 5, depending on the month and year.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="046c9-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="046c9-127">Remarks</span></span>

<span data-ttu-id="046c9-128">Ein [Standard](standardtime.md) Time-Element, das ein **DayOrder** -Element mit dem Wert 5, einem [Month](month.md) -Element mit dem Wert 10 und einem DayOfWeek-Element [(TimeZone)](dayofweek-timezone.md) enthält, das den Wert "Sunday" aufweist, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt.</span><span class="sxs-lookup"><span data-stu-id="046c9-128">A [StandardTime](standardtime.md) element that contains a **DayOrder** element that has a value of 5, a [Month](month.md) element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="046c9-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="046c9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="046c9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="046c9-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="046c9-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="046c9-131">Schema Name</span></span>  <br/> |<span data-ttu-id="046c9-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="046c9-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="046c9-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="046c9-133">Validation File</span></span>  <br/> |<span data-ttu-id="046c9-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="046c9-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="046c9-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="046c9-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="046c9-136">False</span><span class="sxs-lookup"><span data-stu-id="046c9-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="046c9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="046c9-137">See also</span></span>

- [<span data-ttu-id="046c9-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="046c9-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="046c9-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="046c9-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

