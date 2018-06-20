---
title: Übergänge
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Transitions
api_type:
- schema
ms.assetid: 26f38f1c-96a3-440e-805c-1437886d11c5
description: Übergänge-Element stellt ein Array von Zeitzone Übergänge.
ms.openlocfilehash: df7cacdef71c3fdfaa3ecadb486843ea30e6109d
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839259"
---
# <a name="transitions"></a><span data-ttu-id="9e711-103">Übergänge</span><span class="sxs-lookup"><span data-stu-id="9e711-103">Transitions</span></span>

<span data-ttu-id="9e711-104">**Übergänge** -Element stellt ein Array von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="9e711-104">The **Transitions** element represents an array of time zone transitions.</span></span> 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 <span data-ttu-id="9e711-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="9e711-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9e711-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9e711-106">Attributes and elements</span></span>

<span data-ttu-id="9e711-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9e711-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9e711-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9e711-108">Attributes</span></span>

|<span data-ttu-id="9e711-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="9e711-109">**Attribute**</span></span>|<span data-ttu-id="9e711-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e711-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9e711-111">Id</span><span class="sxs-lookup"><span data-stu-id="9e711-111">Id</span></span>  <br/> |<span data-ttu-id="9e711-112">Den eindeutigen Bezeichner der Zeitzonendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="9e711-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="9e711-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e711-113">Child elements</span></span>

|<span data-ttu-id="9e711-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e711-114">**Element**</span></span>|<span data-ttu-id="9e711-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e711-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e711-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="9e711-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="9e711-117">Stellt einen Zeitzone Übergang, die einem bestimmten Datum und zu einem bestimmten Zeitpunkt dar.</span><span class="sxs-lookup"><span data-stu-id="9e711-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="9e711-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="9e711-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="9e711-119">Stellt einen Zeitzone Übergang dar, bei dem gleichen Tag pro Jahr auftritt.</span><span class="sxs-lookup"><span data-stu-id="9e711-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="9e711-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="9e711-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="9e711-121">Stellt einen Zeitzone Übergang, der auftritt, an einem angegebenen Tag des Jahres dar.</span><span class="sxs-lookup"><span data-stu-id="9e711-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="9e711-122">Übergang</span><span class="sxs-lookup"><span data-stu-id="9e711-122">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="9e711-123">Stellt einen Zeitzone Übergang dar.</span><span class="sxs-lookup"><span data-stu-id="9e711-123">Represents a time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9e711-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9e711-124">Parent elements</span></span>

|<span data-ttu-id="9e711-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="9e711-125">**Element**</span></span>|<span data-ttu-id="9e711-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9e711-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9e711-127">StartTimeZone-Zeitzone</span><span class="sxs-lookup"><span data-stu-id="9e711-127">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="9e711-128">Definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="9e711-128">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="9e711-129">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="9e711-129">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="9e711-130">Definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="9e711-130">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="9e711-131">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="9e711-131">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="9e711-132">Definiert eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="9e711-132">Defines a time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="9e711-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="9e711-133">Text value</span></span>

<span data-ttu-id="9e711-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="9e711-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="9e711-135">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9e711-135">Remarks</span></span>

<span data-ttu-id="9e711-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="9e711-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9e711-137">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9e711-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9e711-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="9e711-138">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9e711-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9e711-139">Schema Name</span></span>  <br/> |<span data-ttu-id="9e711-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9e711-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="9e711-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9e711-141">Validation File</span></span>  <br/> |<span data-ttu-id="9e711-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9e711-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9e711-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9e711-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="9e711-144">False</span><span class="sxs-lookup"><span data-stu-id="9e711-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9e711-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9e711-145">See also</span></span>



- [<span data-ttu-id="9e711-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9e711-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

