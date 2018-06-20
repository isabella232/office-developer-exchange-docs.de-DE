---
title: AbsoluteYearlyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- AbsoluteYearlyRecurrence
api_type:
- schema
ms.assetid: 96f53e2c-3893-4f6e-a78a-ac179f45c5db
description: Das AbsoluteYearlyRecurrence-Element stellt ein jährliches Serienmuster dar.
ms.openlocfilehash: 205da336a6a6ca4fd39120e83ab264e1543354e8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758352"
---
# <a name="absoluteyearlyrecurrence"></a><span data-ttu-id="cd4bc-103">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="cd4bc-103">AbsoluteYearlyRecurrence</span></span>

<span data-ttu-id="cd4bc-104">Das **AbsoluteYearlyRecurrence** -Element stellt ein jährliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-104">The **AbsoluteYearlyRecurrence** element represents a yearly recurrence pattern.</span></span> 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 <span data-ttu-id="cd4bc-105">**AbsoluteYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="cd4bc-105">**AbsoluteYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd4bc-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd4bc-106">Attributes and elements</span></span>

<span data-ttu-id="cd4bc-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd4bc-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd4bc-108">Attributes</span></span>

<span data-ttu-id="cd4bc-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd4bc-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd4bc-110">Child elements</span></span>

|<span data-ttu-id="cd4bc-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd4bc-111">**Element**</span></span>|<span data-ttu-id="cd4bc-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd4bc-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd4bc-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="cd4bc-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="cd4bc-114">Beschreibt den Tag im Monat auf dem eine Terminserie auftritt.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-114">Describes the day in a month on which a recurring item occurs.</span></span> <span data-ttu-id="cd4bc-115">Der Bereich der Werte für diese Eigenschaft ist 1 und 31.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="cd4bc-116">Wenn dieser Wert für einen bestimmten Monat größer als die Anzahl der Tage des Monats ist, wird der letzte Tag des Monats für diese Eigenschaft verwendet.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="cd4bc-117">Month (Element Serie)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="cd4bc-118">Beschreibt den Monat, in dem eine jährliche Terminserie erfolgt.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-118">Describes the month in which a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd4bc-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd4bc-119">Parent elements</span></span>

|<span data-ttu-id="cd4bc-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd4bc-120">**Element**</span></span>|<span data-ttu-id="cd4bc-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd4bc-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd4bc-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="cd4bc-123">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="cd4bc-124">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="cd4bc-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="cd4bc-125">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd4bc-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="cd4bc-126">Remarks</span></span>

<span data-ttu-id="cd4bc-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="cd4bc-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd4bc-128">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="cd4bc-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd4bc-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd4bc-129">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd4bc-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd4bc-130">Schema Name</span></span>  <br/> |<span data-ttu-id="cd4bc-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cd4bc-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd4bc-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd4bc-132">Validation File</span></span>  <br/> |<span data-ttu-id="cd4bc-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd4bc-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd4bc-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="cd4bc-134">Can Be Empty</span></span>  <br/> |<span data-ttu-id="cd4bc-135">False</span><span class="sxs-lookup"><span data-stu-id="cd4bc-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd4bc-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd4bc-136">See also</span></span>

- [<span data-ttu-id="cd4bc-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="cd4bc-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

