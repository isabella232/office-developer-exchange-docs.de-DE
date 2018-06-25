---
title: WeeklyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WeeklyRecurrence
api_type:
- schema
ms.assetid: 69c41dd5-597c-45bc-be3f-e2f2b5615aa3
description: Das WeeklyRecurrence-Element wird ein wöchentliches Serienmuster beschrieben.
ms.openlocfilehash: 78bc76dd63c6737786df02f336217dc8de9a3a67
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19839529"
---
# <a name="weeklyrecurrence"></a><span data-ttu-id="4ef25-103">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="4ef25-103">WeeklyRecurrence</span></span>

<span data-ttu-id="4ef25-104">Das **WeeklyRecurrence** -Element wird ein wöchentliches Serienmuster beschrieben.</span><span class="sxs-lookup"><span data-stu-id="4ef25-104">The **WeeklyRecurrence** element describes a weekly recurrence pattern.</span></span> 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 <span data-ttu-id="4ef25-105">**WeeklyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="4ef25-105">**WeeklyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="4ef25-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="4ef25-106">Attributes and elements</span></span>

<span data-ttu-id="4ef25-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="4ef25-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="4ef25-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="4ef25-108">Attributes</span></span>

<span data-ttu-id="4ef25-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ef25-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="4ef25-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ef25-110">Child elements</span></span>

|<span data-ttu-id="4ef25-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ef25-111">**Element**</span></span>|<span data-ttu-id="4ef25-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ef25-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ef25-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="4ef25-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="4ef25-114">Definiert das Intervall in Wochen zwischen zwei aufeinander folgende wöchentliche Serie Muster Elemente.</span><span class="sxs-lookup"><span data-stu-id="4ef25-114">Defines the interval, in weeks, between two consecutive weekly recurrence pattern items.</span></span> <span data-ttu-id="4ef25-115">Der Wert kann im Bereich von 1 bis 99 sein.</span><span class="sxs-lookup"><span data-stu-id="4ef25-115">The value can be in the range from 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="4ef25-116">DaysOfWeek (DaysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="4ef25-116">DaysOfWeek (DaysOfWeekType)</span></span>](daysofweek-daysofweektype.md) <br/> |<span data-ttu-id="4ef25-117">Beschreibt, welche die Wochentage in wöchentliches Serienmuster sind.</span><span class="sxs-lookup"><span data-stu-id="4ef25-117">Describes which days of the week are in the weekly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="4ef25-118">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="4ef25-118">FirstDayOfWeek</span></span>](firstdayofweek.md) <br/> |<span data-ttu-id="4ef25-119">Gibt den ersten Tag der Woche.</span><span class="sxs-lookup"><span data-stu-id="4ef25-119">Specifies the first day of the week.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="4ef25-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="4ef25-120">Parent elements</span></span>

|<span data-ttu-id="4ef25-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="4ef25-121">**Element**</span></span>|<span data-ttu-id="4ef25-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="4ef25-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="4ef25-123">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="4ef25-123">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="4ef25-124">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="4ef25-124">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="4ef25-125">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="4ef25-125">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="4ef25-126">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="4ef25-126">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="4ef25-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="4ef25-127">Text value</span></span>

<span data-ttu-id="4ef25-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="4ef25-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="4ef25-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="4ef25-129">Remarks</span></span>

<span data-ttu-id="4ef25-130">Die Zeitzone Offset Informationen geht verloren, wenn die [ [Starten](start.md) und](end-ex15websvcsotherref.md) Enddatum des wiederkehrenden master-Objekts nicht über ein Datum verfügen, das das erste Auftreten des ein wöchentliches Serienmuster gleich ist.</span><span class="sxs-lookup"><span data-stu-id="4ef25-130">The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="4ef25-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="4ef25-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="4ef25-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="4ef25-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4ef25-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="4ef25-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="4ef25-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="4ef25-134">Schema Name</span></span>  <br/> |<span data-ttu-id="4ef25-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="4ef25-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="4ef25-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="4ef25-136">Validation File</span></span>  <br/> |<span data-ttu-id="4ef25-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="4ef25-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="4ef25-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="4ef25-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="4ef25-139">False</span><span class="sxs-lookup"><span data-stu-id="4ef25-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="4ef25-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="4ef25-140">See also</span></span>



- [<span data-ttu-id="4ef25-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="4ef25-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

