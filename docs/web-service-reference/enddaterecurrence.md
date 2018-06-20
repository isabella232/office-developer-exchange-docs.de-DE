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
ms.lasthandoff: 06/11/2018
ms.locfileid: "19758234"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="b2ccd-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="b2ccd-103">EndDateRecurrence</span></span>

<span data-ttu-id="b2ccd-104">Das Element **EndDateRecurrence** beschreibt das Startdatum und das Enddatum des ein Element Serienmuster.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="b2ccd-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="b2ccd-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b2ccd-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b2ccd-106">Attributes and elements</span></span>

<span data-ttu-id="b2ccd-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b2ccd-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="b2ccd-108">Attributes</span></span>

<span data-ttu-id="b2ccd-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b2ccd-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2ccd-110">Child elements</span></span>

|<span data-ttu-id="b2ccd-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="b2ccd-111">**Element**</span></span>|<span data-ttu-id="b2ccd-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2ccd-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2ccd-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="b2ccd-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="b2ccd-114">Stellt das Startdatum einer Aufgabenserie oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="b2ccd-115">EndDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="b2ccd-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="b2ccd-116">Stellt das Enddatum einer Aufgabenserie oder Kalenderelement.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b2ccd-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b2ccd-117">Parent elements</span></span>

|<span data-ttu-id="b2ccd-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="b2ccd-118">**Element**</span></span>|<span data-ttu-id="b2ccd-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b2ccd-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b2ccd-120">Serie (RecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b2ccd-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="b2ccd-121">Das Serienmuster für Kalenderelemente und Besprechungsanfragen enthält.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="b2ccd-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="b2ccd-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="b2ccd-123">Das Serienmuster für wiederkehrende Aufgaben enthält.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b2ccd-124">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b2ccd-124">Remarks</span></span>

<span data-ttu-id="b2ccd-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b2ccd-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b2ccd-126">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b2ccd-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b2ccd-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="b2ccd-127">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b2ccd-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b2ccd-128">Schema name</span></span>  <br/> |<span data-ttu-id="b2ccd-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b2ccd-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="b2ccd-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b2ccd-130">Validation file</span></span>  <br/> |<span data-ttu-id="b2ccd-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b2ccd-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b2ccd-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="b2ccd-132">Can be empty</span></span>  <br/> |<span data-ttu-id="b2ccd-133">False</span><span class="sxs-lookup"><span data-stu-id="b2ccd-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b2ccd-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b2ccd-134">See also</span></span>



- [<span data-ttu-id="b2ccd-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="b2ccd-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

