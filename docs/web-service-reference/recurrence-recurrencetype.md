---
title: Serie (serietype)
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
description: Das Serienelement enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.
ms.openlocfilehash: d00445c75fb35c3bb99eeed06e30cb1cf2883597
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44529889"
---
# <a name="recurrence-recurrencetype"></a><span data-ttu-id="8585a-103">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="8585a-103">Recurrence (RecurrenceType)</span></span>

<span data-ttu-id="8585a-104">Das **Serien** Element enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="8585a-104">The **Recurrence** element contains the recurrence pattern for calendar items and meeting requests.</span></span> 
  
```xml
<Recurrence>
      <RelativeYearlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/>
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeYearlyRecurrence/> 
      <NumberedRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <DailyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <EndDateRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteMonthlyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <NoEndRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NoEndRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <WeeklyRecurrence/> 
      <NumberedRecurrence/> 
</Recurrence>
```

```xml
<Recurrence>
      <AbsoluteYearlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

```xml
<Recurrence>
      <RelativeMonthlyRecurrence/> 
      <EndDateRecurrence/>
</Recurrence>
```

<span data-ttu-id="8585a-105">**RecurrenceType**</span><span class="sxs-lookup"><span data-stu-id="8585a-105">**RecurrenceType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8585a-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8585a-106">Attributes and elements</span></span>

<span data-ttu-id="8585a-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8585a-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8585a-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8585a-108">Attributes</span></span>

<span data-ttu-id="8585a-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8585a-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8585a-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8585a-110">Child elements</span></span>

|<span data-ttu-id="8585a-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8585a-111">**Element**</span></span>|<span data-ttu-id="8585a-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8585a-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8585a-113">RelativeYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-113">RelativeYearlyRecurrence</span></span>](relativeyearlyrecurrence.md) <br/> |<span data-ttu-id="8585a-114">Beschreibt ein relatives jährliches Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="8585a-114">Describes a relative yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="8585a-115">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-115">AbsoluteYearlyRecurrence</span></span>](absoluteyearlyrecurrence.md) <br/> |<span data-ttu-id="8585a-116">Stellt ein jährliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="8585a-116">Represents a yearly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="8585a-117">RelativeMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-117">RelativeMonthlyRecurrence</span></span>](relativemonthlyrecurrence.md) <br/> |<span data-ttu-id="8585a-118">Beschreibt ein relatives monatliches Serienmuster für ein wiederkehrendes Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="8585a-118">Describes a relative monthly recurrence pattern for a recurring calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8585a-119">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-119">AbsoluteMonthlyRecurrence</span></span>](absolutemonthlyrecurrence.md) <br/> |<span data-ttu-id="8585a-120">Stellt ein monatliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="8585a-120">Represents a monthly recurrence pattern.</span></span>  <br/> |
|[<span data-ttu-id="8585a-121">WeeklyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-121">WeeklyRecurrence</span></span>](weeklyrecurrence.md) <br/> |<span data-ttu-id="8585a-122">Beschreibt die Häufigkeit in Wochen und die Tage, an denen ein Kalenderelement oder eine Aufgabe erneut auftritt.</span><span class="sxs-lookup"><span data-stu-id="8585a-122">Describes the frequency, in weeks, and the days that a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="8585a-123">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-123">DailyRecurrence</span></span>](dailyrecurrence.md) <br/> |<span data-ttu-id="8585a-124">Beschreibt die Häufigkeit in Tagen, in der ein Kalenderelement oder eine Aufgabe erneut auftritt.</span><span class="sxs-lookup"><span data-stu-id="8585a-124">Describes the frequency, in days, in which a calendar item or task recurs.</span></span>  <br/> |
|[<span data-ttu-id="8585a-125">NoEndRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-125">NoEndRecurrence</span></span>](noendrecurrence.md) <br/> |<span data-ttu-id="8585a-126">Beschreibt ein Serienmuster, das nicht über ein definiertes Enddatum verfügt.</span><span class="sxs-lookup"><span data-stu-id="8585a-126">Describes a recurrence pattern that does not have a defined end date.</span></span>  <br/> <span data-ttu-id="8585a-127">Die Verwendung dieses Elements schließt die Verwendung der Elemente [EndDateRecurrence](enddaterecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) aus.</span><span class="sxs-lookup"><span data-stu-id="8585a-127">The use of this element excludes the use of the [EndDateRecurrence](enddaterecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="8585a-128">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-128">EndDateRecurrence</span></span>](enddaterecurrence.md) <br/> |<span data-ttu-id="8585a-129">Beschreibt das Startdatum und das Enddatum eines Element Serienmusters.</span><span class="sxs-lookup"><span data-stu-id="8585a-129">Describes the start date and the end date of an item recurrence pattern.</span></span>  <br/> <span data-ttu-id="8585a-130">Die Verwendung dieses Elements schließt die Verwendung der Elemente [NoEndRecurrence](noendrecurrence.md) und [NumberedRecurrence](numberedrecurrence.md) aus.</span><span class="sxs-lookup"><span data-stu-id="8585a-130">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [NumberedRecurrence](numberedrecurrence.md) elements.</span></span>  <br/> |
|[<span data-ttu-id="8585a-131">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="8585a-131">NumberedRecurrence</span></span>](numberedrecurrence.md) <br/> |<span data-ttu-id="8585a-132">Beschreibt das Startdatum und die Anzahl der Vorkommen eines wiederkehrenden Elements.</span><span class="sxs-lookup"><span data-stu-id="8585a-132">Describes the start date and the number of occurrences of a recurring item.</span></span>  <br/> <span data-ttu-id="8585a-133">Die Verwendung dieses Elements schließt die Verwendung der Elemente [NoEndRecurrence](noendrecurrence.md) und [EndDateRecurrence](enddaterecurrence.md) aus.</span><span class="sxs-lookup"><span data-stu-id="8585a-133">The use of this element excludes the use of the [NoEndRecurrence](noendrecurrence.md) and [EndDateRecurrence](enddaterecurrence.md) elements.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8585a-134">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8585a-134">Parent elements</span></span>

|<span data-ttu-id="8585a-135">**Element**</span><span class="sxs-lookup"><span data-stu-id="8585a-135">**Element**</span></span>|<span data-ttu-id="8585a-136">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8585a-136">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8585a-137">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="8585a-137">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="8585a-138">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="8585a-138">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="8585a-139">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="8585a-139">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="8585a-140">Stellt eine Besprechungsanfrage im Exchange-Informationsspeicher</span><span class="sxs-lookup"><span data-stu-id="8585a-140">Represents a meeting request in the Exchange store</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8585a-141">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8585a-141">Remarks</span></span>

<span data-ttu-id="8585a-142">Dieses Element ist gültig, wenn [CalendarItemType](calendaritemtype.md) den RecurringMaster-Wert aufweist.</span><span class="sxs-lookup"><span data-stu-id="8585a-142">This element is valid if [CalendarItemType](calendaritemtype.md) has the RecurringMaster value.</span></span> 
  
<span data-ttu-id="8585a-143">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8585a-143">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8585a-144">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8585a-144">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8585a-145">Namespace</span><span class="sxs-lookup"><span data-stu-id="8585a-145">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8585a-146">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8585a-146">Schema name</span></span>  <br/> |<span data-ttu-id="8585a-147">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8585a-147">Types schema</span></span>  <br/> |
|<span data-ttu-id="8585a-148">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8585a-148">Validation file</span></span>  <br/> |<span data-ttu-id="8585a-149">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8585a-149">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8585a-150">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8585a-150">Can be empty</span></span>  <br/> |<span data-ttu-id="8585a-151">False</span><span class="sxs-lookup"><span data-stu-id="8585a-151">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8585a-152">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8585a-152">See also</span></span>

- [<span data-ttu-id="8585a-153">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8585a-153">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

