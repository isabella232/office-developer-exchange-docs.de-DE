---
title: EndTimeInMinutes
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- EndTimeInMinutes
api_type:
- schema
ms.assetid: ef05bdda-7a66-44db-bb73-a2ce8316c257
description: Das EndTimeInMinutes-Element stellt das Ende des Arbeitstags für einen Postfachbenutzer dar.
ms.openlocfilehash: cb564f9de944848734749a30c813a94d6b5c4187
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459651"
---
# <a name="endtimeinminutes"></a><span data-ttu-id="d4eaf-103">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d4eaf-103">EndTimeInMinutes</span></span>

<span data-ttu-id="d4eaf-104">Das **EndTimeInMinutes** -Element stellt das Ende des Arbeitstags für einen Postfachbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-104">The **EndTimeInMinutes** element represents the end of the working day for a mailbox user.</span></span> 
  
[<span data-ttu-id="d4eaf-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d4eaf-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="d4eaf-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="d4eaf-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="d4eaf-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="d4eaf-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="d4eaf-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="d4eaf-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="d4eaf-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="d4eaf-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="d4eaf-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="d4eaf-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
[<span data-ttu-id="d4eaf-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="d4eaf-111">WorkingPeriod</span></span>](workingperiod.md)
  
[<span data-ttu-id="d4eaf-112">EndTimeInMinutes</span><span class="sxs-lookup"><span data-stu-id="d4eaf-112">EndTimeInMinutes</span></span>](endtimeinminutes.md)
  
```xml
<StartTimeInMinutes>...</StartTimeInMinutes>
```

 <span data-ttu-id="d4eaf-113">**int**</span><span class="sxs-lookup"><span data-stu-id="d4eaf-113">**int**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d4eaf-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d4eaf-114">Attributes and elements</span></span>

<span data-ttu-id="d4eaf-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d4eaf-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="d4eaf-116">Attributes</span></span>

<span data-ttu-id="d4eaf-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d4eaf-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4eaf-118">Child elements</span></span>

<span data-ttu-id="d4eaf-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="d4eaf-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d4eaf-120">Parent elements</span></span>

|<span data-ttu-id="d4eaf-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="d4eaf-121">**Element**</span></span>|<span data-ttu-id="d4eaf-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d4eaf-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d4eaf-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="d4eaf-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="d4eaf-124">Enthält die Arbeitswochen Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-124">Contains the work week days and hours of the mailbox user.</span></span>  <br/> <span data-ttu-id="d4eaf-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="d4eaf-125">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i]` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="d4eaf-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="d4eaf-126">Text value</span></span>

<span data-ttu-id="d4eaf-127">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-127">A text value is required.</span></span> <span data-ttu-id="d4eaf-128">Der Textwert steht für das Ende des Arbeitstags um die Anzahl der Minuten, die seit dem Tag begonnen haben.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-128">The text value represents the end of the working day by how many minutes have elapsed since the day began.</span></span> <span data-ttu-id="d4eaf-129">Beispiel: ein Endzeitpunkt von 18.00 Uhr</span><span class="sxs-lookup"><span data-stu-id="d4eaf-129">For example, an end time of 6 P.M.</span></span> <span data-ttu-id="d4eaf-130">wird durch 1080 Minuten dargestellt.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-130">is represented by 1080 minutes.</span></span>
  
<span data-ttu-id="d4eaf-131">Der Bereich der möglichen Werte für dieses Element ist 0 bis 1440.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-131">The range of possible values for this element is 0 to 1440.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="d4eaf-132">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d4eaf-132">Remarks</span></span>

<span data-ttu-id="d4eaf-133">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="d4eaf-133">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d4eaf-134">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d4eaf-134">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d4eaf-135">Namespace</span><span class="sxs-lookup"><span data-stu-id="d4eaf-135">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d4eaf-136">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d4eaf-136">Schema Name</span></span>  <br/> |<span data-ttu-id="d4eaf-137">Schematypen</span><span class="sxs-lookup"><span data-stu-id="d4eaf-137">Types schema</span></span>  <br/> |
|<span data-ttu-id="d4eaf-138">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d4eaf-138">Validation File</span></span>  <br/> |<span data-ttu-id="d4eaf-139">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="d4eaf-139">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="d4eaf-140">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="d4eaf-140">Can be Empty</span></span>  <br/> |<span data-ttu-id="d4eaf-141">False</span><span class="sxs-lookup"><span data-stu-id="d4eaf-141">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d4eaf-142">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d4eaf-142">See also</span></span>



[<span data-ttu-id="d4eaf-143">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="d4eaf-143">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="d4eaf-144">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="d4eaf-144">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="d4eaf-145">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="d4eaf-145">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

