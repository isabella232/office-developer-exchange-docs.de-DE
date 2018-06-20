---
title: StartTimeZone-Zeitzone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeZone
api_type:
- schema
ms.assetid: d38c4dc1-4ecb-42a1-8d57-a451b16a2de2
description: Das StartTimeZone-Element definiert die Zeitzone für die Startzeit eines CalendarItem oder MeetingRequest.
ms.openlocfilehash: 6d21869c4b3be048db27dcc9f128fff868aebcb5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831559"
---
# <a name="starttimezone"></a><span data-ttu-id="1fb3e-103">StartTimeZone-Zeitzone</span><span class="sxs-lookup"><span data-stu-id="1fb3e-103">StartTimeZone</span></span>

<span data-ttu-id="1fb3e-104">Das **StartTimeZone** -Element definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="1fb3e-104">The **StartTimeZone** element defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

<span data-ttu-id="1fb3e-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-105">**TimeZoneDefinitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="1fb3e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb3e-106">Attributes and elements</span></span>

<span data-ttu-id="1fb3e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="1fb3e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="1fb3e-108">Attributes</span></span>

|<span data-ttu-id="1fb3e-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-109">**Attribute**</span></span>|<span data-ttu-id="1fb3e-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="1fb3e-111">Id</span><span class="sxs-lookup"><span data-stu-id="1fb3e-111">Id</span></span>  <br/> |<span data-ttu-id="1fb3e-112">Den eindeutigen Bezeichner der Zeitzonendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="1fb3e-113">Name</span><span class="sxs-lookup"><span data-stu-id="1fb3e-113">Name</span></span>  <br/> |<span data-ttu-id="1fb3e-114">Der beschreibende Name der Definition der Zeitzone darstellt.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="1fb3e-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb3e-115">Child elements</span></span>

|<span data-ttu-id="1fb3e-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-116">**Element**</span></span>|<span data-ttu-id="1fb3e-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1fb3e-118">Perioden</span><span class="sxs-lookup"><span data-stu-id="1fb3e-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="1fb3e-119">Stellt ein Array von [Periode](period.md) -Elementen, die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="1fb3e-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="1fb3e-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="1fb3e-121">Stellt ein Array von [TransitionsGroup](transitionsgroup.md) -Elementen, die Zeitzone Übergänge angeben.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="1fb3e-122">Übergänge</span><span class="sxs-lookup"><span data-stu-id="1fb3e-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="1fb3e-123">Stellt ein Array von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="1fb3e-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="1fb3e-124">Parent elements</span></span>

|<span data-ttu-id="1fb3e-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-125">**Element**</span></span>|<span data-ttu-id="1fb3e-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="1fb3e-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="1fb3e-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="1fb3e-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="1fb3e-128">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="1fb3e-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="1fb3e-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="1fb3e-130">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="1fb3e-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="1fb3e-131">Remarks</span></span>

<span data-ttu-id="1fb3e-132">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="1fb3e-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="1fb3e-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="1fb3e-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="1fb3e-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="1fb3e-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="1fb3e-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="1fb3e-135">Schema Name</span></span>  <br/> |<span data-ttu-id="1fb3e-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="1fb3e-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="1fb3e-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="1fb3e-137">Validation File</span></span>  <br/> |<span data-ttu-id="1fb3e-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="1fb3e-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="1fb3e-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="1fb3e-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="1fb3e-140">False</span><span class="sxs-lookup"><span data-stu-id="1fb3e-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1fb3e-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="1fb3e-141">See also</span></span>

- [<span data-ttu-id="1fb3e-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="1fb3e-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

