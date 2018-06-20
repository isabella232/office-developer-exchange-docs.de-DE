---
title: TransitionsGroups
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- TransitionsGroups
api_type:
- schema
ms.assetid: ad0849f8-5158-4a23-9c36-a49f5be1d1e1
description: Das TransitionsGroups-Element stellt ein Array von Zeitzone Übergang Gruppen.
ms.openlocfilehash: 546dd3c96187bf9f1ebf574b37b689e26e3af997
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19839264"
---
# <a name="transitionsgroups"></a><span data-ttu-id="05385-103">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="05385-103">TransitionsGroups</span></span>

<span data-ttu-id="05385-104">Das **TransitionsGroups** -Element stellt ein Array von Zeitzone Übergang Gruppen.</span><span class="sxs-lookup"><span data-stu-id="05385-104">The **TransitionsGroups** element represents an array of time zone transition groups.</span></span> 
  
```XML
<TransitionsGroups>
   <TransitionsGroup/>
</TransitionsGroups>
```

 <span data-ttu-id="05385-105">**ArrayOfTransitionsGroupsType**</span><span class="sxs-lookup"><span data-stu-id="05385-105">**ArrayOfTransitionsGroupsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="05385-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="05385-106">Attributes and elements</span></span>

<span data-ttu-id="05385-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="05385-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="05385-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="05385-108">Attributes</span></span>

<span data-ttu-id="05385-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="05385-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="05385-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05385-110">Child elements</span></span>

|<span data-ttu-id="05385-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="05385-111">**Element**</span></span>|<span data-ttu-id="05385-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05385-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05385-113">TransitionsGroup</span><span class="sxs-lookup"><span data-stu-id="05385-113">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="05385-114">Stellt ein Array von Zeitzone Übergänge.</span><span class="sxs-lookup"><span data-stu-id="05385-114">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="05385-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="05385-115">Parent elements</span></span>

|<span data-ttu-id="05385-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="05385-116">**Element**</span></span>|<span data-ttu-id="05385-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="05385-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="05385-118">StartTimeZone-Zeitzone</span><span class="sxs-lookup"><span data-stu-id="05385-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="05385-119">Definiert die Zeitzone für die Startzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="05385-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="05385-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="05385-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="05385-121">Definiert die Zeitzone für die Endzeit eines [CalendarItem](calendaritem.md) oder [MeetingRequest](meetingrequest.md).</span><span class="sxs-lookup"><span data-stu-id="05385-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="05385-122">Zeitzonendefinition</span><span class="sxs-lookup"><span data-stu-id="05385-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="05385-123">Definiert eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="05385-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="05385-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="05385-124">Remarks</span></span>

<span data-ttu-id="05385-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="05385-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="05385-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="05385-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="05385-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="05385-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="05385-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="05385-128">Schema Name</span></span>  <br/> |<span data-ttu-id="05385-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="05385-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="05385-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="05385-130">Validation File</span></span>  <br/> |<span data-ttu-id="05385-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="05385-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="05385-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="05385-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="05385-133">False</span><span class="sxs-lookup"><span data-stu-id="05385-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="05385-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="05385-134">See also</span></span>



- [<span data-ttu-id="05385-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="05385-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

