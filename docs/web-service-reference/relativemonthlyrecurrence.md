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
description: Das RelativeMonthlyRecurrence-Element wird ein relativer monatliches Serienmuster beschrieben.
ms.openlocfilehash: 9b695052c38e2693946837bf99f03baea093df08
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19831053"
---
# <a name="relativemonthlyrecurrence"></a><span data-ttu-id="78303-103">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="78303-103">RelativeMonthlyRecurrence</span></span>

<span data-ttu-id="78303-104">Das **RelativeMonthlyRecurrence** -Element wird ein relativer monatliches Serienmuster beschrieben.</span><span class="sxs-lookup"><span data-stu-id="78303-104">The **RelativeMonthlyRecurrence** element describes a relative monthly recurrence pattern.</span></span> 
  
```xml
<RelativeMonthlyRecurrence>
   <Interval/>
   <DaysOfWeek/>
   <DayOfWeekIndex/>
</RelativeMonthlyRecurrence>
```

 <span data-ttu-id="78303-105">**RelativeMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="78303-105">**RelativeMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="78303-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="78303-106">Attributes and elements</span></span>

<span data-ttu-id="78303-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="78303-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="78303-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="78303-108">Attributes</span></span>

<span data-ttu-id="78303-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="78303-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="78303-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78303-110">Child elements</span></span>

|<span data-ttu-id="78303-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="78303-111">**Element**</span></span>|<span data-ttu-id="78303-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78303-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78303-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="78303-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="78303-114">Definiert das Intervall zwischen zwei aufeinander folgenden monatliche Muster Terminserien.</span><span class="sxs-lookup"><span data-stu-id="78303-114">Defines the interval between two consecutive monthly recurring pattern items.</span></span> <span data-ttu-id="78303-115">Der Bereich für diesen Wert ist 1 bis 99.</span><span class="sxs-lookup"><span data-stu-id="78303-115">The range for this value is 1 to 99.</span></span>  <br/> |
|[<span data-ttu-id="78303-116">DaysOfWeek (DayOfWeekType)</span><span class="sxs-lookup"><span data-stu-id="78303-116">DaysOfWeek (DayOfWeekType)</span></span>](daysofweek-dayofweektype.md) <br/> |<span data-ttu-id="78303-117">Beschreibt, welche die Wochentage in das relative monatliches Serienmuster sind.</span><span class="sxs-lookup"><span data-stu-id="78303-117">Describes which days of the week are in the relative monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="78303-118">DayOfWeekIndex</span><span class="sxs-lookup"><span data-stu-id="78303-118">DayOfWeekIndex</span></span>](dayofweekindex.md) <br/> |<span data-ttu-id="78303-119">Beschreibt, welche Woche in ein monatliches Serienmuster relative verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="78303-119">Describes which week is used in a relative monthly recurrence pattern.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="78303-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="78303-120">Parent elements</span></span>

|<span data-ttu-id="78303-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="78303-121">**Element**</span></span>|<span data-ttu-id="78303-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="78303-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="78303-123">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="78303-123">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="78303-124">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="78303-124">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="78303-125">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="78303-125">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="78303-126">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="78303-126">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="78303-127">Hinweise</span><span class="sxs-lookup"><span data-stu-id="78303-127">Remarks</span></span>

<span data-ttu-id="78303-128">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der Microsoft Exchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="78303-128">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="78303-129">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="78303-129">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="78303-130">Namespace</span><span class="sxs-lookup"><span data-stu-id="78303-130">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="78303-131">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="78303-131">Schema Name</span></span>  <br/> |<span data-ttu-id="78303-132">Schematypen</span><span class="sxs-lookup"><span data-stu-id="78303-132">Types schema</span></span>  <br/> |
|<span data-ttu-id="78303-133">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="78303-133">Validation File</span></span>  <br/> |<span data-ttu-id="78303-134">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="78303-134">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="78303-135">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="78303-135">Can be Empty</span></span>  <br/> |<span data-ttu-id="78303-136">False</span><span class="sxs-lookup"><span data-stu-id="78303-136">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="78303-137">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="78303-137">See also</span></span>



- [<span data-ttu-id="78303-138">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="78303-138">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

