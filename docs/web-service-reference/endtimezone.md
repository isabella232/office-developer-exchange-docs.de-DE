---
title: EndTimeZone
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeZone
api_type:
- schema
ms.assetid: 6c53c337-be60-4d22-9e9e-a0c140c5e913
description: Das EndTimeZone-Element definiert die Zeitzone für die Endzeit eines CalendarItem oder MeetingRequest.
ms.openlocfilehash: 65eeedcc7c4d0e616ae54d4e2545fd310e9ad905
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758241"
---
# <a name="endtimezone"></a><span data-ttu-id="55efd-103">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="55efd-103">EndTimeZone</span></span>

<span data-ttu-id="55efd-104">Das **EndTimeZone** -Element definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="55efd-104">The **EndTimeZone** element defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<EndTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</EndTimeZone>
```

 <span data-ttu-id="55efd-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="55efd-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="55efd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="55efd-106">Attributes and elements</span></span>

<span data-ttu-id="55efd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="55efd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="55efd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="55efd-108">Attributes</span></span>

|<span data-ttu-id="55efd-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="55efd-109">**Attribute**</span></span>|<span data-ttu-id="55efd-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55efd-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="55efd-111">Id</span><span class="sxs-lookup"><span data-stu-id="55efd-111">Id</span></span>  <br/> |<span data-ttu-id="55efd-112">Den eindeutigen Bezeichner der Zeitzonendefinition darstellt.</span><span class="sxs-lookup"><span data-stu-id="55efd-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="55efd-113">Name</span><span class="sxs-lookup"><span data-stu-id="55efd-113">Name</span></span>  <br/> |<span data-ttu-id="55efd-114">Der beschreibende Name der Definition der Zeitzone darstellt.</span><span class="sxs-lookup"><span data-stu-id="55efd-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="55efd-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55efd-115">Child elements</span></span>

|<span data-ttu-id="55efd-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="55efd-116">**Element**</span></span>|<span data-ttu-id="55efd-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55efd-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55efd-118">Perioden</span><span class="sxs-lookup"><span data-stu-id="55efd-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="55efd-119">Stellt ein Array von [Periode](period.md) -Elementen, die den Uhrzeit-Offset in verschiedenen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="55efd-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="55efd-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="55efd-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="55efd-121">Stellt ein Array von [TransitionsGroup](transitionsgroup.md) -Elementen, die Zeitzone Übergänge angeben.</span><span class="sxs-lookup"><span data-stu-id="55efd-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="55efd-122">Übergänge</span><span class="sxs-lookup"><span data-stu-id="55efd-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="55efd-123">Stellt ein Array von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="55efd-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="55efd-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="55efd-124">Parent elements</span></span>

|<span data-ttu-id="55efd-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="55efd-125">**Element**</span></span>|<span data-ttu-id="55efd-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="55efd-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="55efd-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="55efd-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="55efd-128">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="55efd-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="55efd-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="55efd-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="55efd-130">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="55efd-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55efd-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="55efd-131">Remarks</span></span>

<span data-ttu-id="55efd-132">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="55efd-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="55efd-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="55efd-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55efd-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="55efd-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="55efd-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="55efd-135">Schema Name</span></span>  <br/> |<span data-ttu-id="55efd-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="55efd-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="55efd-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="55efd-137">Validation File</span></span>  <br/> |<span data-ttu-id="55efd-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="55efd-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="55efd-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="55efd-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="55efd-140">False</span><span class="sxs-lookup"><span data-stu-id="55efd-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55efd-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="55efd-141">See also</span></span>



- [<span data-ttu-id="55efd-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="55efd-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

