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
ms.openlocfilehash: 19b617dfd5c0a3d206d62439c880da084fd5f5f0
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460414"
---
# <a name="absoluteyearlyrecurrence"></a><span data-ttu-id="23ee7-103">AbsoluteYearlyRecurrence</span><span class="sxs-lookup"><span data-stu-id="23ee7-103">AbsoluteYearlyRecurrence</span></span>

<span data-ttu-id="23ee7-104">Das **AbsoluteYearlyRecurrence** -Element stellt ein jährliches Serienmuster dar.</span><span class="sxs-lookup"><span data-stu-id="23ee7-104">The **AbsoluteYearlyRecurrence** element represents a yearly recurrence pattern.</span></span> 
  
```xml
<AbsoluteYearlyRecurrence>
   <DayOfMonth/>
   <Month/>
</AbsoluteYearlyRecurrence>
```

 <span data-ttu-id="23ee7-105">**AbsoluteYearlyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="23ee7-105">**AbsoluteYearlyRecurrencePatternType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="23ee7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="23ee7-106">Attributes and elements</span></span>

<span data-ttu-id="23ee7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="23ee7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="23ee7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="23ee7-108">Attributes</span></span>

<span data-ttu-id="23ee7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="23ee7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="23ee7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23ee7-110">Child elements</span></span>

|<span data-ttu-id="23ee7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="23ee7-111">**Element**</span></span>|<span data-ttu-id="23ee7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23ee7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23ee7-113">DayOfMonth</span><span class="sxs-lookup"><span data-stu-id="23ee7-113">DayOfMonth</span></span>](dayofmonth.md) <br/> |<span data-ttu-id="23ee7-114">Beschreibt den Tag in einem Monat, an dem ein wiederkehrendes Element auftritt.</span><span class="sxs-lookup"><span data-stu-id="23ee7-114">Describes the day in a month on which a recurring item occurs.</span></span> <span data-ttu-id="23ee7-115">Der Wertebereich für diese Eigenschaft ist 1 bis 31.</span><span class="sxs-lookup"><span data-stu-id="23ee7-115">The range of values for this property is 1 to 31.</span></span> <span data-ttu-id="23ee7-116">Wenn dieser Wert für einen bestimmten Monat größer ist als die Anzahl der Tage im Monat, wird der letzte Tag des Monats für diese Eigenschaft angenommen.</span><span class="sxs-lookup"><span data-stu-id="23ee7-116">If for a particular month this value is larger than the number of days in the month, the last day of the month is assumed for this property.</span></span>  <br/> |
|[<span data-ttu-id="23ee7-117">Month (Elementserie)</span><span class="sxs-lookup"><span data-stu-id="23ee7-117">Month (Item Recurrence)</span></span>](month-item-recurrence.md) <br/> |<span data-ttu-id="23ee7-118">Beschreibt den Monat, in dem ein jährliches wiederkehrendes Element auftritt.</span><span class="sxs-lookup"><span data-stu-id="23ee7-118">Describes the month in which a yearly recurring item occurs.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="23ee7-119">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="23ee7-119">Parent elements</span></span>

|<span data-ttu-id="23ee7-120">**Element**</span><span class="sxs-lookup"><span data-stu-id="23ee7-120">**Element**</span></span>|<span data-ttu-id="23ee7-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="23ee7-121">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="23ee7-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="23ee7-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="23ee7-123">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="23ee7-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="23ee7-124">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="23ee7-124">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="23ee7-125">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="23ee7-125">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="23ee7-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="23ee7-126">Remarks</span></span>

<span data-ttu-id="23ee7-127">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="23ee7-127">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="23ee7-128">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="23ee7-128">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="23ee7-129">Namespace</span><span class="sxs-lookup"><span data-stu-id="23ee7-129">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="23ee7-130">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="23ee7-130">Schema Name</span></span>  <br/> |<span data-ttu-id="23ee7-131">Schematypen</span><span class="sxs-lookup"><span data-stu-id="23ee7-131">Types schema</span></span>  <br/> |
|<span data-ttu-id="23ee7-132">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="23ee7-132">Validation File</span></span>  <br/> |<span data-ttu-id="23ee7-133">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="23ee7-133">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="23ee7-134">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="23ee7-134">Can Be Empty</span></span>  <br/> |<span data-ttu-id="23ee7-135">False</span><span class="sxs-lookup"><span data-stu-id="23ee7-135">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="23ee7-136">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="23ee7-136">See also</span></span>

- [<span data-ttu-id="23ee7-137">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="23ee7-137">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

