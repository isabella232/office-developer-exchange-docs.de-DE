---
title: WorkingPeriodArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- WorkingPeriodArray
api_type:
- schema
ms.assetid: 3a3f6393-eacc-4734-b6c9-b67023fe2830
description: Das WorkingPeriodArray-Element enthält Informationen zum Arbeitszeitraum für den Postfachbenutzer.
ms.openlocfilehash: a9ca55866a574c5208d8561fca6daf417867fef6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44465198"
---
# <a name="workingperiodarray"></a><span data-ttu-id="31ee8-103">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="31ee8-103">WorkingPeriodArray</span></span>

<span data-ttu-id="31ee8-104">Das **WorkingPeriodArray** -Element enthält Informationen zum Arbeitszeitraum für den Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="31ee8-104">The **WorkingPeriodArray** element contains working period information for the mailbox user.</span></span> 
  
[<span data-ttu-id="31ee8-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="31ee8-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="31ee8-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="31ee8-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="31ee8-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="31ee8-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="31ee8-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="31ee8-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="31ee8-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="31ee8-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)
  
[<span data-ttu-id="31ee8-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="31ee8-110">WorkingPeriodArray</span></span>](workingperiodarray.md)
  
```xml
<WorkingPeriodArray>
   <WorkingPeriod>...</WorkingPeriod>
</WorkingPeriodArray>
```

 <span data-ttu-id="31ee8-111">**ArrayOfWorkingPeriod**</span><span class="sxs-lookup"><span data-stu-id="31ee8-111">**ArrayOfWorkingPeriod**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="31ee8-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="31ee8-112">Attributes and elements</span></span>

<span data-ttu-id="31ee8-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="31ee8-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="31ee8-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="31ee8-114">Attributes</span></span>

<span data-ttu-id="31ee8-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="31ee8-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="31ee8-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31ee8-116">Child elements</span></span>

|<span data-ttu-id="31ee8-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="31ee8-117">**Element**</span></span>|<span data-ttu-id="31ee8-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31ee8-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31ee8-119">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="31ee8-119">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="31ee8-120">Enthält die Arbeitswochen Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="31ee8-120">Contains the work week days and hours of the mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="31ee8-121">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="31ee8-121">Parent elements</span></span>

|<span data-ttu-id="31ee8-122">**Element**</span><span class="sxs-lookup"><span data-stu-id="31ee8-122">**Element**</span></span>|<span data-ttu-id="31ee8-123">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="31ee8-123">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="31ee8-124">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="31ee8-124">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="31ee8-125">Stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="31ee8-125">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> <span data-ttu-id="31ee8-126">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="31ee8-126">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="31ee8-127">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="31ee8-127">Remarks</span></span>

<span data-ttu-id="31ee8-128">Dieses Element ist erforderlich, wenn das [WorkingHours](workinghours-ex15websvcsotherref.md) -Element verwendet wird.</span><span class="sxs-lookup"><span data-stu-id="31ee8-128">This element is required if the [WorkingHours](workinghours-ex15websvcsotherref.md) element is used.</span></span> <span data-ttu-id="31ee8-129">Alle untergeordneten Elemente werden in der Reihenfolge aufgeführt, in der Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="31ee8-129">All the child elements are listed in the sequence in which they occur.</span></span> 
  
<span data-ttu-id="31ee8-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="31ee8-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="31ee8-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="31ee8-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="31ee8-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="31ee8-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="31ee8-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="31ee8-133">Schema Name</span></span>  <br/> |<span data-ttu-id="31ee8-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="31ee8-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="31ee8-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="31ee8-135">Validation File</span></span>  <br/> |<span data-ttu-id="31ee8-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="31ee8-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="31ee8-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="31ee8-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="31ee8-138">False</span><span class="sxs-lookup"><span data-stu-id="31ee8-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="31ee8-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="31ee8-139">See also</span></span>



[<span data-ttu-id="31ee8-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="31ee8-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="31ee8-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="31ee8-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="31ee8-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="31ee8-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

