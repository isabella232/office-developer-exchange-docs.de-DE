---
title: NumberedRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- NumberedRecurrence
api_type:
- schema
ms.assetid: 53746909-ef21-4764-8715-a7769b943cca
description: Das NumberedRecurrence-Element wird das Startdatum und die Anzahl der Vorkommen eines sich wiederholenden-Elements beschrieben.
ms.openlocfilehash: 01fbf831fa7ff378221d4db3d873af730ac564d8
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830628"
---
# <a name="numberedrecurrence"></a><span data-ttu-id="e3a38-103">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="e3a38-103">NumberedRecurrence</span></span>

<span data-ttu-id="e3a38-104">Das **NumberedRecurrence** -Element wird das Startdatum und die Anzahl der Vorkommen eines sich wiederholenden-Elements beschrieben.</span><span class="sxs-lookup"><span data-stu-id="e3a38-104">The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 <span data-ttu-id="e3a38-105">**NumberedRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="e3a38-105">**NumberedRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e3a38-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e3a38-106">Attributes and elements</span></span>

<span data-ttu-id="e3a38-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e3a38-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e3a38-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e3a38-108">Attributes</span></span>

<span data-ttu-id="e3a38-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e3a38-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e3a38-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3a38-110">Child elements</span></span>

|<span data-ttu-id="e3a38-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3a38-111">**Element**</span></span>|<span data-ttu-id="e3a38-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3a38-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3a38-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="e3a38-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="e3a38-114">Stellt das Startdatum einer Aufgabenserie oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="e3a38-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e3a38-115">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="e3a38-115">NumberOfOccurrences</span></span>](numberofoccurrences.md) <br/> |<span data-ttu-id="e3a38-116">Enthält die Anzahl der Vorkommen eines sich wiederholenden-Elements an.</span><span class="sxs-lookup"><span data-stu-id="e3a38-116">Contains the number of occurrences of a recurring item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e3a38-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e3a38-117">Parent elements</span></span>

|<span data-ttu-id="e3a38-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e3a38-118">**Element**</span></span>|<span data-ttu-id="e3a38-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e3a38-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e3a38-120">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="e3a38-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="e3a38-121">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="e3a38-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="e3a38-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="e3a38-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="e3a38-123">Serieninformationen für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="e3a38-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e3a38-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e3a38-124">Remarks</span></span>

<span data-ttu-id="e3a38-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e3a38-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e3a38-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e3a38-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e3a38-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="e3a38-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e3a38-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e3a38-128">Schema name</span></span>  <br/> |<span data-ttu-id="e3a38-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e3a38-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="e3a38-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e3a38-130">Validation file</span></span>  <br/> |<span data-ttu-id="e3a38-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e3a38-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e3a38-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e3a38-132">Can be empty</span></span>  <br/> |<span data-ttu-id="e3a38-133">False</span><span class="sxs-lookup"><span data-stu-id="e3a38-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e3a38-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e3a38-134">See also</span></span>



- [<span data-ttu-id="e3a38-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e3a38-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

