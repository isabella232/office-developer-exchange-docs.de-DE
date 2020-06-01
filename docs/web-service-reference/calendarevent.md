---
title: CalendarEvent
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEvent
api_type:
- schema
ms.assetid: 91958c01-1fcb-4ac0-8601-5e5b434c988a
description: Das CalendarEvent-Element stellt ein eindeutiges Vorkommen eines Kalenderelements dar.
ms.openlocfilehash: 8bf37c907ed726e33dd2b1eff9add5d6235704da
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44459076"
---
# <a name="calendarevent"></a><span data-ttu-id="e2159-103">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="e2159-103">CalendarEvent</span></span>

<span data-ttu-id="e2159-104">Das **CalendarEvent** -Element stellt ein eindeutiges Vorkommen eines Kalenderelements dar.</span><span class="sxs-lookup"><span data-stu-id="e2159-104">The **CalendarEvent** element represents a unique calendar item occurrence.</span></span> 
  
[<span data-ttu-id="e2159-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e2159-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="e2159-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="e2159-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="e2159-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="e2159-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="e2159-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="e2159-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="e2159-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="e2159-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="e2159-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="e2159-110">CalendarEvent</span></span>](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 <span data-ttu-id="e2159-111">**CalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="e2159-111">**CalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="e2159-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="e2159-112">Attributes and elements</span></span>

<span data-ttu-id="e2159-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="e2159-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="e2159-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="e2159-114">Attributes</span></span>

<span data-ttu-id="e2159-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="e2159-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="e2159-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2159-116">Child elements</span></span>

|<span data-ttu-id="e2159-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2159-117">**Element**</span></span>|<span data-ttu-id="e2159-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2159-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2159-119">StartTime</span><span class="sxs-lookup"><span data-stu-id="e2159-119">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="e2159-120">Stellt den Anfang eines Kalenderereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="e2159-120">Represents the start of a calendar event.</span></span> <span data-ttu-id="e2159-121">Dies ist ein erforderliches untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="e2159-121">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="e2159-122">EndTime</span><span class="sxs-lookup"><span data-stu-id="e2159-122">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="e2159-123">Stellt das Ende eines Kalenderereignisses dar.</span><span class="sxs-lookup"><span data-stu-id="e2159-123">Represents the end of a calendar event.</span></span> <span data-ttu-id="e2159-124">Dies ist ein erforderliches untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="e2159-124">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="e2159-125">Busytype</span><span class="sxs-lookup"><span data-stu-id="e2159-125">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="e2159-126">Stellt den Frei/Gebucht-Status für ein Kalenderereignis fest.</span><span class="sxs-lookup"><span data-stu-id="e2159-126">Represents the free/busy status set for a calendar event.</span></span> <span data-ttu-id="e2159-127">Dies ist ein erforderliches untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="e2159-127">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="e2159-128">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="e2159-128">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="e2159-129">Enthält zusätzliche Informationen für ein Calendar-Ereignis.</span><span class="sxs-lookup"><span data-stu-id="e2159-129">Provides additional information for a calendar event.</span></span> <span data-ttu-id="e2159-130">Dies ist ein optionales untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="e2159-130">This is an optional child element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="e2159-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="e2159-131">Parent elements</span></span>

|<span data-ttu-id="e2159-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="e2159-132">**Element**</span></span>|<span data-ttu-id="e2159-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="e2159-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="e2159-134">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="e2159-134">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="e2159-135">Enthält eine Reihe von eindeutigen Kalenderelement vorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen.</span><span class="sxs-lookup"><span data-stu-id="e2159-135">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> <span data-ttu-id="e2159-136">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="e2159-136">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e2159-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="e2159-137">Remarks</span></span>

<span data-ttu-id="e2159-138">Die Termin-und Besprechungszeiten werden in der Zeitzone des Clients zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="e2159-138">The appointment and meeting times are returned in the time zone of the client.</span></span> <span data-ttu-id="e2159-139">Alle untergeordneten Elemente werden in der Reihenfolge aufgeführt, in der Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="e2159-139">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="e2159-140">Die von diesem Element bereitgestellte Detailebene hängt von den Berechtigungen ab, die dem Requestor erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="e2159-140">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="e2159-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="e2159-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="e2159-142">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="e2159-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e2159-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="e2159-143">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="e2159-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="e2159-144">Schema Name</span></span>  <br/> |<span data-ttu-id="e2159-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="e2159-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="e2159-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="e2159-146">Validation File</span></span>  <br/> |<span data-ttu-id="e2159-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="e2159-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="e2159-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="e2159-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="e2159-149">False</span><span class="sxs-lookup"><span data-stu-id="e2159-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e2159-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="e2159-150">See also</span></span>



[<span data-ttu-id="e2159-151">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="e2159-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="e2159-152">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="e2159-152">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="e2159-153">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="e2159-153">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

