---
title: Zeitzone (Verfügbarkeit)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TimeZone
api_type:
- schema
ms.assetid: d662ffae-1f93-4c08-85a4-c69de2f7c681
description: Das TimeZone-Element enthält Elemente, die Zeitzoneninformationen identifizieren. Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.
ms.openlocfilehash: ba4b0a4805dba54450e01e89c5e9ef746404b716
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460274"
---
# <a name="timezone-availability"></a><span data-ttu-id="46092-104">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="46092-104">TimeZone (Availability)</span></span>

<span data-ttu-id="46092-105">Das **TimeZone** -Element enthält Elemente, die Zeitzoneninformationen identifizieren.</span><span class="sxs-lookup"><span data-stu-id="46092-105">The **TimeZone** element contains elements that identify time zone information.</span></span> <span data-ttu-id="46092-106">Dieses Element enthält auch Informationen zum Übergang zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="46092-106">This element also contains information about the transition between standard time and daylight saving time.</span></span> 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 <span data-ttu-id="46092-107">**SerializableTimeZone**</span><span class="sxs-lookup"><span data-stu-id="46092-107">**SerializableTimeZone**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="46092-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="46092-108">Attributes and elements</span></span>

<span data-ttu-id="46092-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="46092-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="46092-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="46092-110">Attributes</span></span>

<span data-ttu-id="46092-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="46092-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="46092-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46092-112">Child elements</span></span>

|<span data-ttu-id="46092-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="46092-113">**Element**</span></span>|<span data-ttu-id="46092-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46092-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46092-115">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="46092-115">Bias (UTC)</span></span>](bias-utc.md) <br/> |<span data-ttu-id="46092-116">Stellt den allgemeinen Offset von koordinierter Weltzeit (Coordinated Universal Time, UTC) dar.</span><span class="sxs-lookup"><span data-stu-id="46092-116">Represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="46092-117">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="46092-117">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="46092-118">Standard Time</span><span class="sxs-lookup"><span data-stu-id="46092-118">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="46092-119">Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="46092-119">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="46092-120">Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="46092-120">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/> |
|[<span data-ttu-id="46092-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="46092-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="46092-122">Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="46092-122">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="46092-123">Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="46092-123">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="46092-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="46092-124">Parent elements</span></span>

|<span data-ttu-id="46092-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="46092-125">**Element**</span></span>|<span data-ttu-id="46092-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="46092-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="46092-127">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="46092-127">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="46092-128">Enthält die Argumente, die zum Abrufen von Informationen zur Benutzerverfügbarkeit verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="46092-128">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="46092-129">Dies ist ein Stammelement.</span><span class="sxs-lookup"><span data-stu-id="46092-129">This is a root element.</span></span>  <br/> <span data-ttu-id="46092-130">Das **TimeZone** -Element in der GetUserAvailabilityRequest-Nachricht stellt die Zeitzone dar, in der die DateTime-Werte in der Anforderung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="46092-130">The **TimeZone** element in the GetUserAvailabilityRequest message represents the time zone in which the DateTime values in the request are specified.</span></span> <span data-ttu-id="46092-131">Die vom Verfügbarkeitsdienst zurückgegebenen DateTime-Werte befinden sich ebenfalls in dieser Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="46092-131">The DateTime values returned by the Availability service are also in this time zone.</span></span>  <br/> <span data-ttu-id="46092-132">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="46092-132">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[<span data-ttu-id="46092-133">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="46092-133">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="46092-134">Stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="46092-134">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="46092-135">Das **TimeZone** -Element in der GetUserAvailabilityResponse-Nachricht stellt die Zeitzoneneinstellungen des angeforderten Postfachbenutzers dar.</span><span class="sxs-lookup"><span data-stu-id="46092-135">The **TimeZone** element in the GetUserAvailabilityResponse message represents the time zone settings of the requested mailbox user.</span></span>  <br/> <span data-ttu-id="46092-136">Es folgt der XPath für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="46092-136">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46092-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="46092-137">Remarks</span></span>

<span data-ttu-id="46092-138">Dieses Element ist im [GetUserAvailabilityRequest](getuseravailabilityrequest.md) -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="46092-138">This element is required in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) element.</span></span> <span data-ttu-id="46092-139">Dieses Element tritt höchstens einmal oder mindestens null mal auf, wenn das übergeordnete Element das [WorkingHours](workinghours-ex15websvcsotherref.md) -Element ist.</span><span class="sxs-lookup"><span data-stu-id="46092-139">This element occurs at most once or at least zero times when the parent element is the [WorkingHours](workinghours-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="46092-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="46092-140">Example</span></span>

<span data-ttu-id="46092-141">Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von einer UTC von 8 Stunden in der Clientanwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="46092-141">The following example shows part of an XML request that identifies an offset from UTC of 8 hours in the client application.</span></span>
  
```XML
<TimeZone xmlns="https://schemas.microsoft.com/exchange/services/2006/types">
  <Bias>480</Bias>
  <StandardTime>
    <Bias>0</Bias>
    <Time>02:00:00</Time>
    <DayOrder>1</DayOrder>
    <Month>11</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </StandardTime>
  <DaylightTime>
    <Bias>-60</Bias>
    <Time>02:00:00</Time>
    <DayOrder>2</DayOrder>
    <Month>3</Month>
    <DayOfWeek>Sunday</DayOfWeek>
  </DaylightTime>
</TimeZone>
```

## <a name="element-information"></a><span data-ttu-id="46092-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="46092-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="46092-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="46092-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="46092-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="46092-144">Schema Name</span></span>  <br/> |<span data-ttu-id="46092-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="46092-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="46092-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="46092-146">Validation File</span></span>  <br/> |<span data-ttu-id="46092-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="46092-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="46092-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="46092-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="46092-149">False</span><span class="sxs-lookup"><span data-stu-id="46092-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="46092-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="46092-150">See also</span></span>



[<span data-ttu-id="46092-151">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="46092-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="46092-152">Bias</span><span class="sxs-lookup"><span data-stu-id="46092-152">Bias</span></span>](bias.md)


[<span data-ttu-id="46092-153">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="46092-153">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

