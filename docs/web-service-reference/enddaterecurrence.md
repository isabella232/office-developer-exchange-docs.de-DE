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
description: Das EndDateRecurrence-Element beschreibt das Startdatum und das Enddatum eines Element Serienmusters.
ms.openlocfilehash: e8ae72012e5bcac8d8b2a06b6d3a9b3a7caf30d7
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44460148"
---
# <a name="enddaterecurrence"></a><span data-ttu-id="17d00-103">EndDateRecurrence</span><span class="sxs-lookup"><span data-stu-id="17d00-103">EndDateRecurrence</span></span>

<span data-ttu-id="17d00-104">Das **EndDateRecurrence** -Element beschreibt das Startdatum und das Enddatum eines Element Serienmusters.</span><span class="sxs-lookup"><span data-stu-id="17d00-104">The **EndDateRecurrence** element describes the start date and the end date of an item recurrence pattern.</span></span> 
  
```xml
<EndDateRecurrence>
   <StartDate/>
   <EndDate/>
</EndDateRecurrence>
```

 <span data-ttu-id="17d00-105">**EndDateRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="17d00-105">**EndDateRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="17d00-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="17d00-106">Attributes and elements</span></span>

<span data-ttu-id="17d00-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="17d00-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="17d00-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="17d00-108">Attributes</span></span>

<span data-ttu-id="17d00-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="17d00-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="17d00-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17d00-110">Child elements</span></span>

|<span data-ttu-id="17d00-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="17d00-111">**Element**</span></span>|<span data-ttu-id="17d00-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17d00-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17d00-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="17d00-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="17d00-114">Stellt das Startdatum eines periodischen Vorgangs oder Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="17d00-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="17d00-115">EndDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="17d00-115">EndDate (Recurrence)</span></span>](enddate-recurrence.md) <br/> |<span data-ttu-id="17d00-116">Stellt das Enddatum eines periodischen Vorgangs oder Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="17d00-116">Represents the end date of a recurring task or calendar item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="17d00-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="17d00-117">Parent elements</span></span>

|<span data-ttu-id="17d00-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="17d00-118">**Element**</span></span>|<span data-ttu-id="17d00-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="17d00-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="17d00-120">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="17d00-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="17d00-121">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="17d00-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="17d00-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="17d00-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="17d00-123">Enthält das Serienmuster für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="17d00-123">Contains the recurrence pattern for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="17d00-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="17d00-124">Remarks</span></span>

<span data-ttu-id="17d00-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="17d00-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="17d00-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="17d00-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="17d00-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="17d00-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="17d00-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="17d00-128">Schema name</span></span>  <br/> |<span data-ttu-id="17d00-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="17d00-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="17d00-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="17d00-130">Validation file</span></span>  <br/> |<span data-ttu-id="17d00-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="17d00-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="17d00-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="17d00-132">Can be empty</span></span>  <br/> |<span data-ttu-id="17d00-133">False</span><span class="sxs-lookup"><span data-stu-id="17d00-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="17d00-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="17d00-134">See also</span></span>



- [<span data-ttu-id="17d00-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="17d00-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

