---
title: DailyRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DailyRecurrence
api_type:
- schema
ms.assetid: 0aaf265d-b723-49c6-8e9c-9ba60141e9ab
description: Das DailyRecurrence-Element beschreibt die Häufigkeit in Tagen, in der ein Kalenderelement oder eine Aufgabe erneut auftritt.
ms.openlocfilehash: d18a04ced19c87996c3a092f6668ab00c5a3f006
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44462171"
---
# <a name="dailyrecurrence"></a><span data-ttu-id="8d8d8-103">DailyRecurrence</span><span class="sxs-lookup"><span data-stu-id="8d8d8-103">DailyRecurrence</span></span>

<span data-ttu-id="8d8d8-104">Das **DailyRecurrence** -Element beschreibt die Häufigkeit in Tagen, in der ein Kalenderelement oder eine Aufgabe erneut auftritt.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-104">The **DailyRecurrence** element describes the frequency, in days, in which a calendar item or a task recurs.</span></span> 
  
```xml
<DailyRecurrence>
   <Interval/>
</DailyRecurrence>
```

<span data-ttu-id="8d8d8-105">**DailyRecurrencePatternType**</span><span class="sxs-lookup"><span data-stu-id="8d8d8-105">**DailyRecurrencePatternType**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="8d8d8-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="8d8d8-106">Attributes and elements</span></span>

<span data-ttu-id="8d8d8-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="8d8d8-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="8d8d8-108">Attributes</span></span>

<span data-ttu-id="8d8d8-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="8d8d8-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d8d8-110">Child elements</span></span>

|<span data-ttu-id="8d8d8-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d8d8-111">**Element**</span></span>|<span data-ttu-id="8d8d8-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d8d8-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d8d8-113">Intervall</span><span class="sxs-lookup"><span data-stu-id="8d8d8-113">Interval</span></span>](interval.md) <br/> |<span data-ttu-id="8d8d8-114">Definiert das Intervall in Tagen zwischen zwei aufeinander folgenden wiederkehrenden Elementen.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-114">Defines the interval, in days, between two consecutive recurring items.</span></span> <span data-ttu-id="8d8d8-115">Der Wert muss im Bereich von 1 bis 999 liegen.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-115">The value must be in the range from 1 to 999.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="8d8d8-116">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="8d8d8-116">Parent elements</span></span>

|<span data-ttu-id="8d8d8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="8d8d8-117">**Element**</span></span>|<span data-ttu-id="8d8d8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="8d8d8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="8d8d8-119">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="8d8d8-119">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="8d8d8-120">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-120">Contains recurrence information for recurring tasks.</span></span>  <br/> |
|[<span data-ttu-id="8d8d8-121">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="8d8d8-121">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="8d8d8-122">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-122">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="8d8d8-123">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="8d8d8-123">Remarks</span></span>

<span data-ttu-id="8d8d8-124">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="8d8d8-124">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="8d8d8-125">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="8d8d8-125">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="8d8d8-126">Namespace</span><span class="sxs-lookup"><span data-stu-id="8d8d8-126">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="8d8d8-127">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="8d8d8-127">Schema name</span></span>  <br/> |<span data-ttu-id="8d8d8-128">Schematypen</span><span class="sxs-lookup"><span data-stu-id="8d8d8-128">Types schema</span></span>  <br/> |
|<span data-ttu-id="8d8d8-129">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="8d8d8-129">Validation file</span></span>  <br/> |<span data-ttu-id="8d8d8-130">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="8d8d8-130">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="8d8d8-131">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="8d8d8-131">Can be empty</span></span>  <br/> |<span data-ttu-id="8d8d8-132">False</span><span class="sxs-lookup"><span data-stu-id="8d8d8-132">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8d8d8-133">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="8d8d8-133">See also</span></span>

- [<span data-ttu-id="8d8d8-134">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="8d8d8-134">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

