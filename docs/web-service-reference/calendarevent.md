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
description: Das CalendarEvent-Element stellt einen eindeutigen Kalender Element vorkommen.
ms.openlocfilehash: f7fff7ba511ca12813dd4c2d694e89c97589ba31
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19757521"
---
# <a name="calendarevent"></a><span data-ttu-id="b45cd-103">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="b45cd-103">CalendarEvent</span></span>

<span data-ttu-id="b45cd-104">Das **CalendarEvent** -Element stellt einen eindeutigen Kalender Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="b45cd-104">The **CalendarEvent** element represents a unique calendar item occurrence.</span></span> 
  
[<span data-ttu-id="b45cd-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b45cd-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="b45cd-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="b45cd-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="b45cd-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="b45cd-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="b45cd-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="b45cd-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="b45cd-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="b45cd-109">CalendarEventArray</span></span>](calendareventarray.md)
  
[<span data-ttu-id="b45cd-110">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="b45cd-110">CalendarEvent</span></span>](calendarevent.md)
  
```xml
<CalendarEvent>
   <StartTime>...</StartTime>
   <EndTime>...</EndTime>
   <BusyType>...</BusyType>
   <CalendarEventDetails>...</CalendarEventDetails>
</CalendarEvent>
```

 <span data-ttu-id="b45cd-111">**CalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="b45cd-111">**CalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="b45cd-112">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="b45cd-112">Attributes and elements</span></span>

<span data-ttu-id="b45cd-113">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="b45cd-113">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="b45cd-114">Attribute</span><span class="sxs-lookup"><span data-stu-id="b45cd-114">Attributes</span></span>

<span data-ttu-id="b45cd-115">Keine.</span><span class="sxs-lookup"><span data-stu-id="b45cd-115">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="b45cd-116">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b45cd-116">Child elements</span></span>

|<span data-ttu-id="b45cd-117">**Element**</span><span class="sxs-lookup"><span data-stu-id="b45cd-117">**Element**</span></span>|<span data-ttu-id="b45cd-118">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b45cd-118">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b45cd-119">StartTime</span><span class="sxs-lookup"><span data-stu-id="b45cd-119">StartTime</span></span>](starttime.md) <br/> |<span data-ttu-id="b45cd-120">Stellt den Anfang des ein Kalenderereignis.</span><span class="sxs-lookup"><span data-stu-id="b45cd-120">Represents the start of a calendar event.</span></span> <span data-ttu-id="b45cd-121">Dies ist ein erforderliches untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="b45cd-121">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="b45cd-122">EndTime</span><span class="sxs-lookup"><span data-stu-id="b45cd-122">EndTime</span></span>](endtime.md) <br/> |<span data-ttu-id="b45cd-123">Stellt das Ende einer Kalenderereignis dar.</span><span class="sxs-lookup"><span data-stu-id="b45cd-123">Represents the end of a calendar event.</span></span> <span data-ttu-id="b45cd-124">Dies ist ein erforderliches untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="b45cd-124">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="b45cd-125">BusyType</span><span class="sxs-lookup"><span data-stu-id="b45cd-125">BusyType</span></span>](busytype.md) <br/> |<span data-ttu-id="b45cd-126">Stellt den Frei/Gebucht-Status für ein Ereignis im Kalender festgelegt.</span><span class="sxs-lookup"><span data-stu-id="b45cd-126">Represents the free/busy status set for a calendar event.</span></span> <span data-ttu-id="b45cd-127">Dies ist ein erforderliches untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="b45cd-127">This is a required child element.</span></span>  <br/> |
|[<span data-ttu-id="b45cd-128">CalendarEventDetails</span><span class="sxs-lookup"><span data-stu-id="b45cd-128">CalendarEventDetails</span></span>](calendareventdetails.md) <br/> |<span data-ttu-id="b45cd-129">Enthält zusätzliche Informationen für ein Ereignis im Kalender.</span><span class="sxs-lookup"><span data-stu-id="b45cd-129">Provides additional information for a calendar event.</span></span> <span data-ttu-id="b45cd-130">Dies ist ein optionales untergeordnetes Element.</span><span class="sxs-lookup"><span data-stu-id="b45cd-130">This is an optional child element.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="b45cd-131">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="b45cd-131">Parent elements</span></span>

|<span data-ttu-id="b45cd-132">**Element**</span><span class="sxs-lookup"><span data-stu-id="b45cd-132">**Element**</span></span>|<span data-ttu-id="b45cd-133">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="b45cd-133">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="b45cd-134">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="b45cd-134">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="b45cd-135">Enthält einen Satz von eindeutigen Kalender Element vorkommen, die den angeforderten Benutzer Verfügbarkeit darstellen.</span><span class="sxs-lookup"><span data-stu-id="b45cd-135">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> <span data-ttu-id="b45cd-136">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="b45cd-136">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView/CalendarEventArray` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="b45cd-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="b45cd-137">Remarks</span></span>

<span data-ttu-id="b45cd-138">Die Zeiten Termin und Besprechung werden in der Zeitzone des Clients zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="b45cd-138">The appointment and meeting times are returned in the time zone of the client.</span></span> <span data-ttu-id="b45cd-139">All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen.</span><span class="sxs-lookup"><span data-stu-id="b45cd-139">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="b45cd-140">Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="b45cd-140">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="b45cd-141">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="b45cd-141">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="b45cd-142">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="b45cd-142">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="b45cd-143">Namespace</span><span class="sxs-lookup"><span data-stu-id="b45cd-143">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="b45cd-144">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="b45cd-144">Schema Name</span></span>  <br/> |<span data-ttu-id="b45cd-145">Schematypen</span><span class="sxs-lookup"><span data-stu-id="b45cd-145">Types schema</span></span>  <br/> |
|<span data-ttu-id="b45cd-146">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="b45cd-146">Validation File</span></span>  <br/> |<span data-ttu-id="b45cd-147">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="b45cd-147">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="b45cd-148">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="b45cd-148">Can be Empty</span></span>  <br/> |<span data-ttu-id="b45cd-149">False</span><span class="sxs-lookup"><span data-stu-id="b45cd-149">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b45cd-150">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="b45cd-150">See also</span></span>



[<span data-ttu-id="b45cd-151">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="b45cd-151">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="b45cd-152">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="b45cd-152">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="b45cd-153">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="b45cd-153">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

