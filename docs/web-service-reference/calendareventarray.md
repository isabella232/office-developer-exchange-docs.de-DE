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
description: Das CalendarEventArray-Element enthält eine Reihe von eindeutigen Kalenderelement vorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen.
ms.openlocfilehash: 6badba2477a9d48c6d109740de454e2815d3c211
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44463370"
---
# <a name="calendareventarray"></a><span data-ttu-id="cd9d4-103">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="cd9d4-103">CalendarEventArray</span></span>

<span data-ttu-id="cd9d4-104">Das **CalendarEventArray** -Element enthält eine Reihe von eindeutigen Kalenderelement vorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-104">The **CalendarEventArray** element contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span> 
  
[<span data-ttu-id="cd9d4-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="cd9d4-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="cd9d4-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="cd9d4-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="cd9d4-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="cd9d4-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="cd9d4-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="cd9d4-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="cd9d4-109">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="cd9d4-109">CalendarEventArray</span></span>](calendareventarray.md)
  
```xml
<CalendarEventArray>
   <CalendarEvent>...</CalendarEvent>
</CalendarEventArray>
```

 <span data-ttu-id="cd9d4-110">**ArrayOfCalendarEvent**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-110">**ArrayOfCalendarEvent**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="cd9d4-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="cd9d4-111">Attributes and elements</span></span>

<span data-ttu-id="cd9d4-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="cd9d4-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="cd9d4-113">Attributes</span></span>

<span data-ttu-id="cd9d4-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="cd9d4-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd9d4-115">Child elements</span></span>

|<span data-ttu-id="cd9d4-116">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-116">**Element**</span></span>|<span data-ttu-id="cd9d4-117">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-117">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd9d4-118">CalendarEvent</span><span class="sxs-lookup"><span data-stu-id="cd9d4-118">CalendarEvent</span></span>](calendarevent.md) <br/> |<span data-ttu-id="cd9d4-119">Stellt ein eindeutiges Kalenderelement vorkommen dar.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-119">Represents a unique calendar item occurrence.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="cd9d4-120">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="cd9d4-120">Parent elements</span></span>

|<span data-ttu-id="cd9d4-121">**Element**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-121">**Element**</span></span>|<span data-ttu-id="cd9d4-122">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="cd9d4-122">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="cd9d4-123">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="cd9d4-123">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="cd9d4-124">Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-124">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="cd9d4-125">Im folgenden finden Sie den XPath 2,0-Ausdruck für dieses Element:</span><span class="sxs-lookup"><span data-stu-id="cd9d4-125">The following is the XPath 2.0 expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="cd9d4-126">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="cd9d4-126">Remarks</span></span>

<span data-ttu-id="cd9d4-127">Die von diesem Element bereitgestellte Detailebene hängt von den Berechtigungen ab, die dem Requestor erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-127">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span> <span data-ttu-id="cd9d4-128">Dieses Element ist enthalten, wenn das [FreeBusyViewType](freebusyviewtype.md) -Element auf **freebusy**, **FreeBusyMerged**, **detailed**oder **DetailedMerged**festgelegt ist.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-128">This element is included when the [FreeBusyViewType](freebusyviewtype.md) element is set to **FreeBusy**, **FreeBusyMerged**, **Detailed**, or **DetailedMerged**.</span></span> <span data-ttu-id="cd9d4-129">Dieses Element enthält keine untergeordneten Elemente, wenn im angeforderten Zeitfenster keine Kalenderelemente vorhanden sind.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-129">This element does not include any child elements if no calendar items are present in the requested time window.</span></span> 
  
<span data-ttu-id="cd9d4-130">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="cd9d4-130">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="cd9d4-131">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="cd9d4-131">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="cd9d4-132">Namespace</span><span class="sxs-lookup"><span data-stu-id="cd9d4-132">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="cd9d4-133">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="cd9d4-133">Schema Name</span></span>  <br/> |<span data-ttu-id="cd9d4-134">Schematypen</span><span class="sxs-lookup"><span data-stu-id="cd9d4-134">Types schema</span></span>  <br/> |
|<span data-ttu-id="cd9d4-135">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="cd9d4-135">Validation File</span></span>  <br/> |<span data-ttu-id="cd9d4-136">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="cd9d4-136">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="cd9d4-137">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="cd9d4-137">Can be Empty</span></span>  <br/> |<span data-ttu-id="cd9d4-138">False</span><span class="sxs-lookup"><span data-stu-id="cd9d4-138">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="cd9d4-139">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="cd9d4-139">See also</span></span>



[<span data-ttu-id="cd9d4-140">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="cd9d4-140">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="cd9d4-141">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="cd9d4-141">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="cd9d4-142">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="cd9d4-142">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

