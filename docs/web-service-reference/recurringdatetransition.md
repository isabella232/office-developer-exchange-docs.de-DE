---
title: RecurringDateTransition
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurringDateTransition
api_type:
- schema
ms.assetid: 52fe1e05-3c50-40a1-8752-5c3c64c9f1ed
description: Das RecurringDateTransition-Element darstellt, den Übergang einer Zeitzone, der einem bestimmten Datum pro Jahr tritt auf.
ms.openlocfilehash: 7cd8f3452a744e0c9a98fd3698dffb9ed8721a6c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831014"
---
# <a name="recurringdatetransition"></a><span data-ttu-id="ab07e-103">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="ab07e-103">RecurringDateTransition</span></span>

<span data-ttu-id="ab07e-104">Das **RecurringDateTransition** -Element darstellt, den Übergang einer Zeitzone, der einem bestimmten Datum pro Jahr tritt auf.</span><span class="sxs-lookup"><span data-stu-id="ab07e-104">The **RecurringDateTransition** element represents a time zone transition that occurs on a specific date each year.</span></span> 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 <span data-ttu-id="ab07e-105">**RecurringDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="ab07e-105">**RecurringDateTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="ab07e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="ab07e-106">Attributes and elements</span></span>

<span data-ttu-id="ab07e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="ab07e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="ab07e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="ab07e-108">Attributes</span></span>

<span data-ttu-id="ab07e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="ab07e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="ab07e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab07e-110">Child elements</span></span>

|<span data-ttu-id="ab07e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab07e-111">**Element**</span></span>|<span data-ttu-id="ab07e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab07e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab07e-113">To</span><span class="sxs-lookup"><span data-stu-id="ab07e-113">To</span></span>](to.md) <br/> |<span data-ttu-id="ab07e-114">Gibt den [Zeitraum](period.md) oder [TransitionsGroup](transitionsgroup.md) , das das Ziel des Übergangs Zeitzone ist.</span><span class="sxs-lookup"><span data-stu-id="ab07e-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="ab07e-115">TimeOffset</span><span class="sxs-lookup"><span data-stu-id="ab07e-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="ab07e-116">Stellt den Offset für die Dauer von koordinierte Weltzeit (UTC) für den Übergang zur Zeitzone dar.</span><span class="sxs-lookup"><span data-stu-id="ab07e-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="ab07e-117">Monat (Übergang Zeitzone)</span><span class="sxs-lookup"><span data-stu-id="ab07e-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="ab07e-118">Stellt den Monat, in dem der Übergang zur Zeitzone auftritt.</span><span class="sxs-lookup"><span data-stu-id="ab07e-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="ab07e-119">Tag</span><span class="sxs-lookup"><span data-stu-id="ab07e-119">Day</span></span>](day.md) <br/> |<span data-ttu-id="ab07e-120">Stellt den Tag des Monats auf der erfolgt der Übergang zur Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="ab07e-120">Represents the day of the month on which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="ab07e-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="ab07e-121">Parent elements</span></span>

|<span data-ttu-id="ab07e-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="ab07e-122">**Element**</span></span>|<span data-ttu-id="ab07e-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="ab07e-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="ab07e-124">Übergänge</span><span class="sxs-lookup"><span data-stu-id="ab07e-124">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="ab07e-125">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="ab07e-125">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="ab07e-126">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="ab07e-126">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="ab07e-127">Stellt eine Auflistung der Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="ab07e-127">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ab07e-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="ab07e-128">Remarks</span></span>

<span data-ttu-id="ab07e-129">Ein Beispiel für einen Übergang Zeitzone, der durch das [RecurringDateTransition](recurringdatetransition.md) -Element dargestellt werden könnte ist ein Übergang, der 15. März jährlich auftritt.</span><span class="sxs-lookup"><span data-stu-id="ab07e-129">An example of a time zone transition that could be represented by the [RecurringDateTransition](recurringdatetransition.md) element is a transition that occurs on March 15 each year.</span></span> 
  
<span data-ttu-id="ab07e-130">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="ab07e-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="ab07e-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="ab07e-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ab07e-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="ab07e-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="ab07e-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="ab07e-133">Schema Name</span></span>  <br/> |<span data-ttu-id="ab07e-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="ab07e-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="ab07e-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="ab07e-135">Validation File</span></span>  <br/> |<span data-ttu-id="ab07e-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="ab07e-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="ab07e-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="ab07e-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="ab07e-138">False</span><span class="sxs-lookup"><span data-stu-id="ab07e-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab07e-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="ab07e-139">See also</span></span>



- [<span data-ttu-id="ab07e-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="ab07e-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

