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
description: Das ConflictingMeetings-Element identifiziert alle Kalenderelemente, die mit einer Besprechungszeit in Konflikt stehen.
ms.openlocfilehash: dc897c9dc33117d379d89bb9bb41104ca02def1f
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44460176"
---
# <a name="conflictingmeetings"></a><span data-ttu-id="e0734-103">ConflictingMeetings</span><span class="sxs-lookup"><span data-stu-id="e0734-103">ConflictingMeetings</span></span>

<span data-ttu-id="e0734-104">Das **ConflictingMeetings** -Element identifiziert alle Kalenderelemente, die mit einer Besprechungszeit in Konflikt stehen.</span><span class="sxs-lookup"><span data-stu-id="e0734-104">The **ConflictingMeetings** element identifies all calendar items that conflict with a meeting time.</span></span> 
  
```xml
<ConflictingMeetings>
   <CalendarItem/>
</ConflictingMeetings>
```

 <span data-ttu-id="e0734-105">**NonEmptyArrayOfAllItemsType**</span><span class="sxs-lookup"><span data-stu-id="e0734-105">**NonEmptyArrayOfAllItemsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e0734-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e0734-106">Attributes and elements</span></span>

<span data-ttu-id="e0734-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e0734-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e0734-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e0734-108">Attributes</span></span>

<span data-ttu-id="e0734-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e0734-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e0734-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0734-110">Child elements</span></span>

|<span data-ttu-id="e0734-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0734-111">**Element**</span></span>|<span data-ttu-id="e0734-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0734-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0734-113">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e0734-113">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e0734-114">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="e0734-114">Represents an Exchange calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e0734-115">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e0734-115">Parent elements</span></span>

|<span data-ttu-id="e0734-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="e0734-116">**Element**</span></span>|<span data-ttu-id="e0734-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e0734-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e0734-118">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="e0734-118">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="e0734-119">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="e0734-119">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="e0734-120">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="e0734-120">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="e0734-121">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="e0734-121">Represents an Exchange calendar item.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e0734-122">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e0734-122">Remarks</span></span>

<span data-ttu-id="e0734-123">Wenn dieses Element verwendet wird, muss es ein oder mehrere untergeordnete Elemente enthalten.</span><span class="sxs-lookup"><span data-stu-id="e0734-123">If this element is used, it must contain one or more child elements.</span></span>
  
<span data-ttu-id="e0734-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="e0734-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0734-125">Obwohl zusätzliche untergeordnete Elemente pro Schema gültig sind, ist das [CalendarItem](calendaritem.md) -Element das einzige untergeordnete Element, das Exchange-Webdienste innerhalb des **ConflictingMeetings** -Elements zurückgibt.</span><span class="sxs-lookup"><span data-stu-id="e0734-125">Although additional child elements are valid per the schema, the [CalendarItem](calendaritem.md) element is the only child element that Exchange Web Services (EWS) will return within the **ConflictingMeetings** element.</span></span> <span data-ttu-id="e0734-126">In diesem Thema werden keine untergeordneten Elemente aufgeführt, die für das Schema gültig sind, aber nicht von EWS zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="e0734-126">This topic does not list child elements that are valid per the schema but will not be returned by EWS.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="e0734-127">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e0734-127">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0734-128">Namespace</span><span class="sxs-lookup"><span data-stu-id="e0734-128">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e0734-129">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e0734-129">Schema Name</span></span>  <br/> |<span data-ttu-id="e0734-130">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e0734-130">Types schema</span></span>  <br/> |
|<span data-ttu-id="e0734-131">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e0734-131">Validation File</span></span>  <br/> |<span data-ttu-id="e0734-132">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e0734-132">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e0734-133">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e0734-133">Can be Empty</span></span>  <br/> |<span data-ttu-id="e0734-134">False</span><span class="sxs-lookup"><span data-stu-id="e0734-134">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0734-135">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e0734-135">See also</span></span>



- [<span data-ttu-id="e0734-136">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e0734-136">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

