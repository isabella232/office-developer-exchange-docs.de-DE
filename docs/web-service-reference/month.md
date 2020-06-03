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
description: Das Month-Element stellt den Übergangs Monat des Jahres in und aus Standardzeit und Sommerzeit dar.
ms.openlocfilehash: f102dca4ed9e833b9742844cfd612c81dfd05e70
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468621"
---
# <a name="month"></a><span data-ttu-id="a4999-103">Monat</span><span class="sxs-lookup"><span data-stu-id="a4999-103">Month</span></span>

<span data-ttu-id="a4999-104">Das **Month** -Element stellt den Übergangs Monat des Jahres in und aus Standardzeit und Sommerzeit dar.</span><span class="sxs-lookup"><span data-stu-id="a4999-104">The **Month** element represents the transition month of the year to and from standard time and daylight saving time.</span></span> 
  
```xml
<Month>...</Month>
```

 <span data-ttu-id="a4999-105">**Kurz**</span><span class="sxs-lookup"><span data-stu-id="a4999-105">**Short**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a4999-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a4999-106">Attributes and elements</span></span>

<span data-ttu-id="a4999-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a4999-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a4999-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a4999-108">Attributes</span></span>

<span data-ttu-id="a4999-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4999-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a4999-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4999-110">Child elements</span></span>

<span data-ttu-id="a4999-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a4999-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a4999-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a4999-112">Parent elements</span></span>

|<span data-ttu-id="a4999-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="a4999-113">**Element**</span></span>|<span data-ttu-id="a4999-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a4999-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a4999-115">Standard Time</span><span class="sxs-lookup"><span data-stu-id="a4999-115">StandardTime</span></span>](standardtime.md) <br/> | <span data-ttu-id="a4999-116">Stellt einen Offset von der Zeit relativ zur koordinierten Weltzeit (Coordinated Universal Time, UTC) dar, dargestellt durch das Element [Bias (UTC)](bias-utc.md) .</span><span class="sxs-lookup"><span data-stu-id="a4999-116">Represents an offset from the time relative to Coordinated Universal Time (UTC) represented by the [Bias (UTC)](bias-utc.md) element.</span></span> <span data-ttu-id="a4999-117">Dieses Element enthält auch Informationen zum Übergang zur Standardzeit von Sommerzeit in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="a4999-117">This element also contains information about the transition to standard time from daylight saving time in regions where daylight saving time is observed.</span></span> <br/> <br/>  <span data-ttu-id="a4999-118">Im folgenden finden Sie die XPath-Ausdrücke für das [Standard](standardtime.md) Time-Element:</span><span class="sxs-lookup"><span data-stu-id="a4999-118">The following are the XPath expressions to the [StandardTime](standardtime.md) element:</span></span> <br/> <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/StandardTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/StandardTime` <br/> |
|[<span data-ttu-id="a4999-119">DaylightTime</span><span class="sxs-lookup"><span data-stu-id="a4999-119">DaylightTime</span></span>](daylighttime.md) <br/> | <span data-ttu-id="a4999-120">Stellt einen Offset von der Zeit relativ zu UTC dar, dargestellt durch das [Bias-Element (UTC)](bias-utc.md) in Regionen, in denen die Sommerzeit beobachtet wird.</span><span class="sxs-lookup"><span data-stu-id="a4999-120">Represents an offset from the time relative to UTC represented by the [Bias (UTC)](bias-utc.md) element in regions where daylight saving time is observed.</span></span> <span data-ttu-id="a4999-121">Dieses Element enthält auch Informationen darüber, wann der Übergang zur Sommerzeit aus der Standardzeit erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a4999-121">This element also contains information about when the transition to daylight saving time from standard time occurs.</span></span>  <br/><br/>  <span data-ttu-id="a4999-122">Im folgenden finden Sie die XPath-Ausdrücke für das [Daylight](daylighttime.md) -Element:</span><span class="sxs-lookup"><span data-stu-id="a4999-122">The following are the XPath expressions to the [DaylightTime](daylighttime.md) element:</span></span>  <br/> <br/> `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone/DaylightTime` <br/><br/>  `/GetUserAvailabilityRequest/TimeZone/DaylightTime` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a4999-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="a4999-123">Text value</span></span>

<span data-ttu-id="a4999-124">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a4999-124">A text value is required.</span></span> <span data-ttu-id="a4999-125">Der Wert stellt den Ordnungs Rang des Monats nach dem Vorkommen dar und muss eine Zahl zwischen 1 und 12 sein.</span><span class="sxs-lookup"><span data-stu-id="a4999-125">The value represents the ordinal rank of the month by occurrence and must be a number between 1 and 12.</span></span> <span data-ttu-id="a4999-126">Dies ist ein kurzer Integer-Datentyp.</span><span class="sxs-lookup"><span data-stu-id="a4999-126">This is a short integer data type.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a4999-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a4999-127">Remarks</span></span>

<span data-ttu-id="a4999-128">Ein [Standard](standardtime.md) Time-Element, das ein [DayOrder](dayorder.md) -Element mit dem Wert 5, einem **Month** -Element mit dem Wert 10 und einem DayOfWeek-Element [(TimeZone)](dayofweek-timezone.md) enthält, das den Wert "Sunday" aufweist, bedeutet, dass der Übergang von Standardzeit zu Sommerzeit am fünften Sonntag des zehnten Monats erfolgt.</span><span class="sxs-lookup"><span data-stu-id="a4999-128">A [StandardTime](standardtime.md) element that contains a [DayOrder](dayorder.md) element that has a value of 5, a **Month** element that has a value of 10, and a [DayOfWeek (TimeZone)](dayofweek-timezone.md) element that has a value of Sunday means that the transition from standard time to daylight saving time occurs on the fifth Sunday of the tenth month.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="a4999-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a4999-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a4999-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="a4999-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a4999-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a4999-131">Schema Name</span></span>  <br/> |<span data-ttu-id="a4999-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a4999-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="a4999-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a4999-133">Validation File</span></span>  <br/> |<span data-ttu-id="a4999-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a4999-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a4999-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a4999-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="a4999-136">False</span><span class="sxs-lookup"><span data-stu-id="a4999-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a4999-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a4999-137">See also</span></span>

- [<span data-ttu-id="a4999-138">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="a4999-138">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="a4999-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="a4999-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

