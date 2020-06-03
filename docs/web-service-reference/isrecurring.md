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
description: Das isterminive-Element gibt an, ob ein Kalenderelement, eine Besprechungsanfrage oder eine Aufgabe Teil eines wiederkehrenden Elements ist. Dieses Element ist schreibgeschützt.
ms.openlocfilehash: 72c71c1955b69f1c0df855ce4bd0ed02d4c89122
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44526487"
---
# <a name="isrecurring"></a><span data-ttu-id="a8091-104">IsRecurring</span><span class="sxs-lookup"><span data-stu-id="a8091-104">IsRecurring</span></span>

<span data-ttu-id="a8091-105">Das **isterminive** -Element gibt an, ob ein Kalenderelement, eine Besprechungsanfrage oder eine Aufgabe Teil eines wiederkehrenden Elements ist.</span><span class="sxs-lookup"><span data-stu-id="a8091-105">The **IsRecurring** element indicates whether a calendar item, meeting request, or task is part of a recurring item.</span></span> <span data-ttu-id="a8091-106">Dieses Element ist schreibgeschützt.</span><span class="sxs-lookup"><span data-stu-id="a8091-106">This element is read-only.</span></span> 
  
```xml
<IsRecurring/>
```

 <span data-ttu-id="a8091-107">**Boolescher Wert**</span><span class="sxs-lookup"><span data-stu-id="a8091-107">**Boolean**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a8091-108">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a8091-108">Attributes and elements</span></span>

<span data-ttu-id="a8091-109">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a8091-109">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a8091-110">Attribute</span><span class="sxs-lookup"><span data-stu-id="a8091-110">Attributes</span></span>

<span data-ttu-id="a8091-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8091-111">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a8091-112">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8091-112">Child elements</span></span>

<span data-ttu-id="a8091-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="a8091-113">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="a8091-114">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a8091-114">Parent elements</span></span>

|<span data-ttu-id="a8091-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="a8091-115">**Element**</span></span>|<span data-ttu-id="a8091-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a8091-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a8091-117">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="a8091-117">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="a8091-118">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="a8091-118">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="a8091-119">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="a8091-119">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="a8091-120">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="a8091-120">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="a8091-121">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="a8091-121">Task</span></span>](task.md) <br/> |<span data-ttu-id="a8091-122">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="a8091-122">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="a8091-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="a8091-123">Text value</span></span>

<span data-ttu-id="a8091-124">Ein Textwert, der einen booleschen Wert darstellt, ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="a8091-124">A text value that represents a Boolean value is required.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="a8091-125">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a8091-125">Remarks</span></span>

<span data-ttu-id="a8091-126">In der folgenden Tabelle wird gezeigt, wie die **isterminive** -Eigenschaft für unterschiedliche Kalenderelement Typen für Organisatoren und Teilnehmer sowie für Besprechungsanfragen und Updates festgelegt wird.</span><span class="sxs-lookup"><span data-stu-id="a8091-126">The following table shows how the **IsRecurring** property is set for different calendar item types for organizers and attendees and for meeting requests and updates.</span></span> 
  
|<span data-ttu-id="a8091-127">**CalendarItem-Typ**</span><span class="sxs-lookup"><span data-stu-id="a8091-127">**CalendarItem Type**</span></span>|<span data-ttu-id="a8091-128">**Organizer <br/> (reterminal)**</span><span class="sxs-lookup"><span data-stu-id="a8091-128">**Organizer  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="a8091-129">**Teilnehmer <br/> (iswiederkehr)**</span><span class="sxs-lookup"><span data-stu-id="a8091-129">**Attendee  <br/> (IsRecurring)**</span></span>|<span data-ttu-id="a8091-130">**Besprechungsanfrage/-Aktualisierung <br/> (einmaliges Anmelden)**</span><span class="sxs-lookup"><span data-stu-id="a8091-130">**Meeting request/update  <br/> (IsRecurring)**</span></span>|
|:-----|:-----|:-----|:-----|
|<span data-ttu-id="a8091-131">Einzelnes Vorkommen</span><span class="sxs-lookup"><span data-stu-id="a8091-131">Single Occurrence</span></span>  <br/> |<span data-ttu-id="a8091-132">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a8091-132">**FALSE**</span></span> <br/> |<span data-ttu-id="a8091-133">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a8091-133">**FALSE**</span></span> <br/> |<span data-ttu-id="a8091-134">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a8091-134">**FALSE**</span></span> <br/> |
|<span data-ttu-id="a8091-135">Wiederkehrendes Master</span><span class="sxs-lookup"><span data-stu-id="a8091-135">Recurring Master</span></span>  <br/> |<span data-ttu-id="a8091-136">**FALSE**</span><span class="sxs-lookup"><span data-stu-id="a8091-136">**FALSE**</span></span> <br/> |<span data-ttu-id="a8091-137">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a8091-137">**TRUE**</span></span> <br/> |<span data-ttu-id="a8091-138">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a8091-138">**TRUE**</span></span> <br/> |
|<span data-ttu-id="a8091-139">Wiederkehrende Ausnahme</span><span class="sxs-lookup"><span data-stu-id="a8091-139">Recurring Exception</span></span>  <br/> |<span data-ttu-id="a8091-140">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a8091-140">**TRUE**</span></span> <br/> |<span data-ttu-id="a8091-141">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a8091-141">**TRUE**</span></span> <br/> |<span data-ttu-id="a8091-142">**TRUE**</span><span class="sxs-lookup"><span data-stu-id="a8091-142">**TRUE**</span></span> <br/> |
   
