---
title: EndDateRecurrence
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndDateRecurrence
api_type:
- schema
ms.assetid: a5ee2504-db84-49ee-870c-cca9269f2e26
description: Das Element EndDateRecurrence beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.
ms.openlocfilehash: 73450bf69c6b122e806d85011975159e348ad740
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758234"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="e5565-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="e5565-103">EndDateRecurrence</span></span>

<span data-ttu-id="e5565-104">Das Element **EndDateRecurrence** beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="e5565-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="e5565-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="e5565-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e5565-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e5565-106">Attributes and elements</span></span>

<span data-ttu-id="e5565-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e5565-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e5565-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="e5565-108">Attributes</span></span>

<span data-ttu-id="e5565-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="e5565-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e5565-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5565-110">Child elements</span></span>

|<span data-ttu-id="e5565-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5565-111">**Element**</span></span>|<span data-ttu-id="e5565-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5565-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5565-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="e5565-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="e5565-114">Stellt das Startdatum einer Aufgabenserie oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="e5565-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="e5565-115">EndDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="e5565-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="e5565-116">Stellt das Enddatum einer Aufgabenserie oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="e5565-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e5565-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e5565-117">Parent elements</span></span>

|<span data-ttu-id="e5565-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="e5565-118">**Element**</span></span>|<span data-ttu-id="e5565-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e5565-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e5565-120">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="e5565-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="e5565-121">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="e5565-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="e5565-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="e5565-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="e5565-123">Das Serienmuster für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="e5565-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e5565-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="e5565-124">Remarks</span></span>

<span data-ttu-id="e5565-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e5565-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e5565-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="e5565-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e5565-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="e5565-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e5565-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e5565-128">Schema name</span></span>  <br/> |<span data-ttu-id="e5565-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e5565-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="e5565-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e5565-130">Validation file</span></span>  <br/> |<span data-ttu-id="e5565-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e5565-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e5565-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="e5565-132">Can be empty</span></span>  <br/> |<span data-ttu-id="e5565-133">False</span><span class="sxs-lookup"><span data-stu-id="e5565-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e5565-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e5565-134">See also</span></span>



- [<span data-ttu-id="e5565-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="e5565-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

