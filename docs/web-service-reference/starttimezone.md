---
title: StartTimeZone
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
description: Das StartTimeZone-Element definiert die Zeitzone für die Startzeit eines CalendarItem-oder MeetingRequest-Elements.
ms.openlocfilehash: fa88f676c0f6a7a2e934f51274942ed3bccbc789
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44458523"
---
# <a name="starttimezone"></a><span data-ttu-id="5a170-103">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="5a170-103">StartTimeZone</span></span>

<span data-ttu-id="5a170-104">Das **StartTimeZone** -Element definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Elements.</span><span class="sxs-lookup"><span data-stu-id="5a170-104">The **StartTimeZone** element defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<StartTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</StartTimeZone>
```

<span data-ttu-id="5a170-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="5a170-105">**TimeZoneDefinitionType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="5a170-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5a170-106">Attributes and elements</span></span>

<span data-ttu-id="5a170-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5a170-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5a170-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5a170-108">Attributes</span></span>

|<span data-ttu-id="5a170-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="5a170-109">**Attribute**</span></span>|<span data-ttu-id="5a170-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a170-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5a170-111">Id</span><span class="sxs-lookup"><span data-stu-id="5a170-111">Id</span></span>  <br/> |<span data-ttu-id="5a170-112">Stellt den eindeutigen Bezeichner der Zeitzonendefinition dar.</span><span class="sxs-lookup"><span data-stu-id="5a170-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="5a170-113">Name</span><span class="sxs-lookup"><span data-stu-id="5a170-113">Name</span></span>  <br/> |<span data-ttu-id="5a170-114">Stellt den beschreibenden Namen der Zeitzonendefinition dar.</span><span class="sxs-lookup"><span data-stu-id="5a170-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="5a170-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a170-115">Child elements</span></span>

|<span data-ttu-id="5a170-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a170-116">**Element**</span></span>|<span data-ttu-id="5a170-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a170-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a170-118">Zeiten</span><span class="sxs-lookup"><span data-stu-id="5a170-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="5a170-119">Stellt ein Array von [Period](period.md) -Elementen dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="5a170-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="5a170-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="5a170-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="5a170-121">Stellt ein Array von [transitiongroup](transitionsgroup.md) -Elementen dar, die Zeit zonenübergänge angeben.</span><span class="sxs-lookup"><span data-stu-id="5a170-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="5a170-122">Übergänge</span><span class="sxs-lookup"><span data-stu-id="5a170-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="5a170-123">Stellt ein Array von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="5a170-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="5a170-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5a170-124">Parent elements</span></span>

|<span data-ttu-id="5a170-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="5a170-125">**Element**</span></span>|<span data-ttu-id="5a170-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5a170-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5a170-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="5a170-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="5a170-128">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="5a170-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="5a170-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5a170-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5a170-130">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5a170-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5a170-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="5a170-131">Remarks</span></span>

<span data-ttu-id="5a170-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5a170-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5a170-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="5a170-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5a170-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="5a170-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5a170-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5a170-135">Schema Name</span></span>  <br/> |<span data-ttu-id="5a170-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5a170-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="5a170-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5a170-137">Validation File</span></span>  <br/> |<span data-ttu-id="5a170-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5a170-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5a170-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5a170-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="5a170-140">False</span><span class="sxs-lookup"><span data-stu-id="5a170-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a170-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5a170-141">See also</span></span>

- [<span data-ttu-id="5a170-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5a170-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

