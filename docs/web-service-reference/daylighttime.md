---
title: DaylightTime
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DaylightTime
api_type:
- schema
ms.assetid: 9f551ee4-d945-477c-b981-9554b197d26d
description: DaylightTime-Element stellt einen Offset von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die Verschiebung (UTC) Element Regionen dargestellt wird, in dem Sommerzeit beobachtet wird. Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.
ms.openlocfilehash: 07ec4b1a5f84669aca33d46cdf1fa2e578f3b43b
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757876"
---
# <a name="daylighttime"></a><span data-ttu-id="13934-104">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="13934-104">DaylightTime</span></span>

<span data-ttu-id="13934-105">**DaylightTime** -Element stellt einen Offset von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC), die durch die [Verschiebung (UTC)](bias-utc.md) Element Regionen dargestellt wird, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="13934-105">The **DaylightTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="13934-106">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="13934-106">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span> 
  
- [<span data-ttu-id="13934-107">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="13934-107">TimeZone (Availability)</span></span>](timezone-availability.md) 
- [<span data-ttu-id="13934-108">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="13934-108">DaylightTime</span></span>](daylighttime.md)
  
```xml
<DaylightTime>
   <Bias>int</Bias>
   <Time>string</Time>
   <DayOrder>short</DayOrder>
   <Month>short</Month>
   <DayOfWeek>Sunday or Monday or Tuesday or Wednesday or Thursday or Friday or Saturday</DayOfWeek>
   <Year>string</Year>
</DaylightTime>
```

<span data-ttu-id="13934-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="13934-109">**SerializableTimeZoneTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="13934-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="13934-110">Attributes and elements</span></span>

<span data-ttu-id="13934-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="13934-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="13934-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="13934-112">Attributes</span></span>

<span data-ttu-id="13934-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="13934-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="13934-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13934-114">Child elements</span></span>

|<span data-ttu-id="13934-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="13934-115">**Element**</span></span>|<span data-ttu-id="13934-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13934-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13934-117">Bias</span><span class="sxs-lookup"><span data-stu-id="13934-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="13934-118">Stellt den Offset von der UTC-Offset, der durch das Element [Bias (UTC)](bias-utc.md) für Standardzeit und Sommerzeit identifiziert wird.</span><span class="sxs-lookup"><span data-stu-id="13934-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="13934-119">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="13934-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="13934-120">Time</span><span class="sxs-lookup"><span data-stu-id="13934-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="13934-121">Stellt die Tageszeit Übergang zu und von Standardzeit und Sommerzeit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="13934-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="13934-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="13934-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="13934-123">Stellt das _n_th Vorkommen des Tags, das im Element [DayOfWeek (TimeZone)](dayofweek-timezone.md) angegeben wird, die das Datum des Übergangs from und to Standardzeit und der Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="13934-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="13934-124">Month</span><span class="sxs-lookup"><span data-stu-id="13934-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="13934-125">Stellt den Übergang Monat des Jahres zu und von Standardzeit und Sommerzeit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="13934-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="13934-126">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="13934-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="13934-127">Tritt für der Übergang zu und von Standardzeit und Sommerzeit Wochentag darstellt.</span><span class="sxs-lookup"><span data-stu-id="13934-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="13934-128">Jahr</span><span class="sxs-lookup"><span data-stu-id="13934-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="13934-129">Verwendet, um eine Zeitzone definiert, die sich je nach dem Jahr ändern.</span><span class="sxs-lookup"><span data-stu-id="13934-129">Used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="13934-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="13934-130">This element is optional.</span></span> <span data-ttu-id="13934-131">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="13934-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="13934-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="13934-132">Parent elements</span></span>

|<span data-ttu-id="13934-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="13934-133">**Element**</span></span>|<span data-ttu-id="13934-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="13934-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="13934-135">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="13934-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="13934-136">Enthält Elemente, die Informationen zur Zeitzone zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="13934-136">Contains elements that identify time zone information.</span></span><br/><br/><span data-ttu-id="13934-137">Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="13934-137">This element also contains information about the transition between standard time and daylight saving time.</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a><span data-ttu-id="13934-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="13934-138">Example</span></span>

<span data-ttu-id="13934-139">Die folgende partielle GetUserAvailability Anforderung stellt eine Clientanwendung an einem Speicherort, der Sommerzeit erkennt.</span><span class="sxs-lookup"><span data-stu-id="13934-139">The following partial GetUserAvailability request represents a client application in a location that recognizes daylight saving time.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="13934-140">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="13934-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="13934-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="13934-141">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="13934-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="13934-142">Schema Name</span></span>  <br/> |<span data-ttu-id="13934-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="13934-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="13934-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="13934-144">Validation File</span></span>  <br/> |<span data-ttu-id="13934-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="13934-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="13934-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="13934-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="13934-147">False</span><span class="sxs-lookup"><span data-stu-id="13934-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="13934-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="13934-148">See also</span></span>

- [<span data-ttu-id="13934-149">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="13934-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="13934-150">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="13934-150">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

