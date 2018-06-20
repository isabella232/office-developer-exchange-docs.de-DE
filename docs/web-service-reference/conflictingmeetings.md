---
title: ConflictingMeetings
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ConflictingMeetings
api_type:
- schema
ms.assetid: cfff7a11-7b3a-4995-9815-afedd45ebb0f
description: Das ConflictingMeetings-Element identifiziert alle Kalenderelemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.
ms.openlocfilehash: 1d2558dba41ec3e7ae2711bb2dc26f54cada827a
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757596"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="87768-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="87768-103">ConflictingMeetings</span></span>

<span data-ttu-id="87768-104">Das **ConflictingMeetings** -Element identifiziert alle Kalenderelemente, die mit einem bestimmten Zeitpunkt treffen in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="87768-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="87768-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="87768-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="87768-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="87768-106">Attributes and elements</span></span>

<span data-ttu-id="87768-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="87768-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="87768-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="87768-108">Attributes</span></span>

<span data-ttu-id="87768-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="87768-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="87768-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87768-110">Child elements</span></span>

|<span data-ttu-id="87768-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="87768-111">**Element**</span></span>|<span data-ttu-id="87768-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87768-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87768-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="87768-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="87768-114">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="87768-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="87768-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="87768-115">Parent elements</span></span>

|<span data-ttu-id="87768-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="87768-116">**Element**</span></span>|<span data-ttu-id="87768-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="87768-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="87768-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="87768-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="87768-119">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="87768-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="87768-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="87768-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="87768-121">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="87768-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="87768-122">Hinweise</span><span class="sxs-lookup"><span data-stu-id="87768-122">Remarks</span></span>

<span data-ttu-id="87768-123">Wenn dieses Element verwendet wird, muss es einen oder mehrere untergeordnete Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="87768-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="87768-124">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="87768-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="87768-125">Obwohl weitere untergeordnete Elemente pro das Schema gültig sind, ist das [CalendarItem](calendaritem.md) -Element das einzige untergeordnete Element, bei dem Exchange-Webdienste (EWS) innerhalb des Elements **ConflictingMeetings** zurückgegeben wird.</span><span class="sxs-lookup"><span data-stu-id="87768-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="87768-126">In diesem Thema wird keine untergeordneten Elemente aufgelistet, die dem Schema gültig sind, aber nicht von EWS zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="87768-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="87768-127">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="87768-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="87768-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="87768-128">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="87768-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="87768-129">Schema Name</span></span>  <br/> |<span data-ttu-id="87768-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="87768-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="87768-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="87768-131">Validation File</span></span>  <br/> |<span data-ttu-id="87768-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="87768-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="87768-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="87768-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="87768-134">False</span><span class="sxs-lookup"><span data-stu-id="87768-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87768-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="87768-135">See also</span></span>



- [<span data-ttu-id="87768-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="87768-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

