---
title: StartTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- StartTimeInMinutes
api_type:
- schema
ms.assetid: 0fb60a78-6e79-4601-8e2f-5bd245c46d69
description: Das StartTimeInMinutes-Element stellt den Anfang des Arbeitstags für einen Postfachbenutzer dar.
ms.openlocfilehash: b33cb12299a146b577dd17939a0585a15d50fb07
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44458530"
---
# <a name="starttimeinminutes"></a><span data-ttu-id="d862d-103">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d862d-103">StartTimeInMinutes</span></span>

<span data-ttu-id="d862d-104">Das **StartTimeInMinutes** -Element stellt den Anfang des Arbeitstags für einen Postfachbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="d862d-104">The **StartTimeInMinutes** element represents the start of the working day for a mailbox user.</span></span> 
  
- [<span data-ttu-id="d862d-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d862d-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
- [<span data-ttu-id="d862d-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="d862d-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
- [<span data-ttu-id="d862d-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="d862d-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
- [<span data-ttu-id="d862d-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d862d-108">FreeBusyView</span></span>](freebusyview.md)
  
- [<span data-ttu-id="d862d-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="d862d-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
- [<span data-ttu-id="d862d-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="d862d-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
- [<span data-ttu-id="d862d-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="d862d-111">WorkingPeriod</span></span>](workingperiod.md)
  
- [<span data-ttu-id="d862d-112">StartTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d862d-112">StartTimeInMinutes</span></span>](starttimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

<span data-ttu-id="d862d-113">**int**</span><span class="sxs-lookup"><span data-stu-id="d862d-113">**int**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="d862d-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d862d-114">Attributes and elements</span></span>

<span data-ttu-id="d862d-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d862d-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d862d-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="d862d-116">Attributes</span></span>

<span data-ttu-id="d862d-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="d862d-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d862d-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d862d-118">Child elements</span></span>

<span data-ttu-id="d862d-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d862d-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d862d-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d862d-120">Parent elements</span></span>

|<span data-ttu-id="d862d-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="d862d-121">**Element**</span></span>|<span data-ttu-id="d862d-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d862d-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d862d-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="d862d-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="d862d-124">Enthält die Arbeitswochen Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="d862d-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="d862d-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d862d-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d862d-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="d862d-126">Text value</span></span>

<span data-ttu-id="d862d-127">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d862d-127">A text value is required.</span></span> <span data-ttu-id="d862d-128">Der Textwert stellt den Beginn des Arbeitstags um die Anzahl der Minuten dar, die seit dem Tag begonnen haben.</span><span class="sxs-lookup"><span data-stu-id="d862d-128">The text value represents the start of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="d862d-129">Beispielsweise eine Startzeit von 8 Uhr.</span><span class="sxs-lookup"><span data-stu-id="d862d-129">For example, a start time of 8 A.M.</span></span> <span data-ttu-id="d862d-130">wird durch 480 Minuten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d862d-130">is represented by 480 minutes.</span></span>
  
<span data-ttu-id="d862d-131">Der Bereich der möglichen Werte für dieses Element ist 0 bis 1440.</span><span class="sxs-lookup"><span data-stu-id="d862d-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d862d-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d862d-132">Remarks</span></span>

<span data-ttu-id="d862d-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d862d-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d862d-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d862d-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d862d-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d862d-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d862d-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d862d-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d862d-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d862d-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="d862d-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d862d-138">Validation File</span></span>  <br/> |<span data-ttu-id="d862d-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d862d-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d862d-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d862d-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d862d-141">False</span><span class="sxs-lookup"><span data-stu-id="d862d-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d862d-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d862d-142">See also</span></span>

- [<span data-ttu-id="d862d-143">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d862d-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
- [<span data-ttu-id="d862d-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d862d-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="d862d-145">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="d862d-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

