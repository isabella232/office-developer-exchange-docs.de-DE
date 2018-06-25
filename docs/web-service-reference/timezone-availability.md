---
title: TimeZone (Verfügbarkeit)
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
description: TimeZone-Element enthält Elemente, die Informationen zur Zeitzone zu identifizieren. Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.
ms.openlocfilehash: dc2466e8039819edc82294ff05f1746ada64cb43
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839229"
---
# <a name="timezone-availability"></a><span data-ttu-id="1c852-104">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="1c852-104">TimeZone (Availability)</span></span>

<span data-ttu-id="1c852-105">**TimeZone** -Element enthält Elemente, die Informationen zur Zeitzone zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="1c852-105">The **TimeZone** element contains elements that identify time zone information.</span></span> <span data-ttu-id="1c852-106">Dieses Element enthält auch Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="1c852-106">This element also contains information about the transition between standard time and daylight saving time.</span></span> 
  
```xml
<TimeZone>
   <Bias/>
   <StandardTime/>
   <DaylightTime/>
</TimeZone>
```

 <span data-ttu-id="1c852-107">**SerializableTimeZone**</span><span class="sxs-lookup"><span data-stu-id="1c852-107">**SerializableTimeZone**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="1c852-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1c852-108">Attributes and elements</span></span>

<span data-ttu-id="1c852-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1c852-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1c852-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="1c852-110">Attributes</span></span>

<span data-ttu-id="1c852-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="1c852-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="1c852-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c852-112">Child elements</span></span>

|<span data-ttu-id="1c852-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c852-113">**Element**</span></span>|<span data-ttu-id="1c852-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c852-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c852-115">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="1c852-115">Bias (UTC)</span></span>](bias-utc.md) <br/> |<span data-ttu-id="1c852-116">Stellt den allgemeinen Offset von koordinierte Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="1c852-116">Represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="1c852-117">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="1c852-117">This value is in minutes.</span></span>  <br/> |
|[<span data-ttu-id="1c852-118">StandardTime</span><span class="sxs-lookup"><span data-stu-id="1c852-118">StandardTime</span></span>](standardtime.md) <br/> |<span data-ttu-id="1c852-119">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="1c852-119">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="1c852-120">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="1c852-120">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span>  <br/> |
|[<span data-ttu-id="1c852-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="1c852-121">DaylightTime</span></span>](daylighttime.md) <br/> |<span data-ttu-id="1c852-122">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="1c852-122">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="1c852-123">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="1c852-123">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1c852-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1c852-124">Parent elements</span></span>

|<span data-ttu-id="1c852-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="1c852-125">**Element**</span></span>|<span data-ttu-id="1c852-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1c852-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1c852-127">GetUserAvailabilityRequest</span><span class="sxs-lookup"><span data-stu-id="1c852-127">GetUserAvailabilityRequest</span></span>](getuseravailabilityrequest.md) <br/> |<span data-ttu-id="1c852-128">Enthält die Argumente, die zum Abrufen von Informationen zur Verfügbarkeit der Benutzer verwendet.</span><span class="sxs-lookup"><span data-stu-id="1c852-128">Contains the arguments used to obtain user availability information.</span></span> <span data-ttu-id="1c852-129">Dies ist eine Stammelements.</span><span class="sxs-lookup"><span data-stu-id="1c852-129">This is a root element.</span></span>  <br/> <span data-ttu-id="1c852-130">Das **TimeZone** -Element in der Nachricht GetUserAvailabilityRequest stellt die Zeitzone, in dem die DateTime-Werte in der Anforderung angegeben werden.</span><span class="sxs-lookup"><span data-stu-id="1c852-130">The **TimeZone** element in the GetUserAvailabilityRequest message represents the time zone in which the DateTime values in the request are specified.</span></span> <span data-ttu-id="1c852-131">Die von den Verfügbarkeitsdienst zurückgegebenen DateTime-Werte sind auch in dieser Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="1c852-131">The DateTime values returned by the Availability service are also in this time zone.</span></span>  <br/> <span data-ttu-id="1c852-132">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1c852-132">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityRequest` <br/> |
|[<span data-ttu-id="1c852-133">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="1c852-133">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="1c852-134">Stellt die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="1c852-134">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="1c852-135">**TimeZone** -Element in der Nachricht GetUserAvailabilityResponse stellt die Einstellungen der Zeitzone des angeforderten Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="1c852-135">The **TimeZone** element in the GetUserAvailabilityResponse message represents the time zone settings of the requested mailbox user.</span></span>  <br/> <span data-ttu-id="1c852-136">Es folgt der XPath-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="1c852-136">The following is the XPath to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1c852-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1c852-137">Remarks</span></span>

<span data-ttu-id="1c852-138">Dieses Element ist im [GetUserAvailabilityRequest](getuseravailabilityrequest.md) -Element erforderlich.</span><span class="sxs-lookup"><span data-stu-id="1c852-138">This element is required in the [GetUserAvailabilityRequest](getuseravailabilityrequest.md) element.</span></span> <span data-ttu-id="1c852-139">Dieses Element wird höchstens einmal oder wenn das übergeordnete Element ist mindestens Male [WorkingHours](workinghours-ex15websvcsotherref.md) -Element.</span><span class="sxs-lookup"><span data-stu-id="1c852-139">This element occurs at most once or at least zero times when the parent element is the [WorkingHours](workinghours-ex15websvcsotherref.md) element.</span></span> 
  
## <a name="example"></a><span data-ttu-id="1c852-140">Beispiel</span><span class="sxs-lookup"><span data-stu-id="1c852-140">Example</span></span>

<span data-ttu-id="1c852-141">Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von UTC von 8 Stunden in der Clientanwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="1c852-141">The following example shows part of an XML request that identifies an offset from UTC of 8 hours in the client application.</span></span>
  
```XML
<TimeZone xmlns="http://schemas.microsoft.com/exchange/services/2006/types">
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

## <a name="element-information"></a><span data-ttu-id="1c852-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1c852-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1c852-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="1c852-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1c852-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1c852-144">Schema Name</span></span>  <br/> |<span data-ttu-id="1c852-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1c852-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="1c852-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1c852-146">Validation File</span></span>  <br/> |<span data-ttu-id="1c852-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1c852-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1c852-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1c852-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="1c852-149">False</span><span class="sxs-lookup"><span data-stu-id="1c852-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1c852-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1c852-150">See also</span></span>



[<span data-ttu-id="1c852-151">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="1c852-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="1c852-152">Bias</span><span class="sxs-lookup"><span data-stu-id="1c852-152">Bias</span></span>](bias.md)


[<span data-ttu-id="1c852-153">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="1c852-153">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

