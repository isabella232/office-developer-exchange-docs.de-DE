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
description: Das RecurringDayTransition-Element stellt einen Zeitzone Übergang, der am gleichen Tag pro Jahr auftritt, dar.
ms.openlocfilehash: 913345188547ce9903809fdc1cbbbe3e20ae7f36
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831012"
---
# <a name="recurringdaytransition"></a><span data-ttu-id="9d746-103">RecurringDayTransition</span><span class="sxs-lookup"><span data-stu-id="9d746-103">RecurringDayTransition</span></span>

<span data-ttu-id="9d746-104">Das **RecurringDayTransition** -Element stellt einen Zeitzone Übergang, der am gleichen Tag pro Jahr auftritt, dar.</span><span class="sxs-lookup"><span data-stu-id="9d746-104">The **RecurringDayTransition** element represents a time zone transition that occurs on the same day each year.</span></span> 
  
```xml
<RecurringDayTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <DayOfWeek/>
   <Occurrence/>
</RecurringDayTransition>
```

 <span data-ttu-id="9d746-105">**RecurringDayTransitionType**</span><span class="sxs-lookup"><span data-stu-id="9d746-105">**RecurringDayTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="9d746-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="9d746-106">Attributes and elements</span></span>

<span data-ttu-id="9d746-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="9d746-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="9d746-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="9d746-108">Attributes</span></span>

<span data-ttu-id="9d746-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="9d746-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="9d746-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d746-110">Child elements</span></span>

|<span data-ttu-id="9d746-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d746-111">**Element**</span></span>|<span data-ttu-id="9d746-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d746-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d746-113">To</span><span class="sxs-lookup"><span data-stu-id="9d746-113">To</span></span>](to.md) <br/> |<span data-ttu-id="9d746-114">Gibt den [Zeitraum](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.</span><span class="sxs-lookup"><span data-stu-id="9d746-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="9d746-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="9d746-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="9d746-116">Stellt den Offset für die Dauer von koordinierte Weltzeit (UTC) für den Übergang zur Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="9d746-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="9d746-117">Monat (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="9d746-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="9d746-118">Stellt den Monat, in dem der Übergang zur Zeitzone auftritt.</span><span class="sxs-lookup"><span data-stu-id="9d746-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="9d746-119">DayOfWeek (TimeZone)</span><span class="sxs-lookup"><span data-stu-id="9d746-119">DayOfWeek (TimeZone)</span></span>](dayofweek-timezone.md) <br/> |<span data-ttu-id="9d746-120">Stellt den Tag der Woche auf der erfolgt der Übergang zur Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="9d746-120">Represents the day of the week on which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="9d746-121">Vorkommen (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="9d746-121">Occurrence (Time Zone Transition)</span></span>](occurrence-time-zone-transition.md) <br/> |<span data-ttu-id="9d746-122">Stellt das Vorkommen des Tags der Woche des Monats, der der Übergang zur Zeitzone auftritt.</span><span class="sxs-lookup"><span data-stu-id="9d746-122">Represents the occurrence of the day of the week in the month that the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="9d746-123">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="9d746-123">Parent elements</span></span>

|<span data-ttu-id="9d746-124">**Element**</span><span class="sxs-lookup"><span data-stu-id="9d746-124">**Element**</span></span>|<span data-ttu-id="9d746-125">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="9d746-125">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="9d746-126">Übergänge</span><span class="sxs-lookup"><span data-stu-id="9d746-126">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="9d746-127">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="9d746-127">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="9d746-128">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="9d746-128">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="9d746-129">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="9d746-129">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="9d746-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="9d746-130">Remarks</span></span>

<span data-ttu-id="9d746-131">Einen Übergang, der am zweiten Dienstag Februar jährlich auftritt, ist ein Beispiel für einen Übergang Zeitzone, der durch das [RecurringDayTransition](recurringdaytransition.md) -Element dargestellt werden könnte.</span><span class="sxs-lookup"><span data-stu-id="9d746-131">An example of a time zone transition that could be represented by the [RecurringDayTransition](recurringdaytransition.md) element is a transition that occurs on the second Tuesday of February each year.</span></span> 
  
<span data-ttu-id="9d746-132">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="9d746-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="9d746-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="9d746-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9d746-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="9d746-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="9d746-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="9d746-135">Schema Name</span></span>  <br/> |<span data-ttu-id="9d746-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="9d746-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="9d746-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="9d746-137">Validation File</span></span>  <br/> |<span data-ttu-id="9d746-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="9d746-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="9d746-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="9d746-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="9d746-140">False</span><span class="sxs-lookup"><span data-stu-id="9d746-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9d746-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="9d746-141">See also</span></span>



- [<span data-ttu-id="9d746-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="9d746-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

