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
description: Das TransitionsGroups-Element stellt ein Array von Zeit Zonen Übergangs Gruppen dar.
ms.openlocfilehash: 35244e122ee31045359afd0833459bbb94fd0aa1
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44467410"
---
# <a name="transitionsgroups"></a><span data-ttu-id="3b5c4-103">TransitionsGroups</span><span class="sxs-lookup"><span data-stu-id="3b5c4-103">TransitionsGroups</span></span>

<span data-ttu-id="3b5c4-104">Das **TransitionsGroups** -Element stellt ein Array von Zeit Zonen Übergangs Gruppen dar.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-104">The **TransitionsGroups** element represents an array of time zone transition groups.</span></span> 
  
```XML
<TransitionsGroups>
   <TransitionsGroup/>
</TransitionsGroups>
```

 <span data-ttu-id="3b5c4-105">**ArrayOfTransitionsGroupsType**</span><span class="sxs-lookup"><span data-stu-id="3b5c4-105">**ArrayOfTransitionsGroupsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="3b5c4-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="3b5c4-106">Attributes and elements</span></span>

<span data-ttu-id="3b5c4-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="3b5c4-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="3b5c4-108">Attributes</span></span>

<span data-ttu-id="3b5c4-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="3b5c4-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b5c4-110">Child elements</span></span>

|<span data-ttu-id="3b5c4-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b5c4-111">**Element**</span></span>|<span data-ttu-id="3b5c4-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b5c4-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b5c4-113">Transitiongroup</span><span class="sxs-lookup"><span data-stu-id="3b5c4-113">TransitionsGroup</span></span>](transitionsgroup.md) <br/> |<span data-ttu-id="3b5c4-114">Stellt ein Array von Zeit Zonen Übergängen dar.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-114">Represents an array of time zone transitions.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="3b5c4-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="3b5c4-115">Parent elements</span></span>

|<span data-ttu-id="3b5c4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="3b5c4-116">**Element**</span></span>|<span data-ttu-id="3b5c4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="3b5c4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="3b5c4-118">StartTimeZone</span><span class="sxs-lookup"><span data-stu-id="3b5c4-118">StartTimeZone</span></span>](starttimezone.md) <br/> |<span data-ttu-id="3b5c4-119">Definiert die Zeitzone für die Startzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Start Zeit.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-119">Defines the time zone for the start time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="3b5c4-120">EndTimeZone</span><span class="sxs-lookup"><span data-stu-id="3b5c4-120">EndTimeZone</span></span>](endtimezone.md) <br/> |<span data-ttu-id="3b5c4-121">Definiert die Zeitzone für die Endzeit einer [CalendarItem](calendaritem.md) -oder [MeetingRequest](meetingrequest.md)-Datei.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-121">Defines the time zone for the end time of a [CalendarItem](calendaritem.md) or [MeetingRequest](meetingrequest.md).</span></span>  <br/> |
|[<span data-ttu-id="3b5c4-122">TimeZoneDefinition</span><span class="sxs-lookup"><span data-stu-id="3b5c4-122">TimeZoneDefinition</span></span>](timezonedefinition.md) <br/> |<span data-ttu-id="3b5c4-123">Definiert eine Zeitzone.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-123">Defines a time zone.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="3b5c4-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="3b5c4-124">Remarks</span></span>

<span data-ttu-id="3b5c4-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="3b5c4-125">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="3b5c4-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="3b5c4-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3b5c4-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="3b5c4-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="3b5c4-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="3b5c4-128">Schema Name</span></span>  <br/> |<span data-ttu-id="3b5c4-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="3b5c4-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="3b5c4-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="3b5c4-130">Validation File</span></span>  <br/> |<span data-ttu-id="3b5c4-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="3b5c4-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="3b5c4-132">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="3b5c4-132">Can be Empty</span></span>  <br/> |<span data-ttu-id="3b5c4-133">False</span><span class="sxs-lookup"><span data-stu-id="3b5c4-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3b5c4-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="3b5c4-134">See also</span></span>



- [<span data-ttu-id="3b5c4-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="3b5c4-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

