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
ms.openlocfilehash: f4613fa71a9164c45b60a82f675959817cd4bdd5
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758357"
---
# <a name="absolutemonthlyrecurrence"></a><span data-ttu-id="c9d69-103">AbsoluteMonthlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="c9d69-103">AbsoluteMonthlyRecurrence</span></span>

<span data-ttu-id="c9d69-104">Das **AbsoluteMonthlyRecurrence** -Element stellt ein monatliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="c9d69-104">The **AbsoluteMonthlyRecurrence** element represents a monthly recurrence pattern.</span></span> 
  
```xml
<AbsoluteMonthlyRecurrence>
   <Interval/>
   <DayOfMonth/>
</AbsoluteMonthlyRecurrence>
```

 <span data-ttu-id="c9d69-105">**AbsoluteMonthlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="c9d69-105">**AbsoluteMonthlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="c9d69-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d69-106">Attributes and elements</span></span>

<span data-ttu-id="c9d69-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="c9d69-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="c9d69-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="c9d69-108">Attributes</span></span>

<span data-ttu-id="c9d69-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="c9d69-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="c9d69-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d69-110">Child elements</span></span>

|<span data-ttu-id="c9d69-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9d69-111">**Element**</span></span>|<span data-ttu-id="c9d69-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9d69-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9d69-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="c9d69-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="c9d69-114">Beschreibt den Tag im Monat, den eine Terminserie auftritt.</span><span class="sxs-lookup"><span data-stu-id="c9d69-114">Describes the day in a month that a recurring item occurs.</span></span> <span data-ttu-id="c9d69-115">Der Bereich der Werte für diese Eigenschaft ist 1 und 31.</span><span class="sxs-lookup"><span data-stu-id="c9d69-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="c9d69-116">Wenn dieser Wert für einen bestimmten Monat größer als die Anzahl der Tage des Monats ist, wird der letzte Tag des Monats für diese Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="c9d69-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="c9d69-117">Intervall</span><span class="sxs-lookup"><span data-stu-id="c9d69-117">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="c9d69-118">Definiert das Intervall zwischen zwei aufeinander folgenden Terminserien.</span><span class="sxs-lookup"><span data-stu-id="c9d69-118">Defines the interval between two consecutive recurring items.</span></span> <span data-ttu-id="c9d69-119">Beispielsweise tritt das **Intervall** -Element den Wert 5 hat, das Serienelement alle 5 Monate.</span><span class="sxs-lookup"><span data-stu-id="c9d69-119">For example, if the **Interval** element has a value of 5, the recurring item occurs every 5 months.</span></span> <span data-ttu-id="c9d69-120">Der gültige Wertebereich liegt zwischen 1 und 99.</span><span class="sxs-lookup"><span data-stu-id="c9d69-120">The range of valid values is from 1 to 99.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="c9d69-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="c9d69-121">Parent elements</span></span>

|<span data-ttu-id="c9d69-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="c9d69-122">**Element**</span></span>|<span data-ttu-id="c9d69-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="c9d69-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="c9d69-124">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c9d69-124">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="c9d69-125">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="c9d69-125">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="c9d69-126">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="c9d69-126">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="c9d69-127">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="c9d69-127">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c9d69-128">Hinweise</span><span class="sxs-lookup"><span data-stu-id="c9d69-128">Remarks</span></span>

<span data-ttu-id="c9d69-129">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="c9d69-129">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="c9d69-130">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="c9d69-130">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="c9d69-131">Namespace</span><span class="sxs-lookup"><span data-stu-id="c9d69-131">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="c9d69-132">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="c9d69-132">Schema Name</span></span>  <br/> |<span data-ttu-id="c9d69-133">Schematypen</span><span class="sxs-lookup"><span data-stu-id="c9d69-133">Types schema</span></span>  <br/> |
|<span data-ttu-id="c9d69-134">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="c9d69-134">Validation File</span></span>  <br/> |<span data-ttu-id="c9d69-135">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="c9d69-135">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="c9d69-136">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="c9d69-136">Can Be Empty</span></span>  <br/> |<span data-ttu-id="c9d69-137">False</span><span class="sxs-lookup"><span data-stu-id="c9d69-137">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c9d69-138">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="c9d69-138">See also</span></span>

- [<span data-ttu-id="c9d69-139">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="c9d69-139">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

