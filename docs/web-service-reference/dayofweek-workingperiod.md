---
title: DayOfWeek (WorkingPeriod)
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- DayOfWeek
api_type:
- schema
ms.assetid: 7a8a8cc1-392b-4db5-bb76-710477e31396
description: Das DayOfWeek-Element enthält die Liste der Arbeitstage, die für den Postfachbenutzer geplant sind.
ms.openlocfilehash: 06d4a7d5541b3b71fcbf9be9beb7512d06853283
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44457445"
---
# <a name="dayofweek-workingperiod"></a><span data-ttu-id="92fe9-103">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="92fe9-103">DayOfWeek (WorkingPeriod)</span></span>

<span data-ttu-id="92fe9-104">Das **DayOfWeek** -Element enthält die Liste der Arbeitstage, die für den Postfachbenutzer geplant sind.</span><span class="sxs-lookup"><span data-stu-id="92fe9-104">The **DayOfWeek** element contains the list of working days scheduled for the mailbox user.</span></span> 
  
- [<span data-ttu-id="92fe9-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="92fe9-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)  
- [<span data-ttu-id="92fe9-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="92fe9-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)  
- [<span data-ttu-id="92fe9-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="92fe9-107">FreeBusyResponse</span></span>](freebusyresponse.md)  
- [<span data-ttu-id="92fe9-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="92fe9-108">FreeBusyView</span></span>](freebusyview.md)  
- [<span data-ttu-id="92fe9-109">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="92fe9-109">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md)  
- [<span data-ttu-id="92fe9-110">WorkingPeriodArray</span><span class="sxs-lookup"><span data-stu-id="92fe9-110">WorkingPeriodArray</span></span>](workingperiodarray.md) 
- [<span data-ttu-id="92fe9-111">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="92fe9-111">WorkingPeriod</span></span>](workingperiod.md)  
- [<span data-ttu-id="92fe9-112">DayOfWeek (WorkingPeriod)</span><span class="sxs-lookup"><span data-stu-id="92fe9-112">DayOfWeek (WorkingPeriod)</span></span>](dayofweek-workingperiod.md)
  
```xml
<DayOfWeek>Sunday Monday Tuesday Wednesday Thursday Friday Saturday</DayOfWeek>
```

<span data-ttu-id="92fe9-113">**DaysOfWeek**</span><span class="sxs-lookup"><span data-stu-id="92fe9-113">**DaysOfWeek**</span></span>

## <a name="attributes-and-elements"></a><span data-ttu-id="92fe9-114">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="92fe9-114">Attributes and elements</span></span>

<span data-ttu-id="92fe9-115">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="92fe9-115">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="92fe9-116">Attribute</span><span class="sxs-lookup"><span data-stu-id="92fe9-116">Attributes</span></span>

<span data-ttu-id="92fe9-117">Keine.</span><span class="sxs-lookup"><span data-stu-id="92fe9-117">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="92fe9-118">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92fe9-118">Child elements</span></span>

<span data-ttu-id="92fe9-119">Keine.</span><span class="sxs-lookup"><span data-stu-id="92fe9-119">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="92fe9-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="92fe9-120">Parent elements</span></span>

|<span data-ttu-id="92fe9-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="92fe9-121">**Element**</span></span>|<span data-ttu-id="92fe9-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="92fe9-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="92fe9-123">WorkingPeriod</span><span class="sxs-lookup"><span data-stu-id="92fe9-123">WorkingPeriod</span></span>](workingperiod.md) <br/> |<span data-ttu-id="92fe9-124">Enthält die Arbeitswochen Tage und Stunden des Postfachbenutzers.</span><span class="sxs-lookup"><span data-stu-id="92fe9-124">Contains the work week days and hours of the mailbox user.</span></span><br/><br/><span data-ttu-id="92fe9-125">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="92fe9-125">The following is the XPath expression to this element:</span></span><br/><br/>`/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/WorkingHours/WorkingPeriodArray/WorkingPeriod[i[` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="92fe9-126">Textwert</span><span class="sxs-lookup"><span data-stu-id="92fe9-126">Text value</span></span>

<span data-ttu-id="92fe9-127">Ein Textwert wird zurückgegeben, wenn der Postfachbenutzer Tage festgelegt hat, um die Arbeitswoche darzustellen.</span><span class="sxs-lookup"><span data-stu-id="92fe9-127">A text value is returned if the mailbox user has days set to represent the work week.</span></span> <span data-ttu-id="92fe9-128">Im folgenden sind die möglichen Werte für dieses Element angegeben:</span><span class="sxs-lookup"><span data-stu-id="92fe9-128">The following are the possible values for this element:</span></span>
  
- <span data-ttu-id="92fe9-129">Sonntag</span><span class="sxs-lookup"><span data-stu-id="92fe9-129">Sunday</span></span>    
- <span data-ttu-id="92fe9-130">Montag</span><span class="sxs-lookup"><span data-stu-id="92fe9-130">Monday</span></span>    
- <span data-ttu-id="92fe9-131">Dienstag</span><span class="sxs-lookup"><span data-stu-id="92fe9-131">Tuesday</span></span>    
- <span data-ttu-id="92fe9-132">Mittwoch</span><span class="sxs-lookup"><span data-stu-id="92fe9-132">Wednesday</span></span>    
- <span data-ttu-id="92fe9-133">Donnerstag</span><span class="sxs-lookup"><span data-stu-id="92fe9-133">Thursday</span></span>    
- <span data-ttu-id="92fe9-134">Freitag</span><span class="sxs-lookup"><span data-stu-id="92fe9-134">Friday</span></span>    
- <span data-ttu-id="92fe9-135">Samstag</span><span class="sxs-lookup"><span data-stu-id="92fe9-135">Saturday</span></span> 
    
<span data-ttu-id="92fe9-136">Die Text Werte werden in dieser Reihenfolge zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="92fe9-136">The text values will be returned in that order.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="92fe9-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="92fe9-137">Remarks</span></span>

<span data-ttu-id="92fe9-138">Beachten Sie, dass der Unterschied zwischen diesem Element und dem Element der Verfügbarkeit [DayOfWeek (TimeZone)](dayofweek-timezone.md) der Typ ist.</span><span class="sxs-lookup"><span data-stu-id="92fe9-138">It is important to note that the difference between this element and the Availability [DayOfWeek (TimeZone)](dayofweek-timezone.md) element is the type.</span></span> 
  
<span data-ttu-id="92fe9-139">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="92fe9-139">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="92fe9-140">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="92fe9-140">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="92fe9-141">Namespace</span><span class="sxs-lookup"><span data-stu-id="92fe9-141">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="92fe9-142">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="92fe9-142">Schema Name</span></span>  <br/> |<span data-ttu-id="92fe9-143">Schematypen</span><span class="sxs-lookup"><span data-stu-id="92fe9-143">Types schema</span></span>  <br/> |
|<span data-ttu-id="92fe9-144">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="92fe9-144">Validation File</span></span>  <br/> |<span data-ttu-id="92fe9-145">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="92fe9-145">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="92fe9-146">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="92fe9-146">Can be Empty</span></span>  <br/> |<span data-ttu-id="92fe9-147">False</span><span class="sxs-lookup"><span data-stu-id="92fe9-147">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="92fe9-148">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="92fe9-148">See also</span></span>

- [<span data-ttu-id="92fe9-149">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="92fe9-149">GetUserAvailability operation</span></span>](getuseravailability-operation.md)  
- [<span data-ttu-id="92fe9-150">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="92fe9-150">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
- [<span data-ttu-id="92fe9-151">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="92fe9-151">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

