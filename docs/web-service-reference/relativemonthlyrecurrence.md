---
title: RelativeMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- RelativeMonthlyRecurrence
api_type:
- schema
ms.assetid: a76595db-7460-44ac-ac2a-53241caa33a7
description: Das RelativeMonthlyRecurrence-Element beschreibt ein relatives monatliches Serienmuster.
ms.openlocfilehash: 90aa0e43684bfb09a3e13cf86ec96f680e80a714
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457508"
---
# <a name="relativemonthlyrecurrence"></a><span data-ttu-id="75ae9-103">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="75ae9-103">RelativeMonthlyRecurrence</span></span>

<span data-ttu-id="75ae9-104">Das **RelativeMonthlyRecurrence** -Element beschreibt ein relatives monatliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="75ae9-104">The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern.</span></span> 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 <span data-ttu-id="75ae9-105">**RelativeMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="75ae9-105">**RelativeMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="75ae9-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="75ae9-106">Attributes and elements</span></span>

<span data-ttu-id="75ae9-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="75ae9-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="75ae9-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="75ae9-108">Attributes</span></span>

<span data-ttu-id="75ae9-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="75ae9-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="75ae9-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75ae9-110">Child elements</span></span>

|<span data-ttu-id="75ae9-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="75ae9-111">**Element**</span></span>|<span data-ttu-id="75ae9-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75ae9-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75ae9-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="75ae9-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="75ae9-114">Definiert das Intervall zwischen zwei aufeinander folgenden monatlichen wiederkehrenden Musterelementen.</span><span class="sxs-lookup"><span data-stu-id="75ae9-114">Defines the interval between two consecutive monthly recurring pattern items.</span></span> <span data-ttu-id="75ae9-115">Der Bereich für diesen Wert ist 1 bis 99.</span><span class="sxs-lookup"><span data-stu-id="75ae9-115">The range for this value is 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="75ae9-116">DaysOfWeek (dayofweektype)</span><span class="sxs-lookup"><span data-stu-id="75ae9-116">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="75ae9-117">Beschreibt, welche Wochentage sich im relativen monatlichen Serienmuster befinden.</span><span class="sxs-lookup"><span data-stu-id="75ae9-117">Describes which days of the week are in the relative monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="75ae9-118">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="75ae9-118">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="75ae9-119">Beschreibt, welche Woche in einem relativen monatlichen Serienmuster verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="75ae9-119">Describes which week is used in a relative monthly recurrence pattern.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="75ae9-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="75ae9-120">Parent elements</span></span>

|<span data-ttu-id="75ae9-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="75ae9-121">**Element**</span></span>|<span data-ttu-id="75ae9-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="75ae9-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="75ae9-123">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="75ae9-123">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="75ae9-124">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="75ae9-124">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="75ae9-125">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="75ae9-125">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="75ae9-126">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="75ae9-126">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="75ae9-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="75ae9-127">Remarks</span></span>

<span data-ttu-id="75ae9-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="75ae9-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="75ae9-129">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="75ae9-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="75ae9-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="75ae9-130">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="75ae9-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="75ae9-131">Schema Name</span></span>  <br/> |<span data-ttu-id="75ae9-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="75ae9-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="75ae9-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="75ae9-133">Validation File</span></span>  <br/> |<span data-ttu-id="75ae9-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="75ae9-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="75ae9-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="75ae9-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="75ae9-136">False</span><span class="sxs-lookup"><span data-stu-id="75ae9-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="75ae9-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="75ae9-137">See also</span></span>



- [<span data-ttu-id="75ae9-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="75ae9-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

