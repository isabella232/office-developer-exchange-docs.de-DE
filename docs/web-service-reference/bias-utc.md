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
description: Das Bias-Element stellt den allgemeinen Offset von koordinierter Weltzeit (Coordinated Universal Time, UTC) dar. Dieser Wert wird in Minuten angegeben.
ms.openlocfilehash: d95284aa28e59542d1a1ee40686163138b015702
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460246"
---
# <a name="bias-utc"></a><span data-ttu-id="038e9-104">Bias (UTC)</span><span class="sxs-lookup"><span data-stu-id="038e9-104">Bias (UTC)</span></span>

<span data-ttu-id="038e9-105">Das **Bias** -Element stellt den allgemeinen Offset von koordinierter Weltzeit (Coordinated Universal Time, UTC) dar.</span><span class="sxs-lookup"><span data-stu-id="038e9-105">The **Bias** element represents the general offset from Coordinated Universal Time (UTC).</span></span> <span data-ttu-id="038e9-106">Dieser Wert wird in Minuten angegeben.</span><span class="sxs-lookup"><span data-stu-id="038e9-106">This value is in minutes.</span></span> 
  
```xml
<TimeZone>
   <Bias>int</Bias>
</TimeZone>
```

<span data-ttu-id="038e9-107">**int**</span><span class="sxs-lookup"><span data-stu-id="038e9-107">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="038e9-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="038e9-108">Attributes and elements</span></span>

<span data-ttu-id="038e9-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="038e9-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="038e9-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="038e9-110">Attributes</span></span>

<span data-ttu-id="038e9-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="038e9-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="038e9-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="038e9-112">Child elements</span></span>

<span data-ttu-id="038e9-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="038e9-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="038e9-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="038e9-114">Parent elements</span></span>

|<span data-ttu-id="038e9-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="038e9-115">**Element**</span></span>|<span data-ttu-id="038e9-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="038e9-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="038e9-117">Zeitzone (Verfügbarkeit)</span><span class="sxs-lookup"><span data-stu-id="038e9-117">TimeZone (Availability)</span></span>](timezone-availability.md) <br/> | <span data-ttu-id="038e9-118">Der Container, der die Datum-Uhrzeit-Informationen der Anforderung angibt.</span><span class="sxs-lookup"><span data-stu-id="038e9-118">The container that identifies the date-time information of the request.</span></span> <span data-ttu-id="038e9-119">Dieses Element enthält Informationen über den Übergang zwischen Standardzeit und Sommerzeit.</span><span class="sxs-lookup"><span data-stu-id="038e9-119">This element contains information about the transition between standard time and daylight saving time.</span></span>  <br/><br/><span data-ttu-id="038e9-120">Folgende XPath-Ausdrücke werden für dieses Element verwendet:</span><span class="sxs-lookup"><span data-stu-id="038e9-120">The following are the XPath expressions to this element:</span></span><br/><br/>   `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/TimeZone` <br/><br/>`/GetUserAvailabilityRequest/TimeZone` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="038e9-121">Textwert</span><span class="sxs-lookup"><span data-stu-id="038e9-121">Text value</span></span>

<span data-ttu-id="038e9-122">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="038e9-122">A text value is required.</span></span> <span data-ttu-id="038e9-123">Der Wert Text stellt eine ganze Zahl dar.</span><span class="sxs-lookup"><span data-stu-id="038e9-123">The text value represents an integer.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="038e9-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="038e9-124">Remarks</span></span>

<span data-ttu-id="038e9-125">Ein zweites [Bias](bias.md) -Element im Schema stellt den Offset des Offsets für koordinierte Weltzeit (Coordinated Universal Time, UTC) dar.</span><span class="sxs-lookup"><span data-stu-id="038e9-125">A second [Bias](bias.md) element in the schema represents the offset from the Coordinated Universal Time (UTC) offset.</span></span> 
  
## <a name="example"></a><span data-ttu-id="038e9-126">Beispiel</span><span class="sxs-lookup"><span data-stu-id="038e9-126">Example</span></span>

<span data-ttu-id="038e9-127">Das folgende Beispiel zeigt einen Teil einer XML-Anforderung, die einen Offset von 8 Stunden von UTC in der Clientanwendung identifiziert.</span><span class="sxs-lookup"><span data-stu-id="038e9-127">The following example shows part of an XML request that identifies an offset of 8 hours from UTC on the client application.</span></span>
  
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

## <a name="element-information"></a><span data-ttu-id="038e9-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="038e9-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="038e9-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="038e9-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="038e9-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="038e9-130">Schema Name</span></span>  <br/> |<span data-ttu-id="038e9-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="038e9-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="038e9-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="038e9-132">Validation File</span></span>  <br/> |<span data-ttu-id="038e9-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="038e9-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="038e9-134">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="038e9-134">Can be Empty</span></span>  <br/> |<span data-ttu-id="038e9-135">False</span><span class="sxs-lookup"><span data-stu-id="038e9-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="038e9-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="038e9-136">See also</span></span>

- [<span data-ttu-id="038e9-137">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="038e9-137">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="038e9-138">Bias</span><span class="sxs-lookup"><span data-stu-id="038e9-138">Bias</span></span>](bias.md)
- [<span data-ttu-id="038e9-139">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="038e9-139">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

