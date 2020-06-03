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
description: Das EndTimeZone-Element definiert die Zeitzone für die Endzeit eines CalendarItem-oder MeetingRequest-Elements.
ms.openlocfilehash: 83ab2ab90e2bed7658fe83ed33a72b60d5f10135
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44462985"
---
# <a name="endtimezone"></a><span data-ttu-id="4900f-103">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="4900f-103">EndTimeZone</span></span>

<span data-ttu-id="4900f-104">Das **EndTimeZone** -Element definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Elements.</span><span class="sxs-lookup"><span data-stu-id="4900f-104">The **EndTimeZone** element defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>
  
```xml
<EndTimeZone Id="" Name="">
   <Periods/>
   <TransitionsGroups/>
   <Transitions/>
</EndTimeZone>
```

 <span data-ttu-id="4900f-105">**TimeZoneDefinitionType**</span><span class="sxs-lookup"><span data-stu-id="4900f-105">**TimeZoneDefinitionType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4900f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4900f-106">Attributes and elements</span></span>

<span data-ttu-id="4900f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4900f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4900f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4900f-108">Attributes</span></span>

|<span data-ttu-id="4900f-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="4900f-109">**Attribute**</span></span>|<span data-ttu-id="4900f-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4900f-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4900f-111">Id</span><span class="sxs-lookup"><span data-stu-id="4900f-111">Id</span></span>  <br/> |<span data-ttu-id="4900f-112">Stellt den eindeutigen Bezeichner der Zeitzonendefinition dar.</span><span class="sxs-lookup"><span data-stu-id="4900f-112">Represents the unique identifier of the time zone definition.</span></span>  <br/> |
|<span data-ttu-id="4900f-113">Name</span><span class="sxs-lookup"><span data-stu-id="4900f-113">Name</span></span>  <br/> |<span data-ttu-id="4900f-114">Stellt den beschreibenden Namen der Zeitzonendefinition dar.</span><span class="sxs-lookup"><span data-stu-id="4900f-114">Represents the descriptive name of the time zone definition.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="4900f-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4900f-115">Child elements</span></span>

|<span data-ttu-id="4900f-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="4900f-116">**Element**</span></span>|<span data-ttu-id="4900f-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4900f-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4900f-118">Zeiten</span><span class="sxs-lookup"><span data-stu-id="4900f-118">Periods</span></span>](periods.md) <br/> |<span data-ttu-id="4900f-119">Stellt ein Array von [Period](period.md) -Elementen dar, die den Zeit Offset in unterschiedlichen Phasen der Zeitzone definieren.</span><span class="sxs-lookup"><span data-stu-id="4900f-119">Represents an array of [Period](period.md) elements that define the time offset at different stages of the time zone.</span></span>  <br/> |
|[<span data-ttu-id="4900f-120">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="4900f-120">TransitionsGroups</span></span>](transitionsgroups.md) <br/> |<span data-ttu-id="4900f-121">Stellt ein Array von [transitiongroup](transitionsgroup.md) -Elementen dar, die Zeit zonenübergänge angeben.</span><span class="sxs-lookup"><span data-stu-id="4900f-121">Represents an array of [TransitionsGroup](transitionsgroup.md) elements that specify time zone transitions.</span></span>  <br/> |
|[<span data-ttu-id="4900f-122">Übergänge</span><span class="sxs-lookup"><span data-stu-id="4900f-122">Transitions</span></span>](transitions.md) <br/> |<span data-ttu-id="4900f-123">Stellt ein Array von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="4900f-123">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4900f-124">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4900f-124">Parent elements</span></span>

|<span data-ttu-id="4900f-125">**Element**</span><span class="sxs-lookup"><span data-stu-id="4900f-125">**Element**</span></span>|<span data-ttu-id="4900f-126">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4900f-126">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4900f-127">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="4900f-127">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="4900f-128">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="4900f-128">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="4900f-129">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="4900f-129">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="4900f-130">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="4900f-130">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4900f-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="4900f-131">Remarks</span></span>

<span data-ttu-id="4900f-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Exchange Server ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="4900f-132">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4900f-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="4900f-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4900f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="4900f-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4900f-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4900f-135">Schema Name</span></span>  <br/> |<span data-ttu-id="4900f-136">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4900f-136">Types schema</span></span>  <br/> |
|<span data-ttu-id="4900f-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4900f-137">Validation File</span></span>  <br/> |<span data-ttu-id="4900f-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4900f-138">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4900f-139">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4900f-139">Can be Empty</span></span>  <br/> |<span data-ttu-id="4900f-140">False</span><span class="sxs-lookup"><span data-stu-id="4900f-140">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4900f-141">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4900f-141">See also</span></span>



- [<span data-ttu-id="4900f-142">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4900f-142">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

