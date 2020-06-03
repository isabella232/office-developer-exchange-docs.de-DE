---
title: RelativeYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeYearlyRecurrence
api_type:
- schema
ms.assetid: 25b67876-9979-4a30-a637-357ea10a93b8
description: Das RelativeYearlyRecurrence-Element beschreibt ein relatives jährliches Serienmuster.
ms.openlocfilehash: 2abe09ddfe52c24211ef5d0a392ddecaf15bf7bf
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44456729"
---
# <a name="relativeyearlyrecurrence"></a><span data-ttu-id="a501e-103">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="a501e-103">RelativeYearlyRecurrence</span></span>

<span data-ttu-id="a501e-104">Das **RelativeYearlyRecurrence** -Element beschreibt ein relatives jährliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="a501e-104">The **RelativeYearlyRecurrence** element describes a relative yearly recurrence pattern.</span></span> 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 <span data-ttu-id="a501e-105">**RelativeYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="a501e-105">**RelativeYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="a501e-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="a501e-106">Attributes and elements</span></span>

<span data-ttu-id="a501e-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="a501e-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="a501e-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="a501e-108">Attributes</span></span>

<span data-ttu-id="a501e-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="a501e-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="a501e-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a501e-110">Child elements</span></span>

|<span data-ttu-id="a501e-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="a501e-111">**Element**</span></span>|<span data-ttu-id="a501e-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a501e-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a501e-113">DaysOfWeek (dayofweektype)</span><span class="sxs-lookup"><span data-stu-id="a501e-113">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="a501e-114">Beschreibt die Wochentage, die in Element Serien Mustern verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="a501e-114">Describes the days of the week that are used in item recurrence patterns.</span></span>  <br/> |
|[<span data-ttu-id="a501e-115">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="a501e-115">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="a501e-116">Beschreibt, welche Woche in einem Monat in einem relativen jährlichen Serienmuster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="a501e-116">Describes which week in a month is used in a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="a501e-117">Month (Elementserie)</span><span class="sxs-lookup"><span data-stu-id="a501e-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="a501e-118">Beschreibt den Monat, in dem ein jährliches wiederkehrendes Element auftritt.</span><span class="sxs-lookup"><span data-stu-id="a501e-118">Describes the month when a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="a501e-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="a501e-119">Parent elements</span></span>

|<span data-ttu-id="a501e-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="a501e-120">**Element**</span></span>|<span data-ttu-id="a501e-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="a501e-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="a501e-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="a501e-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="a501e-123">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="a501e-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="a501e-124">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="a501e-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="a501e-125">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="a501e-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="a501e-126">Standard</span><span class="sxs-lookup"><span data-stu-id="a501e-126">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="a501e-127">Stellt das Datum und die Uhrzeit dar, zu der sich die Zeit von Sommerzeit zu Standardzeit ändert.</span><span class="sxs-lookup"><span data-stu-id="a501e-127">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="a501e-128">Sommer</span><span class="sxs-lookup"><span data-stu-id="a501e-128">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="a501e-129">Stellt das Datum und die Uhrzeit dar, zu der die Zeit von Standardzeit zu Sommerzeit wechselt.</span><span class="sxs-lookup"><span data-stu-id="a501e-129">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a501e-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="a501e-130">Remarks</span></span>

<span data-ttu-id="a501e-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="a501e-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="a501e-132">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="a501e-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="a501e-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="a501e-133">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="a501e-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="a501e-134">Schema Name</span></span>  <br/> |<span data-ttu-id="a501e-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="a501e-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="a501e-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="a501e-136">Validation File</span></span>  <br/> |<span data-ttu-id="a501e-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="a501e-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="a501e-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="a501e-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="a501e-139">False</span><span class="sxs-lookup"><span data-stu-id="a501e-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a501e-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="a501e-140">See also</span></span>



- [<span data-ttu-id="a501e-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="a501e-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