<span data-ttu-id="a8091-143">Der Wert der **iswiederkehr** -Eigenschaft, der für wiederkehrende Hauptkalender Elemente für den Organisator festgelegt ist, ist falsch; Dieser Wert sollte auf **true**festgelegt werden.</span><span class="sxs-lookup"><span data-stu-id="a8091-143">The **IsRecurring** property value that is set for recurring master calendar items for the organizer is incorrect; this value should be set to **TRUE**.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="a8091-144">Der GetUserAvailability-Vorgang verfügt auch über ein [iswiederkehr Endes Element (CalendarEventDetails)](isrecurring-calendareventdetails.md) .</span><span class="sxs-lookup"><span data-stu-id="a8091-144">The GetUserAvailability operation also has an [IsRecurring (CalendarEventDetails)](isrecurring-calendareventdetails.md) element.</span></span> 
  
<span data-ttu-id="a8091-145">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a8091-145">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a8091-146">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a8091-146">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a8091-147">Namespace</span><span class="sxs-lookup"><span data-stu-id="a8091-147">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a8091-148">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a8091-148">Schema name</span></span>  <br/> |<span data-ttu-id="a8091-149">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a8091-149">Types schema</span></span>  <br/> |
|<span data-ttu-id="a8091-150">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a8091-150">Validation file</span></span>  <br/> |<span data-ttu-id="a8091-151">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a8091-151">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a8091-152">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="a8091-152">Can be empty</span></span>  <br/> |<span data-ttu-id="a8091-153">False</span><span class="sxs-lookup"><span data-stu-id="a8091-153">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a8091-154">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a8091-154">See also</span></span>



[<span data-ttu-id="a8091-155">TaskType. iswiederkehr Ende</span><span class="sxs-lookup"><span data-stu-id="a8091-155">TaskType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurring.aspx)
  
[<span data-ttu-id="a8091-156">CalendarEventDetails. iswiederkehr Ende</span><span class="sxs-lookup"><span data-stu-id="a8091-156">CalendarEventDetails.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarEventDetails.IsRecurring.aspx)
  
[<span data-ttu-id="a8091-157">CalendarItemType. iswiederkehr Ende</span><span class="sxs-lookup"><span data-stu-id="a8091-157">CalendarItemType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurring.aspx)
  
[<span data-ttu-id="a8091-158">MeetingRequestMessageType. iswiederkehr Ende</span><span class="sxs-lookup"><span data-stu-id="a8091-158">MeetingRequestMessageType.IsRecurring</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurring.aspx)
  
[<span data-ttu-id="a8091-159">CalendarItemType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="a8091-159">CalendarItemType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.CalendarItemType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="a8091-160">MeetingRequestMessageType.IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="a8091-160">MeetingRequestMessageType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.MeetingRequestMessageType.IsRecurringSpecified.aspx)
  
[<span data-ttu-id="a8091-161">TaskType. IsRecurringSpecified</span><span class="sxs-lookup"><span data-stu-id="a8091-161">TaskType.IsRecurringSpecified</span></span>](https://msdn.microsoft.com/library/ExchangeWebServices.TaskType.IsRecurringSpecified.aspx)


- [<span data-ttu-id="a8091-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a8091-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

