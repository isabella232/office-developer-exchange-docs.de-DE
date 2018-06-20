---
title: CalendarEventArray
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CalendarEventArray
api_type:
- schema
ms.assetid: a00f7f56-d7f1-429d-ae02-97043718c864
description: Das CalendarEventArray-Element enthält eine Reihe von eindeutigen Kalender Element vorkommen, die den angeforderten Benutzer Verfügbarkeit darstellen.
ms.openlocfilehash: 2e56b7b2b94e12401ba708dfca94101064d625e1
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757522"
---
# <a name="calendareventarray"></a><span data-ttu-id="fbb78-103">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="fbb78-103">CalendarEventArray</span></span>

<span data-ttu-id="fbb78-104">Das **CalendarEventArray** -Element enthält eine Reihe von eindeutigen Kalender Element vorkommen, die den angeforderten Benutzer Verfügbarkeit darstellen.</span><span class="sxs-lookup"><span data-stu-id="fbb78-104">The **CalendarEventArray** element contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span> 
  
[<span data-ttu-id="fbb78-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fbb78-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="fbb78-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="fbb78-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="fbb78-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="fbb78-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="fbb78-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="fbb78-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="fbb78-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="fbb78-109">CalendarEventArray</span></span>](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 <span data-ttu-id="fbb78-110">**ArrayOfCalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="fbb78-110">**ArrayOfCalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="fbb78-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="fbb78-111">Attributes and elements</span></span>

<span data-ttu-id="fbb78-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="fbb78-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="fbb78-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="fbb78-113">Attributes</span></span>

<span data-ttu-id="fbb78-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="fbb78-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="fbb78-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbb78-115">Child elements</span></span>

|<span data-ttu-id="fbb78-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbb78-116">**Element**</span></span>|<span data-ttu-id="fbb78-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbb78-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbb78-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="fbb78-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="fbb78-119">Stellt eine einzelne Kalender Element vorkommen.</span><span class="sxs-lookup"><span data-stu-id="fbb78-119">Represents a unique calendar item occurrence.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="fbb78-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="fbb78-120">Parent elements</span></span>

|<span data-ttu-id="fbb78-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="fbb78-121">**Element**</span></span>|<span data-ttu-id="fbb78-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="fbb78-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="fbb78-123">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="fbb78-123">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="fbb78-124">Enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="fbb78-124">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="fbb78-125">Es folgt der 2.0 XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="fbb78-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="fbb78-126">Hinweise</span><span class="sxs-lookup"><span data-stu-id="fbb78-126">Remarks</span></span>

<span data-ttu-id="fbb78-127">Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="fbb78-127">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span> <span data-ttu-id="fbb78-128">Dieses Element ist enthalten, wenn das Element [FreeBusyViewType](freebusyviewtype.md) auf **Frei/Gebucht**, **FreeBusyMerged**, **Detailed**oder **DetailedMerged**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="fbb78-128">This element is included when the [FreeBusyViewType](freebusyviewtype.md) element is set to **FreeBusy**, **FreeBusyMerged**, **Detailed**, or **DetailedMerged**.</span></span> <span data-ttu-id="fbb78-129">Dieses Element enthält keine untergeordneten Elemente keinen, wenn keine Elemente im Kalender in die angeforderte Zeitfenster vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="fbb78-129">This element does not include any child elements if no calendar items are present in the requested time window.</span></span> 
  
<span data-ttu-id="fbb78-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="fbb78-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="fbb78-131">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="fbb78-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="fbb78-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="fbb78-132">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="fbb78-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="fbb78-133">Schema Name</span></span>  <br/> |<span data-ttu-id="fbb78-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="fbb78-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="fbb78-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="fbb78-135">Validation File</span></span>  <br/> |<span data-ttu-id="fbb78-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="fbb78-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="fbb78-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="fbb78-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="fbb78-138">False</span><span class="sxs-lookup"><span data-stu-id="fbb78-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="fbb78-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="fbb78-139">See also</span></span>



[<span data-ttu-id="fbb78-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="fbb78-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="fbb78-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="fbb78-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="fbb78-142">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="fbb78-142">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

