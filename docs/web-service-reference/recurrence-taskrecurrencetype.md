---
title: Serie (TaskRecurrenceType)
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
ms.assetid: 99f8414a-9110-4721-a6e5-ebf225d7ed0a
description: Recurrence-Element enthält Serieninformationen für wiederkehrende Aufgaben.
ms.openlocfilehash: ae2bb35e89a0a50c7ca67cb0e580427150afb99e
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19831006"
---
# <a name="recurrence-taskrecurrencetype"></a><span data-ttu-id="469d6-103">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="469d6-103">Recurrence (TaskRecurrenceType)</span></span>

<span data-ttu-id="469d6-104">**Recurrence** -Element enthält Serieninformationen für wiederkehrende Aufgaben.</span><span class="sxs-lookup"><span data-stu-id="469d6-104">The **Recurrence** element contains recurrence information for recurring tasks.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

 <span data-ttu-id="469d6-105">**TaskRecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="469d6-105">**TaskRecurrenceType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="469d6-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="469d6-106">Attributes and elements</span></span>

<span data-ttu-id="469d6-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="469d6-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="469d6-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="469d6-108">Attributes</span></span>

<span data-ttu-id="469d6-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="469d6-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="469d6-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="469d6-110">Child elements</span></span>

|<span data-ttu-id="469d6-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="469d6-111">**Element**</span></span>|<span data-ttu-id="469d6-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="469d6-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="469d6-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="469d6-114">Ein relative jährliches Serienmuster für einen sich wiederholenden Vorgang beschreibt.</span><span class="sxs-lookup"><span data-stu-id="469d6-114">Describes a relative yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="469d6-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="469d6-116">Stellt ein jährliches Serienmuster für einen sich wiederholenden Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="469d6-116">Represents a yearly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="469d6-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="469d6-118">Ein relative monatliches Serienmuster für einen sich wiederholenden Vorgang beschreibt.</span><span class="sxs-lookup"><span data-stu-id="469d6-118">Describes a relative monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="469d6-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="469d6-120">Stellt ein monatliches Serienmuster für einen sich wiederholenden Vorgang dar.</span><span class="sxs-lookup"><span data-stu-id="469d6-120">Represents a monthly recurrence pattern for a recurring task.</span></span>  <br/> |
|[<span data-ttu-id="469d6-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="469d6-122">Beschreibt die Häufigkeit in Wochen und die Tage, an denen eine Aufgabe wiederholt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="469d6-122">Describes the frequency, in weeks, and the days on which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="469d6-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="469d6-124">Beschreibt die Häufigkeit in Tagen, in denen eine Aufgabe wiederholt ausgeführt.</span><span class="sxs-lookup"><span data-stu-id="469d6-124">Describes the frequency, in days, in which a task recurs.</span></span>  <br/> |
|[<span data-ttu-id="469d6-125">DailyRegeneration</span><span class="sxs-lookup"><span data-stu-id="469d6-125">DailyRegeneration</span></span>](dailyregeneration.md) <br/> |<span data-ttu-id="469d6-126">Beschreibt, wie viele Tage nach dem Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.</span><span class="sxs-lookup"><span data-stu-id="469d6-126">Describes how many days after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="469d6-127">WeeklyRegeneration</span><span class="sxs-lookup"><span data-stu-id="469d6-127">WeeklyRegeneration</span></span>](weeklyregeneration.md) <br/> |<span data-ttu-id="469d6-128">Beschreibt, wie viele Wochen nach Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.</span><span class="sxs-lookup"><span data-stu-id="469d6-128">Describes how many weeks after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="469d6-129">MonthlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="469d6-129">MonthlyRegeneration</span></span>](monthlyregeneration.md) <br/> |<span data-ttu-id="469d6-130">Beschreibt, wie viele Monate nach Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.</span><span class="sxs-lookup"><span data-stu-id="469d6-130">Describes how many months after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="469d6-131">YearlyRegeneration</span><span class="sxs-lookup"><span data-stu-id="469d6-131">YearlyRegeneration</span></span>](yearlyregeneration.md) <br/> |<span data-ttu-id="469d6-132">Beschreibt, wie viele Jahre nach Abschluss des Vorgangs aktuelle das nächste Vorkommen fällig werden.</span><span class="sxs-lookup"><span data-stu-id="469d6-132">Describes how many years after the completion of the current task the next occurrence will be due.</span></span>  <br/> |
|[<span data-ttu-id="469d6-133">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-133">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="469d6-134">Beschreibt ein Serienmuster, die nicht über einen definierten Enddatum verfügt.</span><span class="sxs-lookup"><span data-stu-id="469d6-134">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="469d6-135">Die Verwendung dieses Elements schließt die Verwendung der [EndDateRecurrence](enddaterecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="469d6-135">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="469d6-136">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-136">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="469d6-137">Beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="469d6-137">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="469d6-138">Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="469d6-138">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> <span data-ttu-id="469d6-139">[EndDateRecurrence](enddaterecurrence.md) kann nicht zusammen mit einem Muster mithilfe verwendet werden.</span><span class="sxs-lookup"><span data-stu-id="469d6-139">[EndDateRecurrence](enddaterecurrence.md) cannot be used together with a regeneration pattern.</span></span>  <br/> |
|[<span data-ttu-id="469d6-140">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="469d6-140">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="469d6-141">Beschreibt das Startdatum und die Anzahl der Vorkommen eines sich wiederholenden-Elements.</span><span class="sxs-lookup"><span data-stu-id="469d6-141">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="469d6-142">Die Verwendung dieses Elements schließt die Verwendung der [NoEndRecurrence](noendrecurrence.md) und [EndDateRecurrence](enddaterecurrence.md) Elemente.</span><span class="sxs-lookup"><span data-stu-id="469d6-142">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="469d6-143">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="469d6-143">Parent elements</span></span>

|<span data-ttu-id="469d6-144">**Element**</span><span class="sxs-lookup"><span data-stu-id="469d6-144">**Element**</span></span>|<span data-ttu-id="469d6-145">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="469d6-145">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="469d6-146">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="469d6-146">Task</span></span>](task.md) <br/> |<span data-ttu-id="469d6-147">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="469d6-147">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="469d6-148">Hinweise</span><span class="sxs-lookup"><span data-stu-id="469d6-148">Remarks</span></span>

<span data-ttu-id="469d6-149">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="469d6-149">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="469d6-150">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="469d6-150">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="469d6-151">Namespace</span><span class="sxs-lookup"><span data-stu-id="469d6-151">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="469d6-152">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="469d6-152">Schema name</span></span>  <br/> |<span data-ttu-id="469d6-153">Schematypen</span><span class="sxs-lookup"><span data-stu-id="469d6-153">Types schema</span></span>  <br/> |
|<span data-ttu-id="469d6-154">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="469d6-154">Validation file</span></span>  <br/> |<span data-ttu-id="469d6-155">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="469d6-155">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="469d6-156">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="469d6-156">Can be empty</span></span>  <br/> |<span data-ttu-id="469d6-157">False</span><span class="sxs-lookup"><span data-stu-id="469d6-157">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="469d6-158">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="469d6-158">See also</span></span>



- [<span data-ttu-id="469d6-159">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="469d6-159">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

