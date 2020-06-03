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
description: Das Daylight-Element stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, die durch das Bias-Element (UTC) in Regionen dargestellt wird, in denen die Sommerzeit eingehaltenwird. Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.
ms.openlocfilehash: 350fcb4ce278f423c62fcc5ecaa160eda71e4a2c
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44455653"
---
# <a name="daylighttime"></a><span data-ttu-id="28c5e-104">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="28c5e-104">DaylightTime</span></span>

<span data-ttu-id="28c5e-105">Das **Daylight** -Element stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, die durch das [Bias-Element (UTC)](bias-utc.md) in Regionen dargestellt wird, in denen die Sommerzeit eingehaltenwird.</span><span class="sxs-lookup"><span data-stu-id="28c5e-105">The **DaylightTime** element represents an offset from the time relative to Coordinated Universal Time (UTC) that is represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="28c5e-106">Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="28c5e-106">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span> 
  
- [<span data-ttu-id="28c5e-107">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="28c5e-107">TimeZone (Availability)</span></span>](timezone-availability.md) 
- [<span data-ttu-id="28c5e-108">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="28c5e-108">DaylightTime</span></span>](daylighttime.md)
  
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

<span data-ttu-id="28c5e-109">**SerializableTimeZoneTime**</span><span class="sxs-lookup"><span data-stu-id="28c5e-109">**SerializableTimeZoneTime**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="28c5e-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="28c5e-110">Attributes and elements</span></span>

<span data-ttu-id="28c5e-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="28c5e-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="28c5e-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="28c5e-112">Attributes</span></span>

<span data-ttu-id="28c5e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="28c5e-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="28c5e-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28c5e-114">Child elements</span></span>

|<span data-ttu-id="28c5e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="28c5e-115">**Element**</span></span>|<span data-ttu-id="28c5e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c5e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28c5e-117">Bias</span><span class="sxs-lookup"><span data-stu-id="28c5e-117">Bias</span></span>](bias.md) <br/> |<span data-ttu-id="28c5e-118">Stellt den Offset vom UTC-Offset dar, der durch das [Bias-Element (UTC)](bias-utc.md) für Standardzeit und Sommerzeit bestimmt wird.</span><span class="sxs-lookup"><span data-stu-id="28c5e-118">Represents the offset from the UTC offset that is identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="28c5e-119">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="28c5e-119">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="28c5e-120">Time</span><span class="sxs-lookup"><span data-stu-id="28c5e-120">Time</span></span>](time.md) <br/> |<span data-ttu-id="28c5e-121">Stellt die Übergangszeit von Tag zu und von Standardzeit und Sommerzeit dar.</span><span class="sxs-lookup"><span data-stu-id="28c5e-121">Represents the transition time of day to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="28c5e-122">DayOrder</span><span class="sxs-lookup"><span data-stu-id="28c5e-122">DayOrder</span></span>](dayorder.md) <br/> |<span data-ttu-id="28c5e-123">Stellt das _n_th Vorkommen des Tags dar, der im [DayOfWeek-Element (TimeZone)](dayofweek-timezone.md) angegeben ist, das das Datum des Übergangs von und zur Standardzeit und zur Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="28c5e-123">Represents the  _n_th occurrence of the day that is specified in the [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that represents the date of transition from and to standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="28c5e-124">Month</span><span class="sxs-lookup"><span data-stu-id="28c5e-124">Month</span></span>](month.md) <br/> |<span data-ttu-id="28c5e-125">Stellt den Übergangs Monat des Jahres zu und von Standardzeit und Sommerzeit dar.</span><span class="sxs-lookup"><span data-stu-id="28c5e-125">Represents the transition month of the year to and from standard time and daylight saving time.</span></span>  <br/> |
|[<span data-ttu-id="28c5e-126">DayOfWeek (Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="28c5e-126">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="28c5e-127">Stellt den Wochentag dar, an dem der Übergang zu und von Standardzeit und Sommerzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="28c5e-127">Represents the day of the week when the transition to and from standard time and daylight saving time occurs.</span></span>  <br/> |
|[<span data-ttu-id="28c5e-128">Jahr</span><span class="sxs-lookup"><span data-stu-id="28c5e-128">Year</span></span>](year.md) <br/> |<span data-ttu-id="28c5e-129">Dient zum Definieren einer Zeitzone, die sich je nach Jahr ändert.</span><span class="sxs-lookup"><span data-stu-id="28c5e-129">Used to define a time zone that changes depending on the year.</span></span> <span data-ttu-id="28c5e-130">Dieses Element ist optional.</span><span class="sxs-lookup"><span data-stu-id="28c5e-130">This element is optional.</span></span> <span data-ttu-id="28c5e-131">Dieses Element wurde in Microsoft Exchange Server 2007 Service Pack 1 (SP1) eingeführt.</span><span class="sxs-lookup"><span data-stu-id="28c5e-131">This element was introduced in Microsoft Exchange Server 2007 Service Pack 1 (SP1).</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="28c5e-132">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="28c5e-132">Parent elements</span></span>

|<span data-ttu-id="28c5e-133">**Element**</span><span class="sxs-lookup"><span data-stu-id="28c5e-133">**Element**</span></span>|<span data-ttu-id="28c5e-134">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="28c5e-134">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="28c5e-135">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="28c5e-135">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="28c5e-136">Enthält Elemente, die Zeitzoneninformationen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="28c5e-136">Contains elements that identify time zone information.</span></span><br/><br/><span data-ttu-id="28c5e-137">Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="28c5e-137">This element also contains information about the transition between standard time and daylight saving time.</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="example"></a><span data-ttu-id="28c5e-138">Beispiel</span><span class="sxs-lookup"><span data-stu-id="28c5e-138">Example</span></span>

<span data-ttu-id="28c5e-139">Die folgende partielle GetUserAvailability-Anforderung stellt eine Clientanwendung an einem Speicherort dar, der die Sommerzeit erkennt.</span><span class="sxs-lookup"><span data-stu-id="28c5e-139">The following partial GetUserAvailability request represents a client application in a location that recognizes daylight saving time.</span></span>
  
```xml
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="28c5e-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="28c5e-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="28c5e-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="28c5e-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="28c5e-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="28c5e-142">Schema Name</span></span>  <br/> |<span data-ttu-id="28c5e-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="28c5e-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="28c5e-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="28c5e-144">Validation File</span></span>  <br/> |<span data-ttu-id="28c5e-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="28c5e-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="28c5e-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="28c5e-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="28c5e-147">False</span><span class="sxs-lookup"><span data-stu-id="28c5e-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="28c5e-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="28c5e-148">See also</span></span>

- [<span data-ttu-id="28c5e-149">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="28c5e-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="28c5e-150">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="28c5e-150">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

