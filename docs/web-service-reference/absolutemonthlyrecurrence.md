---
title: AbsoluteMonthlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteMonthlyRecurrence
api_type:
- schema
ms.assetid: 178fa0ae-9dfc-417f-933c-d657d31c2161
description: Das AbsoluteMonthlyRecurrence-Element stellt ein monatliches Serienmuster dar.
ms.openlocfilehash: 3176cd30a1cfe7b2310f960ce377ab7a277e795a
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460435"
---
# <a name="absolutemonthlyrecurrence"></a><span data-ttu-id="df9c7-103">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="df9c7-103">AbsoluteMonthlyRecurrence</span></span>

<span data-ttu-id="df9c7-104">Das **AbsoluteMonthlyRecurrence** -Element stellt ein monatliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="df9c7-104">The **AbsoluteMonthlyRecurrence** element represents a monthly recurrence pattern.</span></span> 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 <span data-ttu-id="df9c7-105">**AbsoluteMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="df9c7-105">**AbsoluteMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="df9c7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="df9c7-106">Attributes and elements</span></span>

<span data-ttu-id="df9c7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="df9c7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="df9c7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="df9c7-108">Attributes</span></span>

<span data-ttu-id="df9c7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="df9c7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="df9c7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df9c7-110">Child elements</span></span>

|<span data-ttu-id="df9c7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="df9c7-111">**Element**</span></span>|<span data-ttu-id="df9c7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df9c7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df9c7-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="df9c7-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="df9c7-114">Beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt.</span><span class="sxs-lookup"><span data-stu-id="df9c7-114">Describes the day in a month that a recurring item occurs.</span></span> <span data-ttu-id="df9c7-115">Der Wertebereich für diese Eigenschaft ist 1 bis 31.</span><span class="sxs-lookup"><span data-stu-id="df9c7-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="df9c7-116">Wenn dieser Wert für einen bestimmten Monat größer ist als die Anzahl der Tage im Monat, wird der letzte Tag des Monats für diese Eigenschaft angenommen.</span><span class="sxs-lookup"><span data-stu-id="df9c7-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="df9c7-117">Intervall</span><span class="sxs-lookup"><span data-stu-id="df9c7-117">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="df9c7-118">Definiert das Intervall zwischen zwei aufeinander folgenden wiederkehrenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="df9c7-118">Defines the interval between two consecutive recurring items.</span></span> <span data-ttu-id="df9c7-119">Wenn das **Interval** -Element beispielsweise den Wert 5 aufweist, tritt das wiederkehrende Element alle 5 Monate auf.</span><span class="sxs-lookup"><span data-stu-id="df9c7-119">For example, if the **Interval** element has a value of 5, the recurring item occurs every 5 months.</span></span> <span data-ttu-id="df9c7-120">Der Bereich der gültigen Werte liegt zwischen 1 und 99.</span><span class="sxs-lookup"><span data-stu-id="df9c7-120">The range of valid values is from 1 to 99.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="df9c7-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="df9c7-121">Parent elements</span></span>

|<span data-ttu-id="df9c7-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="df9c7-122">**Element**</span></span>|<span data-ttu-id="df9c7-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="df9c7-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="df9c7-124">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="df9c7-124">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="df9c7-125">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="df9c7-125">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="df9c7-126">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="df9c7-126">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="df9c7-127">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="df9c7-127">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df9c7-128">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="df9c7-128">Remarks</span></span>

<span data-ttu-id="df9c7-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="df9c7-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="df9c7-130">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="df9c7-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="df9c7-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="df9c7-131">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="df9c7-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="df9c7-132">Schema Name</span></span>  <br/> |<span data-ttu-id="df9c7-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="df9c7-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="df9c7-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="df9c7-134">Validation File</span></span>  <br/> |<span data-ttu-id="df9c7-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="df9c7-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="df9c7-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="df9c7-136">Can Be Empty</span></span>  <br/> |<span data-ttu-id="df9c7-137">False</span><span class="sxs-lookup"><span data-stu-id="df9c7-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="df9c7-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="df9c7-138">See also</span></span>

- [<span data-ttu-id="df9c7-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="df9c7-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

