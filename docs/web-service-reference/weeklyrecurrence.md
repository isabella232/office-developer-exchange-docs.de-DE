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
description: Das WeeklyRecurrence-Element beschreibt ein wöchentliches Serienmuster.
ms.openlocfilehash: 5006238590c4cd7556a92fb1fbe13292383412b8
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44530366"
---
# <a name="weeklyrecurrence"></a><span data-ttu-id="d1295-103">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="d1295-103">WeeklyRecurrence</span></span>

<span data-ttu-id="d1295-104">Das **WeeklyRecurrence** -Element beschreibt ein wöchentliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="d1295-104">The **WeeklyRecurrence** element describes a weekly recurrence pattern.</span></span> 
  
```XML
<WeeklyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <FirstDayOfWeek/>
</WeeklyRecurrence>
```

 <span data-ttu-id="d1295-105">**WeeklyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="d1295-105">**WeeklyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d1295-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d1295-106">Attributes and elements</span></span>

<span data-ttu-id="d1295-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d1295-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d1295-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d1295-108">Attributes</span></span>

<span data-ttu-id="d1295-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1295-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d1295-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1295-110">Child elements</span></span>

|<span data-ttu-id="d1295-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1295-111">**Element**</span></span>|<span data-ttu-id="d1295-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1295-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1295-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="d1295-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="d1295-114">Definiert das Intervall zwischen zwei aufeinander folgenden wöchentlichen Serienmuster Elementen in Wochen.</span><span class="sxs-lookup"><span data-stu-id="d1295-114">Defines the interval, in weeks, between two consecutive weekly recurrence pattern items.</span></span> <span data-ttu-id="d1295-115">Der Wert kann im Bereich von 1 bis 99 liegen.</span><span class="sxs-lookup"><span data-stu-id="d1295-115">The value can be in the range from 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="d1295-116">DaysOfWeek (DaysOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="d1295-116">DaysOfWeek (DaysOfWeekType)</span></span>](daysofweek-daysofweektype.md) <br/> |<span data-ttu-id="d1295-117">Beschreibt, welche Wochentage im wöchentlichen Serienmuster liegen.</span><span class="sxs-lookup"><span data-stu-id="d1295-117">Describes which days of the week are in the weekly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="d1295-118">FirstDayOfWeek</span><span class="sxs-lookup"><span data-stu-id="d1295-118">FirstDayOfWeek</span></span>](firstdayofweek.md) <br/> |<span data-ttu-id="d1295-119">Gibt den ersten Tag der Woche an.</span><span class="sxs-lookup"><span data-stu-id="d1295-119">Specifies the first day of the week.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d1295-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d1295-120">Parent elements</span></span>

|<span data-ttu-id="d1295-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="d1295-121">**Element**</span></span>|<span data-ttu-id="d1295-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d1295-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d1295-123">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="d1295-123">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="d1295-124">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="d1295-124">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="d1295-125">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="d1295-125">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="d1295-126">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="d1295-126">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d1295-127">Textwert</span><span class="sxs-lookup"><span data-stu-id="d1295-127">Text value</span></span>

<span data-ttu-id="d1295-128">Keine.</span><span class="sxs-lookup"><span data-stu-id="d1295-128">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d1295-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d1295-129">Remarks</span></span>

<span data-ttu-id="d1295-130">Die Zeitzonenoffset Informationen gehen verloren, wenn das [anfangs](start.md) -und Enddatum des [wiederkehrenden Haupt](end-ex15websvcsotherref.md) Elements kein Datum aufweist, das dem ersten Vorkommen eines wöchentlichen Serienmusters entspricht.</span><span class="sxs-lookup"><span data-stu-id="d1295-130">The time zone offset information is lost if the [Start](start.md) and [End ](end-ex15websvcsotherref.md) dates of the recurring master item do not have a date that is equal to the first occurrence of a weekly recurrence pattern.</span></span> 
  
<span data-ttu-id="d1295-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d1295-131">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d1295-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d1295-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d1295-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="d1295-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d1295-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d1295-134">Schema Name</span></span>  <br/> |<span data-ttu-id="d1295-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d1295-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="d1295-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d1295-136">Validation File</span></span>  <br/> |<span data-ttu-id="d1295-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d1295-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d1295-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d1295-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="d1295-139">False</span><span class="sxs-lookup"><span data-stu-id="d1295-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d1295-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d1295-140">See also</span></span>



- [<span data-ttu-id="d1295-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d1295-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

