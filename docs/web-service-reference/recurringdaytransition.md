---
title: RecurringDayTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDayTransition
api_type:
- schema
ms.assetid: 1ae28d14-c2b8-4084-9e76-e2e347a884ce
description: Das RecurringDayTransition-Element stellt einen Zeitzonenübergang dar, der jedes Jahr am gleichen Tag erfolgt.
ms.openlocfilehash: 44c2a6ec4dbaaa52a2772cb5c35a84b14dd77f97
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44468467"
---
# <a name="recurringdaytransition"></a><span data-ttu-id="d219c-103">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="d219c-103">RecurringDayTransition</span></span>

<span data-ttu-id="d219c-104">Das **RecurringDayTransition** -Element stellt einen Zeitzonenübergang dar, der jedes Jahr am gleichen Tag erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d219c-104">The **RecurringDayTransition** element represents a time zone transition that occurs on the same day each year.</span></span> 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 <span data-ttu-id="d219c-105">**RecurringDayTransitionType**</span><span class="sxs-lookup"><span data-stu-id="d219c-105">**RecurringDayTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d219c-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d219c-106">Attributes and elements</span></span>

<span data-ttu-id="d219c-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d219c-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d219c-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d219c-108">Attributes</span></span>

<span data-ttu-id="d219c-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d219c-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d219c-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d219c-110">Child elements</span></span>

|<span data-ttu-id="d219c-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d219c-111">**Element**</span></span>|<span data-ttu-id="d219c-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d219c-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d219c-113">To</span><span class="sxs-lookup"><span data-stu-id="d219c-113">To</span></span>](to.md) <br/> |<span data-ttu-id="d219c-114">Gibt den [Zeitraum](period.md) oder die [Transitions](transitionsgroup.md) an, der das Ziel des Zeit Zonen Übergangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="d219c-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="d219c-115">Offset</span><span class="sxs-lookup"><span data-stu-id="d219c-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="d219c-116">Stellt den Offset für die Dauer der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitzonenübergang dar.</span><span class="sxs-lookup"><span data-stu-id="d219c-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="d219c-117">Month (Zeitzonenübergang)</span><span class="sxs-lookup"><span data-stu-id="d219c-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="d219c-118">Stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d219c-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="d219c-119">DayOfWeek (Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="d219c-119">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="d219c-120">Stellt den Wochentag dar, an dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d219c-120">Represents the day of the week on which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="d219c-121">Vorkommen (Zeitzonenübergang)</span><span class="sxs-lookup"><span data-stu-id="d219c-121">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="d219c-122">Stellt das Vorkommen des Wochentags in dem Monat dar, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="d219c-122">Represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d219c-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d219c-123">Parent elements</span></span>

|<span data-ttu-id="d219c-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="d219c-124">**Element**</span></span>|<span data-ttu-id="d219c-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d219c-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d219c-126">Übergänge</span><span class="sxs-lookup"><span data-stu-id="d219c-126">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="d219c-127">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="d219c-127">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="d219c-128">Transitiongroup</span><span class="sxs-lookup"><span data-stu-id="d219c-128">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="d219c-129">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="d219c-129">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d219c-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d219c-130">Remarks</span></span>

<span data-ttu-id="d219c-131">Ein Beispiel für einen Zeitzonenübergang, der durch das [RecurringDayTransition](recurringdaytransition.md) -Element dargestellt werden kann, ist ein Übergang, der jedes Jahr am zweiten Dienstag im Februar stattfindet.</span><span class="sxs-lookup"><span data-stu-id="d219c-131">An example of a time zone transition that could be represented by the [RecurringDayTransition](recurringdaytransition.md) element is a transition that occurs on the second Tuesday of February each year.</span></span> 
  
<span data-ttu-id="d219c-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="d219c-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d219c-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d219c-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d219c-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d219c-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d219c-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d219c-135">Schema Name</span></span>  <br/> |<span data-ttu-id="d219c-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d219c-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="d219c-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d219c-137">Validation File</span></span>  <br/> |<span data-ttu-id="d219c-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d219c-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d219c-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d219c-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="d219c-140">False</span><span class="sxs-lookup"><span data-stu-id="d219c-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d219c-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d219c-141">See also</span></span>



- [<span data-ttu-id="d219c-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d219c-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

