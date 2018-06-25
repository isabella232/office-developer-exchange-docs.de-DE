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
description: Das RelativeYearlyRecurrence-Element wird ein relativer jährliches Serienmuster beschrieben.
ms.openlocfilehash: ce8d2b134ce1fa34cbce8bd2fa921cab18d908a4
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831057"
---
# <a name="relativeyearlyrecurrence"></a><span data-ttu-id="66b52-103">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="66b52-103">RelativeYearlyRecurrence</span></span>

<span data-ttu-id="66b52-104">Das **RelativeYearlyRecurrence** -Element wird ein relativer jährliches Serienmuster beschrieben.</span><span class="sxs-lookup"><span data-stu-id="66b52-104">The **RelativeYearlyRecurrence** element describes a relative yearly recurrence pattern.</span></span> 
  
```xml
<RelativeYearlyRecurrence>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
   <Month/>
</RelativeYearlyRecurrence>
```

 <span data-ttu-id="66b52-105">**RelativeYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="66b52-105">**RelativeYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="66b52-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="66b52-106">Attributes and elements</span></span>

<span data-ttu-id="66b52-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="66b52-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="66b52-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="66b52-108">Attributes</span></span>

<span data-ttu-id="66b52-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="66b52-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="66b52-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66b52-110">Child elements</span></span>

|<span data-ttu-id="66b52-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="66b52-111">**Element**</span></span>|<span data-ttu-id="66b52-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66b52-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66b52-113">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="66b52-113">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="66b52-114">Beschreibt die Wochentage, die in Artikel Serienmuster verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="66b52-114">Describes the days of the week that are used in item recurrence patterns.</span></span>  <br/> |
|[<span data-ttu-id="66b52-115">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="66b52-115">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="66b52-116">Beschreibt die Woche im Monat in ein jährliches Serienmuster relative verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="66b52-116">Describes which week in a month is used in a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="66b52-117">Month (Element Serie)</span><span class="sxs-lookup"><span data-stu-id="66b52-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="66b52-118">Beschreibt den Monat, wenn eine jährliche Terminserie erfolgt.</span><span class="sxs-lookup"><span data-stu-id="66b52-118">Describes the month when a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="66b52-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="66b52-119">Parent elements</span></span>

|<span data-ttu-id="66b52-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="66b52-120">**Element**</span></span>|<span data-ttu-id="66b52-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="66b52-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="66b52-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="66b52-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="66b52-123">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="66b52-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="66b52-124">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="66b52-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="66b52-125">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="66b52-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="66b52-126">Standard</span><span class="sxs-lookup"><span data-stu-id="66b52-126">Standard</span></span>](standard.md) <br/> |<span data-ttu-id="66b52-127">Das Datum und Zeitpunkt der Änderung die Zeit von Sommerzeit auf Normalzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="66b52-127">Represents the date and time when the time changes from daylight saving time to standard time.</span></span>  <br/> |
|[<span data-ttu-id="66b52-128">Sommerzeit</span><span class="sxs-lookup"><span data-stu-id="66b52-128">Daylight</span></span>](daylight.md) <br/> |<span data-ttu-id="66b52-129">Das Datum und Zeitpunkt der Änderung die Zeit von Normalzeit auf Sommerzeit darstellt.</span><span class="sxs-lookup"><span data-stu-id="66b52-129">Represents the date and time when the time changes from standard time to daylight saving time.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="66b52-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="66b52-130">Remarks</span></span>

<span data-ttu-id="66b52-131">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="66b52-131">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="66b52-132">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="66b52-132">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="66b52-133">Namespace</span><span class="sxs-lookup"><span data-stu-id="66b52-133">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="66b52-134">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="66b52-134">Schema Name</span></span>  <br/> |<span data-ttu-id="66b52-135">Schematypen</span><span class="sxs-lookup"><span data-stu-id="66b52-135">Types schema</span></span>  <br/> |
|<span data-ttu-id="66b52-136">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="66b52-136">Validation File</span></span>  <br/> |<span data-ttu-id="66b52-137">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="66b52-137">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="66b52-138">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="66b52-138">Can be Empty</span></span>  <br/> |<span data-ttu-id="66b52-139">False</span><span class="sxs-lookup"><span data-stu-id="66b52-139">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="66b52-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="66b52-140">See also</span></span>



- [<span data-ttu-id="66b52-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="66b52-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

