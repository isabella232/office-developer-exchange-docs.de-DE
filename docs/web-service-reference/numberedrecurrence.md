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
description: Das NumberedRecurrence-Element beschreibt das Startdatum und die Anzahl der Vorkommen eines wiederkehrenden Elements.
ms.openlocfilehash: 000674e5b0bad9deea5aa4ac78d41135a922c755
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465940"
---
# <a name="numberedrecurrence"></a><span data-ttu-id="f2f3d-103">NumberedRecurrence</span><span class="sxs-lookup"><span data-stu-id="f2f3d-103">NumberedRecurrence</span></span>

<span data-ttu-id="f2f3d-104">Das **NumberedRecurrence** -Element beschreibt das Startdatum und die Anzahl der Vorkommen eines wiederkehrenden Elements.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-104">The **NumberedRecurrence** element describes the start date and the number of occurrences of a recurring item.</span></span> 
  
```xml
<NumberedRecurrence>
   <StartDate/>
   <NumberOfOccurrences/>
</NumberedRecurrence>
```

 <span data-ttu-id="f2f3d-105">**NumberedRecurrenceRangeType**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-105">**NumberedRecurrenceRangeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="f2f3d-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="f2f3d-106">Attributes and elements</span></span>

<span data-ttu-id="f2f3d-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="f2f3d-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="f2f3d-108">Attributes</span></span>

<span data-ttu-id="f2f3d-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="f2f3d-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2f3d-110">Child elements</span></span>

|<span data-ttu-id="f2f3d-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-111">**Element**</span></span>|<span data-ttu-id="f2f3d-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2f3d-113">StartDate (Serie)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-113">StartDate (Recurrence)</span></span>](startdate-recurrence.md) <br/> |<span data-ttu-id="f2f3d-114">Stellt das Startdatum eines periodischen Vorgangs oder Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-114">Represents the start date of a recurring task or calendar item.</span></span>  <br/> |
|[<span data-ttu-id="f2f3d-115">NumberOfOccurrences</span><span class="sxs-lookup"><span data-stu-id="f2f3d-115">NumberOfOccurrences</span></span>](numberofoccurrences.md) <br/> |<span data-ttu-id="f2f3d-116">Enthält die Anzahl der Vorkommen eines wiederkehrenden Elements.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-116">Contains the number of occurrences of a recurring item.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="f2f3d-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="f2f3d-117">Parent elements</span></span>

|<span data-ttu-id="f2f3d-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-118">**Element**</span></span>|<span data-ttu-id="f2f3d-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="f2f3d-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="f2f3d-120">Serie (serietype)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-120">Recurrence (RecurrenceType)</span></span>](recurrence-recurrencetype.md) <br/> |<span data-ttu-id="f2f3d-121">Enthält das Serienmuster für Kalenderelemente und Besprechungsanfragen.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-121">Contains the recurrence pattern for calendar items and meeting requests.</span></span>  <br/> |
|[<span data-ttu-id="f2f3d-122">Serie (TaskRecurrenceType)</span><span class="sxs-lookup"><span data-stu-id="f2f3d-122">Recurrence (TaskRecurrenceType)</span></span>](recurrence-taskrecurrencetype.md) <br/> |<span data-ttu-id="f2f3d-123">Enthält Serieninformationen für wiederkehrende Vorgänge.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-123">Contains recurrence information for recurring tasks.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="f2f3d-124">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="f2f3d-124">Remarks</span></span>

<span data-ttu-id="f2f3d-125">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="f2f3d-125">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="f2f3d-126">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="f2f3d-126">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="f2f3d-127">Namespace</span><span class="sxs-lookup"><span data-stu-id="f2f3d-127">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="f2f3d-128">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="f2f3d-128">Schema name</span></span>  <br/> |<span data-ttu-id="f2f3d-129">Schematypen</span><span class="sxs-lookup"><span data-stu-id="f2f3d-129">Types schema</span></span>  <br/> |
|<span data-ttu-id="f2f3d-130">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="f2f3d-130">Validation file</span></span>  <br/> |<span data-ttu-id="f2f3d-131">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="f2f3d-131">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="f2f3d-132">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="f2f3d-132">Can be empty</span></span>  <br/> |<span data-ttu-id="f2f3d-133">False</span><span class="sxs-lookup"><span data-stu-id="f2f3d-133">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f2f3d-134">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="f2f3d-134">See also</span></span>



- [<span data-ttu-id="f2f3d-135">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="f2f3d-135">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

