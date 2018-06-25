---
title: IsRecurring
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IsRecurring
api_type:
- schema
ms.assetid: f4df6997-8d5b-4893-a4a5-fc7047e0a9c3
description: IsRecurring-Element gibt an, ob ein Kalenderelement, einer Besprechungsanfrage oder Aufgabe Teil einer Terminserie ist. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: dfb0c28fe225792c7128409a8cf010627c624fe0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830104"
---
# <a name="isrecurring"></a><span data-ttu-id="69d5e-104">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="69d5e-104">IsRecurring</span></span>

<span data-ttu-id="69d5e-105">**IsRecurring** -Element gibt an, ob ein Kalenderelement, einer Besprechungsanfrage oder Aufgabe Teil einer Terminserie ist.</span><span class="sxs-lookup"><span data-stu-id="69d5e-105">The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item.</span></span> <span data-ttu-id="69d5e-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="69d5e-106">This element is read-only.</span></span> 
  
```xml
<IsRecurring/>
```

 <span data-ttu-id="69d5e-107">**Boolean**</span><span class="sxs-lookup"><span data-stu-id="69d5e-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="69d5e-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="69d5e-108">Attributes and elements</span></span>

<span data-ttu-id="69d5e-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="69d5e-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="69d5e-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="69d5e-110">Attributes</span></span>

<span data-ttu-id="69d5e-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="69d5e-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="69d5e-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69d5e-112">Child elements</span></span>

<span data-ttu-id="69d5e-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="69d5e-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="69d5e-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="69d5e-114">Parent elements</span></span>

|<span data-ttu-id="69d5e-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="69d5e-115">**Element**</span></span>|<span data-ttu-id="69d5e-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="69d5e-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="69d5e-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="69d5e-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="69d5e-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="69d5e-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="69d5e-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="69d5e-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="69d5e-120">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="69d5e-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="69d5e-121">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="69d5e-121">Task</span></span>](task.md) <br/> |<span data-ttu-id="69d5e-122">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="69d5e-122">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="69d5e-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="69d5e-123">Text value</span></span>

<span data-ttu-id="69d5e-124">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="69d5e-124">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="69d5e-125">Hinweise</span><span class="sxs-lookup"><span data-stu-id="69d5e-125">Remarks</span></span>

<span data-ttu-id="69d5e-126">In der folgenden Tabelle wird gezeigt, wie die **IsRecurring** -Eigenschaft für verschiedene Kalender Elementtypen für Organisatoren und Teilnehmer sowie für Besprechungsanfragen und Updates festlegen ist.</span><span class="sxs-lookup"><span data-stu-id="69d5e-126">The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates.</span></span> 
  
|<span data-ttu-id="69d5e-127">**CalendarItem-Typ**</span><span class="sxs-lookup"><span data-stu-id="69d5e-127">**CalendarItem Type**</span></span>|<span data-ttu-id="69d5e-128">**Organizer <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="69d5e-128">**Organizer  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="69d5e-129">**ATTENDEE <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="69d5e-129">**Attendee  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="69d5e-130">**/ Aktualisierung der Besprechungsanfrage <br/> (IsRecurring)**</span><span class="sxs-lookup"><span data-stu-id="69d5e-130">**Meeting request/update  <br/> (IsRecurring)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="69d5e-131">Einzelnes Vorkommen</span><span class="sxs-lookup"><span data-stu-id="69d5e-131">Single Occurrence</span></span>  <br/> |<span data-ttu-id="69d5e-132">**"FALSE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-132">**FALSE**</span></span> <br/> |<span data-ttu-id="69d5e-133">**"FALSE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-133">**FALSE**</span></span> <br/> |<span data-ttu-id="69d5e-134">**"FALSE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-134">**FALSE**</span></span> <br/> |
|<span data-ttu-id="69d5e-135">Wiederkehrende Master-Shape</span><span class="sxs-lookup"><span data-stu-id="69d5e-135">Recurring Master</span></span>  <br/> |<span data-ttu-id="69d5e-136">**"FALSE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-136">**FALSE**</span></span> <br/> |<span data-ttu-id="69d5e-137">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-137">**TRUE**</span></span> <br/> |<span data-ttu-id="69d5e-138">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-138">**TRUE**</span></span> <br/> |
|<span data-ttu-id="69d5e-139">Periodische Ausnahme</span><span class="sxs-lookup"><span data-stu-id="69d5e-139">Recurring Exception</span></span>  <br/> |<span data-ttu-id="69d5e-140">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-140">**TRUE**</span></span> <br/> |<span data-ttu-id="69d5e-141">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-141">**TRUE**</span></span> <br/> |<span data-ttu-id="69d5e-142">**"TRUE"**</span><span class="sxs-lookup"><span data-stu-id="69d5e-142">**TRUE**</span></span> <br/> |
   
<span data-ttu-id="69d5e-143">Der Wert der **IsRecurring** -Eigenschaft, der sich wiederholenden master Kalenderelemente für den Organisator festgelegt ist, ist falsch. Dieser Wert muss auf **TRUE**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="69d5e-143">The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="69d5e-144">Der GetUserAvailability Vorgang enthält auch ein Element [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="69d5e-144">The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element.</span></span> 
  
<span data-ttu-id="69d5e-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="69d5e-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="69d5e-146">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="69d5e-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="69d5e-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="69d5e-147">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="69d5e-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="69d5e-148">Schema name</span></span>  <br/> |<span data-ttu-id="69d5e-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="69d5e-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="69d5e-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="69d5e-150">Validation file</span></span>  <br/> |<span data-ttu-id="69d5e-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="69d5e-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="69d5e-152">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="69d5e-152">Can be empty</span></span>  <br/> |<span data-ttu-id="69d5e-153">False</span><span class="sxs-lookup"><span data-stu-id="69d5e-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="69d5e-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="69d5e-154">See also</span></span>



[<span data-ttu-id="69d5e-155">TaskType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="69d5e-155">TaskType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[<span data-ttu-id="69d5e-156">CalendarEventDetails.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="69d5e-156">CalendarEventDetails.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[<span data-ttu-id="69d5e-157">CalendarItemType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="69d5e-157">CalendarItemType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[<span data-ttu-id="69d5e-158">MeetingRequestMessageType.IsRecurring</span><span class="sxs-lookup"><span data-stu-id="69d5e-158">MeetingRequestMessageType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[<span data-ttu-id="69d5e-159">CalendarItemType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="69d5e-159">CalendarItemType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="69d5e-160">MeetingRequestMessageType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="69d5e-160">MeetingRequestMessageType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="69d5e-161">TaskType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="69d5e-161">TaskType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [<span data-ttu-id="69d5e-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="69d5e-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

