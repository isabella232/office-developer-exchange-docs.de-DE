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
description: Das Transitions-Element stellt ein Array von Zeit Zonen Übergängen dar.
ms.openlocfilehash: d48fb8872b2f7e052f733c32e5dd1c9b4d04d898
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467438"
---
# <a name="transitions"></a><span data-ttu-id="679b2-103">Übergänge</span><span class="sxs-lookup"><span data-stu-id="679b2-103">Transitions</span></span>

<span data-ttu-id="679b2-104">Das **Transitions** -Element stellt ein Array von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="679b2-104">The **Transitions** element represents an array of time zone transitions.</span></span> 
  
```xml
<Transitions Id="">
   <Transition/>
   <AbsoluteDateTransition/>
   <RecurringDayTransition/>
   <RecurringDateTransition/>
</Transitions>
```

 <span data-ttu-id="679b2-105">**ArrayOfTransitionsType**</span><span class="sxs-lookup"><span data-stu-id="679b2-105">**ArrayOfTransitionsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="679b2-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="679b2-106">Attributes and elements</span></span>

<span data-ttu-id="679b2-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="679b2-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="679b2-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="679b2-108">Attributes</span></span>

|<span data-ttu-id="679b2-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="679b2-109">**Attribute**</span></span>|<span data-ttu-id="679b2-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="679b2-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="679b2-111">Id</span><span class="sxs-lookup"><span data-stu-id="679b2-111">Id</span></span>  <br/> |<span data-ttu-id="679b2-112">Stellt den eindeutigen Bezeichner der Zeitzonendefinition dar.</span><span class="sxs-lookup"><span data-stu-id="679b2-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="679b2-113">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="679b2-113">Child elements</span></span>

|<span data-ttu-id="679b2-114">**Element**</span><span class="sxs-lookup"><span data-stu-id="679b2-114">**Element**</span></span>|<span data-ttu-id="679b2-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="679b2-115">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="679b2-116">AbsoluteDateTransition</span><span class="sxs-lookup"><span data-stu-id="679b2-116">AbsoluteDateTransition</span></span>](absolutedatetransition.md) <br/> |<span data-ttu-id="679b2-117">Stellt einen Zeitzonenübergang dar, der zu einem bestimmten Datum und zu einem bestimmten Zeitpunkt erfolgt.</span><span class="sxs-lookup"><span data-stu-id="679b2-117">Represents a time zone transition that occurs on a specific date and at a specific time.</span></span>  <br/> |
|[<span data-ttu-id="679b2-118">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="679b2-118">RecurringDayTransition</span></span>](recurringdaytransition.md) <br/> |<span data-ttu-id="679b2-119">Stellt einen Zeitzonenübergang dar, der an demselben Tag jedes Jahr erfolgt.</span><span class="sxs-lookup"><span data-stu-id="679b2-119">Represents a time zone transition that occurs on the same day each year.</span></span>  <br/> |
|[<span data-ttu-id="679b2-120">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="679b2-120">RecurringDateTransition</span></span>](recurringdatetransition.md) <br/> |<span data-ttu-id="679b2-121">Stellt einen Zeitzonenübergang dar, der an einem angegebenen Tag des Jahres erfolgt.</span><span class="sxs-lookup"><span data-stu-id="679b2-121">Represents a time zone transition that occurs on a specified day of the year.</span></span>  <br/> |
|[<span data-ttu-id="679b2-122">Übergang</span><span class="sxs-lookup"><span data-stu-id="679b2-122">Transition</span></span>](transition.md) <br/> |<span data-ttu-id="679b2-123">Stellt einen Zeitzonenübergang dar.</span><span class="sxs-lookup"><span data-stu-id="679b2-123">Represents a time zone transition.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="679b2-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="679b2-124">Parent elements</span></span>

|<span data-ttu-id="679b2-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="679b2-125">**Element**</span></span>|<span data-ttu-id="679b2-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="679b2-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="679b2-127">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="679b2-127">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="679b2-128">Definiert die Zeitzone für die Startzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Start Zeit.</span><span class="sxs-lookup"><span data-stu-id="679b2-128">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="679b2-129">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="679b2-129">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="679b2-130">Definiert die Zeitzone für die Endzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Datei.</span><span class="sxs-lookup"><span data-stu-id="679b2-130">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="679b2-131">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="679b2-131">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="679b2-132">Definiert eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="679b2-132">Defines a time zone.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="679b2-133">Textwert</span><span class="sxs-lookup"><span data-stu-id="679b2-133">Text value</span></span>

<span data-ttu-id="679b2-134">Keine.</span><span class="sxs-lookup"><span data-stu-id="679b2-134">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="679b2-135">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="679b2-135">Remarks</span></span>

<span data-ttu-id="679b2-136">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="679b2-136">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="679b2-137">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="679b2-137">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="679b2-138">Namespace</span><span class="sxs-lookup"><span data-stu-id="679b2-138">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="679b2-139">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="679b2-139">Schema Name</span></span>  <br/> |<span data-ttu-id="679b2-140">Schematypen</span><span class="sxs-lookup"><span data-stu-id="679b2-140">Types schema</span></span>  <br/> |
|<span data-ttu-id="679b2-141">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="679b2-141">Validation File</span></span>  <br/> |<span data-ttu-id="679b2-142">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="679b2-142">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="679b2-143">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="679b2-143">Can be Empty</span></span>  <br/> |<span data-ttu-id="679b2-144">False</span><span class="sxs-lookup"><span data-stu-id="679b2-144">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="679b2-145">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="679b2-145">See also</span></span>



- [<span data-ttu-id="679b2-146">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="679b2-146">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

