---
title: Monat
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Month
api_type:
- schema
ms.assetid: b12ac64f-b230-4573-be05-c86a428c4965
description: Month-Element stellt den Übergang Monat des Jahres zu und von Standardzeit und Sommerzeit einer Zeitzone.
ms.openlocfilehash: 73d052ef16bc51cd574eb8b04e21546f97347258
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830476"
---
# <a name="month"></a><span data-ttu-id="cb088-103">Monat</span><span class="sxs-lookup"><span data-stu-id="cb088-103">Month</span></span>

<span data-ttu-id="cb088-104">**Month** -Element stellt den Übergang Monat des Jahres zu und von Standardzeit und Sommerzeit einer Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="cb088-104">The **Month** element represents the transition month of the year to and from standard time and daylight saving time.</span></span> 
  
```xml
<Month>...</Month>
```

 <span data-ttu-id="cb088-105">**Kurze**</span><span class="sxs-lookup"><span data-stu-id="cb088-105">**Short**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cb088-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cb088-106">Attributes and elements</span></span>

<span data-ttu-id="cb088-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cb088-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cb088-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cb088-108">Attributes</span></span>

<span data-ttu-id="cb088-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb088-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cb088-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb088-110">Child elements</span></span>

<span data-ttu-id="cb088-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="cb088-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="cb088-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cb088-112">Parent elements</span></span>

|<span data-ttu-id="cb088-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="cb088-113">**Element**</span></span>|<span data-ttu-id="cb088-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cb088-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cb088-115">StandardTime</span><span class="sxs-lookup"><span data-stu-id="cb088-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="cb088-116">Stellt einen Abstand von dem Zeitpunkt relativ zur koordinierten Weltzeit (UTC) dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="cb088-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="cb088-117">Dieses Element enthält auch Informationen über den Wechsel zur Standardzeit von Sommerzeit Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="cb088-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> <br/> <br/>  <span data-ttu-id="cb088-118">Es folgen die XPath-Ausdrücke auf das [StandardTime](standardtime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="cb088-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="cb088-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="cb088-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="cb088-120">Stellt einen Abstand von dem Zeitpunkt relativ zur UTC, dargestellt durch das Element [Bias (UTC)](bias-utc.md) Regionen, in dem Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="cb088-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="cb088-121">Dieses Element enthält auch Informationen dazu, wann der Übergang von Normalzeit zu Sommerzeit auftritt.</span><span class="sxs-lookup"><span data-stu-id="cb088-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="cb088-122">Es folgen die XPath-Ausdrücke auf das [DaylightTime](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="cb088-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="cb088-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="cb088-123">Text value</span></span>

<span data-ttu-id="cb088-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="cb088-124">A text value is required.</span></span> <span data-ttu-id="cb088-125">Der Wert den ordinalen Rang des Monats darstellt, indem Sie vorkommen und muss eine Zahl zwischen 1 und 12.</span><span class="sxs-lookup"><span data-stu-id="cb088-125">The value represents the ordinal rank of the month by occurrence and must be a number between 1 and 12.</span></span> <span data-ttu-id="cb088-126">Dies ist eine kurze Integer-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="cb088-126">This is a short integer data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="cb088-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cb088-127">Remarks</span></span>

<span data-ttu-id="cb088-128">Ein [StandardTime](standardtime.md) -Element, enthält ein [DayOrder](dayorder.md) -Element, das den Wert 5 hat, ein **Month** -Element, das einen Wert von 10 aufweist und ein [DayOfWeek (TimeZone)](dayofweek-timezone.md) -Element, das den Wert Sonntag hat, bedeutet, dass den Übergang vom Standardzeit Sommerzeit tritt am fünften Sonntag der zehnte Monat.</span><span class="sxs-lookup"><span data-stu-id="cb088-128">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a **Month** element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="cb088-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cb088-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cb088-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="cb088-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cb088-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cb088-131">Schema Name</span></span>  <br/> |<span data-ttu-id="cb088-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cb088-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="cb088-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cb088-133">Validation File</span></span>  <br/> |<span data-ttu-id="cb088-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cb088-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cb088-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cb088-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="cb088-136">False</span><span class="sxs-lookup"><span data-stu-id="cb088-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cb088-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cb088-137">See also</span></span>

- [<span data-ttu-id="cb088-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cb088-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="cb088-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="cb088-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

