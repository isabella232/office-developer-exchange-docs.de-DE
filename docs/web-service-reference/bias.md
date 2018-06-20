---
title: Bias
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Bias
api_type:
- schema
ms.assetid: ae10aa44-e6d3-483d-a3e6-bb9c45966810
description: Bias-Element stellt den Offset vom Offset (Coordinated Universal Time, UTC) vom für Standardzeit und Sommerzeit Bias (UTC)-Element identifiziert. Dieser Wert wird in Minuten angegeben.
ms.openlocfilehash: 770bf97b030ac1293595560bc269f54896e35a15
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757447"
---
# <a name="bias"></a><span data-ttu-id="0d78e-104">Bias</span><span class="sxs-lookup"><span data-stu-id="0d78e-104">Bias</span></span>

<span data-ttu-id="0d78e-105">**Bias** -Element stellt den Offset vom Offset (Coordinated Universal Time, UTC) vom für Standardzeit und Sommerzeit [Bias (UTC)](bias-utc.md) -Element identifiziert.</span><span class="sxs-lookup"><span data-stu-id="0d78e-105">The **Bias** element represents the offset from the Coordinated Universal Time (UTC) offset identified by the [Bias (UTC)](bias-utc.md) element for standard time and daylight saving time.</span></span> <span data-ttu-id="0d78e-106">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="0d78e-106">This value is in minutes.</span></span> 
  
```xml
<Bias>...</Bias>
```

<span data-ttu-id="0d78e-107">**int**</span><span class="sxs-lookup"><span data-stu-id="0d78e-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="0d78e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="0d78e-108">Attributes and elements</span></span>

<span data-ttu-id="0d78e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="0d78e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="0d78e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="0d78e-110">Attributes</span></span>

<span data-ttu-id="0d78e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d78e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="0d78e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d78e-112">Child elements</span></span>

<span data-ttu-id="0d78e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="0d78e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="0d78e-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="0d78e-114">Parent elements</span></span>

|<span data-ttu-id="0d78e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="0d78e-115">**Element**</span></span>|<span data-ttu-id="0d78e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="0d78e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="0d78e-117">StandardTime</span><span class="sxs-lookup"><span data-stu-id="0d78e-117">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="0d78e-118">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="0d78e-118">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="0d78e-119">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="0d78e-119">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span><br/><br/><span data-ttu-id="0d78e-120">Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="0d78e-120">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="0d78e-121">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="0d78e-121">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="0d78e-122">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="0d78e-122">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="0d78e-123">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="0d78e-123">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/><span data-ttu-id="0d78e-124">Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="0d78e-124">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span><br/><br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/> `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="0d78e-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="0d78e-125">Text value</span></span>

<span data-ttu-id="0d78e-126">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="0d78e-126">A text value is required.</span></span> <span data-ttu-id="0d78e-127">Der Textwert stellt eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="0d78e-127">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="0d78e-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="0d78e-128">Remarks</span></span>

<span data-ttu-id="0d78e-129">Der Offset verwendet, um die Ortszeit bestimmen kann nur mithilfe eines der **Bias** Elemente bereitgestellt werden.</span><span class="sxs-lookup"><span data-stu-id="0d78e-129">The offset used to determine the local time can only be provided by one of the **Bias** elements.</span></span> <span data-ttu-id="0d78e-130">Die Summe der Werte von dem Bias-Element zur Verfügung gestellt, durch das [DaylightTime](daylighttime.md) -Element oder das [StandardTime](standardtime.md) -Element plus [Weltzeit (UTC) Bias](bias-utc.md) -Element identifiziert die Ortszeit.</span><span class="sxs-lookup"><span data-stu-id="0d78e-130">The sum of the values of the Bias element provided by the [DaylightTime](daylighttime.md) element or the [StandardTime](standardtime.md) element plus the [Bias (UTC)](bias-utc.md) element identifies the local time.</span></span> 
  
## <a name="example"></a><span data-ttu-id="0d78e-131">Beispiel</span><span class="sxs-lookup"><span data-stu-id="0d78e-131">Example</span></span>

<span data-ttu-id="0d78e-132">Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Benutzer, von der wem Sommerzeit angibt durch Anpassen der UTC-Offset von 60 Minuten verwendet.</span><span class="sxs-lookup"><span data-stu-id="0d78e-132">The following example shows part of an XML request that identifies a user who observes daylight saving time by adjusting the offset from UTC by -60 minutes.</span></span> <span data-ttu-id="0d78e-133">Dadurch wird effektiv die Verschiebung 420 Minuten von UTC.</span><span class="sxs-lookup"><span data-stu-id="0d78e-133">This effectively makes the bias 420 minutes from UTC.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="0d78e-134">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="0d78e-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="0d78e-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="0d78e-135">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="0d78e-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="0d78e-136">Schema Name</span></span>  <br/> |<span data-ttu-id="0d78e-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="0d78e-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="0d78e-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="0d78e-138">Validation File</span></span>  <br/> |<span data-ttu-id="0d78e-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="0d78e-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="0d78e-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="0d78e-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="0d78e-141">False</span><span class="sxs-lookup"><span data-stu-id="0d78e-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0d78e-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="0d78e-142">See also</span></span>

- [<span data-ttu-id="0d78e-143">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="0d78e-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="0d78e-144">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="0d78e-144">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

