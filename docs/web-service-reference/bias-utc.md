---
title: Bias (UTC)
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
ms.assetid: 15790d5a-5134-457b-8f2b-d9dee1f807a2
description: Bias-Element stellt den allgemeinen Offset von koordinierte Weltzeit (UTC). Dieser Wert wird in Minuten angegeben.
ms.openlocfilehash: 43613593565ca15be97bd2a98dbe5c512dbe5fc7
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757443"
---
# <a name="bias-utc"></a><span data-ttu-id="f57ce-104">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="f57ce-104">Bias (UTC)</span></span>

<span data-ttu-id="f57ce-105">**Bias** -Element stellt den allgemeinen Offset von koordinierte Weltzeit (UTC).</span><span class="sxs-lookup"><span data-stu-id="f57ce-105">The **Bias** element represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="f57ce-106">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="f57ce-106">This value is in minutes.</span></span> 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

<span data-ttu-id="f57ce-107">**int**</span><span class="sxs-lookup"><span data-stu-id="f57ce-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="f57ce-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f57ce-108">Attributes and elements</span></span>

<span data-ttu-id="f57ce-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f57ce-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f57ce-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="f57ce-110">Attributes</span></span>

<span data-ttu-id="f57ce-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="f57ce-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f57ce-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f57ce-112">Child elements</span></span>

<span data-ttu-id="f57ce-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="f57ce-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="f57ce-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f57ce-114">Parent elements</span></span>

|<span data-ttu-id="f57ce-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="f57ce-115">**Element**</span></span>|<span data-ttu-id="f57ce-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f57ce-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f57ce-117">TimeZone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="f57ce-117">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="f57ce-118">Der Container, der die Datum-Uhrzeit-Informationen der Anforderung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f57ce-118">The container that identifies the date-time information of the request.</span></span> <span data-ttu-id="f57ce-119">Dieses Element enthält Informationen über den Wechsel zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="f57ce-119">This element contains information about the transition between standard time and daylight saving time.</span></span>  <br/><br/><span data-ttu-id="f57ce-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="f57ce-120">The following are the XPath expressions to this element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="f57ce-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="f57ce-121">Text value</span></span>

<span data-ttu-id="f57ce-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="f57ce-122">A text value is required.</span></span> <span data-ttu-id="f57ce-123">Der Textwert stellt eine ganze Zahl.</span><span class="sxs-lookup"><span data-stu-id="f57ce-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="f57ce-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="f57ce-124">Remarks</span></span>

<span data-ttu-id="f57ce-125">Ein zweites [Bias](bias.md) -Element im Schema stellt den Offset vom Offset (Coordinated Universal Time, UTC).</span><span class="sxs-lookup"><span data-stu-id="f57ce-125">A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f57ce-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="f57ce-126">Example</span></span>

<span data-ttu-id="f57ce-127">Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von 8 Stunden aus UTC in die Clientanwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="f57ce-127">The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="f57ce-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="f57ce-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f57ce-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="f57ce-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f57ce-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f57ce-130">Schema Name</span></span>  <br/> |<span data-ttu-id="f57ce-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f57ce-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="f57ce-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f57ce-132">Validation File</span></span>  <br/> |<span data-ttu-id="f57ce-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f57ce-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f57ce-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="f57ce-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="f57ce-135">False</span><span class="sxs-lookup"><span data-stu-id="f57ce-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f57ce-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f57ce-136">See also</span></span>

- [<span data-ttu-id="f57ce-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="f57ce-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="f57ce-138">Bias</span><span class="sxs-lookup"><span data-stu-id="f57ce-138">Bias</span></span>](bias.md)
- [<span data-ttu-id="f57ce-139">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="f57ce-139">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

