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
description: Das RecurringDateTransition-Element stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum auftritt.
ms.openlocfilehash: 2acbd3afb50a92d4e4f3d7b552eecb36fe59be8b
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44461576"
---
# <a name="recurringdatetransition"></a><span data-ttu-id="8d70a-103">RecurringDateTransition</span><span class="sxs-lookup"><span data-stu-id="8d70a-103">RecurringDateTransition</span></span>

<span data-ttu-id="8d70a-104">Das **RecurringDateTransition** -Element stellt einen Zeitzonenübergang dar, der jedes Jahr an einem bestimmten Datum auftritt.</span><span class="sxs-lookup"><span data-stu-id="8d70a-104">The **RecurringDateTransition** element represents a time zone transition that occurs on a specific date each year.</span></span> 
  
```xml
<RecurringDateTransition>
   <To/>
   <TimeOffset/>
   <Month/>
   <Day/>
</RecurringDateTransition>
```

 <span data-ttu-id="8d70a-105">**RecurringDateTransitionType**</span><span class="sxs-lookup"><span data-stu-id="8d70a-105">**RecurringDateTransitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="8d70a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d70a-106">Attributes and elements</span></span>

<span data-ttu-id="8d70a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d70a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d70a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d70a-108">Attributes</span></span>

<span data-ttu-id="8d70a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d70a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d70a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d70a-110">Child elements</span></span>

|<span data-ttu-id="8d70a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d70a-111">**Element**</span></span>|<span data-ttu-id="8d70a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d70a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d70a-113">To</span><span class="sxs-lookup"><span data-stu-id="8d70a-113">To</span></span>](to.md) <br/> |<span data-ttu-id="8d70a-114">Gibt den [Zeitraum](period.md) oder die [Transitions](transitionsgroup.md) an, der das Ziel des Zeit Zonen Übergangs darstellt.</span><span class="sxs-lookup"><span data-stu-id="8d70a-114">Specifies the [Period](period.md) or [TransitionsGroup](transitionsgroup.md) that is the target of the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="8d70a-115">Offset</span><span class="sxs-lookup"><span data-stu-id="8d70a-115">TimeOffset</span></span>](timeoffset.md) <br/> |<span data-ttu-id="8d70a-116">Stellt den Offset für die Dauer der koordinierten Weltzeit (Coordinated Universal Time, UTC) für den Zeitzonenübergang dar.</span><span class="sxs-lookup"><span data-stu-id="8d70a-116">Represents the duration offset from Coordinated Universal Time (UTC) for the time zone transition.</span></span>  <br/> |
|[<span data-ttu-id="8d70a-117">Month (Zeitzonenübergang)</span><span class="sxs-lookup"><span data-stu-id="8d70a-117">Month (Time Zone Transition)</span></span>](month-time-zone-transition.md) <br/> |<span data-ttu-id="8d70a-118">Stellt den Monat dar, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="8d70a-118">Represents the month in which the time zone transition occurs.</span></span>  <br/> |
|[<span data-ttu-id="8d70a-119">Day</span><span class="sxs-lookup"><span data-stu-id="8d70a-119">Day</span></span>](day.md) <br/> |<span data-ttu-id="8d70a-120">Stellt den Tag des Monats dar, in dem der Zeitzonenübergang erfolgt.</span><span class="sxs-lookup"><span data-stu-id="8d70a-120">Represents the day of the month on which the time zone transition occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8d70a-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d70a-121">Parent elements</span></span>

|<span data-ttu-id="8d70a-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d70a-122">**Element**</span></span>|<span data-ttu-id="8d70a-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d70a-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d70a-124">Übergänge</span><span class="sxs-lookup"><span data-stu-id="8d70a-124">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="8d70a-125">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="8d70a-125">Represents a collection of time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="8d70a-126">Transitiongroup</span><span class="sxs-lookup"><span data-stu-id="8d70a-126">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="8d70a-127">Stellt eine Auflistung von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="8d70a-127">Represents a collection of time zone transitions.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d70a-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d70a-128">Remarks</span></span>

<span data-ttu-id="8d70a-129">Ein Beispiel für einen Zeitzonenübergang, der durch das [RecurringDateTransition](recurringdatetransition.md) -Element dargestellt werden kann, ist ein Übergang, der jedes Jahr am 15. März stattfindet.</span><span class="sxs-lookup"><span data-stu-id="8d70a-129">An example of a time zone transition that could be represented by the [RecurringDateTransition](recurringdatetransition.md) element is a transition that occurs on March 15 each year.</span></span> 
  
<span data-ttu-id="8d70a-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="8d70a-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d70a-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8d70a-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d70a-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d70a-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d70a-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d70a-133">Schema Name</span></span>  <br/> |<span data-ttu-id="8d70a-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d70a-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d70a-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d70a-135">Validation File</span></span>  <br/> |<span data-ttu-id="8d70a-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d70a-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d70a-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="8d70a-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="8d70a-138">False</span><span class="sxs-lookup"><span data-stu-id="8d70a-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d70a-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d70a-139">See also</span></span>



- [<span data-ttu-id="8d70a-140">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8d70a-140">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

