---
title: Serie (RecurrenceType)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Recurrence
api_type:
- schema
ms.assetid: 3d1c2c1c-4103-47ce-ad3c-ad16ec6e9b12
description: Recurrence-Element enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.
ms.openlocfilehash: f26ccf5912848a6d7fbbfa7d0a19d41635c896e0
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831004"
---
# <a name="recurrence-recurrencetype"></a><span data-ttu-id="773a9-103">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="773a9-103">Recurrence (RecurrenceType)</span></span>

<span data-ttu-id="773a9-104">**Recurrence** -Element enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="773a9-104">The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 <span data-ttu-id="773a9-105">**RecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="773a9-105">**RecurrenceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="773a9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="773a9-106">Attributes and elements</span></span>

<span data-ttu-id="773a9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="773a9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="773a9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="773a9-108">Attributes</span></span>

<span data-ttu-id="773a9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="773a9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="773a9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="773a9-110">Child elements</span></span>

|<span data-ttu-id="773a9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="773a9-111">**Element**</span></span>|<span data-ttu-id="773a9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="773a9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="773a9-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="773a9-114">Wird ein relativer jährliches Serienmuster beschrieben.</span><span class="sxs-lookup"><span data-stu-id="773a9-114">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="773a9-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="773a9-116">Stellt ein jährliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="773a9-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="773a9-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="773a9-118">Beschreibt ein relative monatliches Serienmuster wiederkehrende Kalenderelemente.</span><span class="sxs-lookup"><span data-stu-id="773a9-118">Describes a relative monthly recurrence pattern for a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="773a9-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="773a9-120">Stellt ein monatliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="773a9-120">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="773a9-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="773a9-122">Beschreibt die Häufigkeit in Wochen und die Tage, die ein Kalenderelement oder eine Aufgabe wiederholt.</span><span class="sxs-lookup"><span data-stu-id="773a9-122">Describes the frequency, in weeks, and the days that a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="773a9-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="773a9-124">Beschreibt die Häufigkeit in Tagen, in dem ein Kalenderelement oder eine Aufgabe wiederholt.</span><span class="sxs-lookup"><span data-stu-id="773a9-124">Describes the frequency, in days, in which a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="773a9-125">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-125">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="773a9-126">Beschreibt ein Serienmuster, die nicht über einen definierten Enddatum verfügt.</span><span class="sxs-lookup"><span data-stu-id="773a9-126">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="773a9-127">Die Verwendung dieses Elements schließt die Verwendung der [EndDateRecurrence](enddaterecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="773a9-127">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="773a9-128">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-128">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="773a9-129">Beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="773a9-129">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="773a9-130">Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="773a9-130">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="773a9-131">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="773a9-131">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="773a9-132">Beschreibt das Startdatum und die Anzahl der Vorkommen eines sich wiederholenden-Elements.</span><span class="sxs-lookup"><span data-stu-id="773a9-132">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="773a9-133">Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [EndDateRecurrence](enddaterecurrence.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="773a9-133">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="773a9-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="773a9-134">Parent elements</span></span>

|<span data-ttu-id="773a9-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="773a9-135">**Element**</span></span>|<span data-ttu-id="773a9-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="773a9-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="773a9-137">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="773a9-137">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="773a9-138">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="773a9-138">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="773a9-139">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="773a9-139">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="773a9-140">Stellt eine Besprechungsanfrage im Exchange-Speicher</span><span class="sxs-lookup"><span data-stu-id="773a9-140">Represents a meeting request in the Exchange store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="773a9-141">Hinweise</span><span class="sxs-lookup"><span data-stu-id="773a9-141">Remarks</span></span>

<span data-ttu-id="773a9-142">Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den Wert RecurringMaster hat.</span><span class="sxs-lookup"><span data-stu-id="773a9-142">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="773a9-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="773a9-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="773a9-144">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="773a9-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="773a9-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="773a9-145">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="773a9-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="773a9-146">Schema name</span></span>  <br/> |<span data-ttu-id="773a9-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="773a9-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="773a9-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="773a9-148">Validation file</span></span>  <br/> |<span data-ttu-id="773a9-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="773a9-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="773a9-150">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="773a9-150">Can be empty</span></span>  <br/> |<span data-ttu-id="773a9-151">False</span><span class="sxs-lookup"><span data-stu-id="773a9-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="773a9-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="773a9-152">See also</span></span>



- [<span data-ttu-id="773a9-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="773a9-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

