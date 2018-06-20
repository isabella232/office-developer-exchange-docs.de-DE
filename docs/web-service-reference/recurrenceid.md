---
title: RecurrenceId
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RecurrenceId
api_type:
- schema
ms.assetid: 9ef3569d-ee56-4b22-b008-609fb3337da7
description: Das Element RecurrenceId wird verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.
ms.openlocfilehash: 078bec85e1ca1530137f9935365d7dd3e530ea34
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831005"
---
# <a name="recurrenceid"></a><span data-ttu-id="97728-103">RecurrenceId</span><span class="sxs-lookup"><span data-stu-id="97728-103">RecurrenceId</span></span>

<span data-ttu-id="97728-104">Das Element **RecurrenceId** wird verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="97728-104">The **RecurrenceId** element is used to identify a specific instance of a recurring calendar item.</span></span> 
  
```xml
<RecurrenceId/>
```

 <span data-ttu-id="97728-105">**dateTime**</span><span class="sxs-lookup"><span data-stu-id="97728-105">**dateTime**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="97728-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="97728-106">Attributes and elements</span></span>

<span data-ttu-id="97728-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="97728-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="97728-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="97728-108">Attributes</span></span>

<span data-ttu-id="97728-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="97728-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="97728-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97728-110">Child elements</span></span>

<span data-ttu-id="97728-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="97728-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="97728-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="97728-112">Parent elements</span></span>

|<span data-ttu-id="97728-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="97728-113">**Element**</span></span>|<span data-ttu-id="97728-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="97728-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="97728-115">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="97728-115">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="97728-116">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="97728-116">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="97728-117">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="97728-117">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="97728-118">Stellt eine Besprechungsnachricht dar.</span><span class="sxs-lookup"><span data-stu-id="97728-118">Represents a meeting message.</span></span>  <br/> |
|[<span data-ttu-id="97728-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="97728-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="97728-120">Stellt eine Besprechungsanfrage an.</span><span class="sxs-lookup"><span data-stu-id="97728-120">Represents a meeting request.</span></span>  <br/> |
|[<span data-ttu-id="97728-121">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="97728-121">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="97728-122">Stellt eine Antwort auf Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="97728-122">Represents a meeting response.</span></span>  <br/> |
|[<span data-ttu-id="97728-123">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="97728-123">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="97728-124">Einen Besprechungsabsage darstellt.</span><span class="sxs-lookup"><span data-stu-id="97728-124">Represents a meeting cancellation.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="97728-125">Textwert</span><span class="sxs-lookup"><span data-stu-id="97728-125">Text value</span></span>

<span data-ttu-id="97728-126">Der Textwert stellt einen Datum/Uhrzeit-Wert, der ein Kalender Vorkommen identifiziert.</span><span class="sxs-lookup"><span data-stu-id="97728-126">The text value represents a date/time value that identifies a calendar occurrence.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="97728-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="97728-127">Remarks</span></span>

<span data-ttu-id="97728-128">Diese Eigenschaft wird mit der [UID](uid.md) -Eigenschaft verwendet, um eine bestimmte Instanz eines sich wiederholenden Kalenderelements zu identifizieren.</span><span class="sxs-lookup"><span data-stu-id="97728-128">This property is used with the [UID](uid.md) property to identify a specific instance of a recurring calendar item.</span></span> 
  
## <a name="element-information"></a><span data-ttu-id="97728-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="97728-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="97728-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="97728-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="97728-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="97728-131">Schema Name</span></span>  <br/> |<span data-ttu-id="97728-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="97728-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="97728-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="97728-133">Validation File</span></span>  <br/> |<span data-ttu-id="97728-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="97728-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="97728-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="97728-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="97728-136">False</span><span class="sxs-lookup"><span data-stu-id="97728-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="97728-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="97728-137">See also</span></span>



- [<span data-ttu-id="97728-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="97728-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

