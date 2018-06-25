---
title: FreeBusyView
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- FreeBusyView
api_type:
- schema
ms.assetid: cb18434f-5f41-4e05-a5ce-d921b2721a8c
description: Das FreeBusyView-Element enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.
ms.openlocfilehash: d0d603f18642a94e841a1a6bb8e8849aa6b5b273
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19758544"
---
# <a name="freebusyview"></a><span data-ttu-id="edd9b-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="edd9b-103">FreeBusyView</span></span>

<span data-ttu-id="edd9b-104">Das **FreeBusyView** -Element enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="edd9b-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="edd9b-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="edd9b-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="edd9b-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="edd9b-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="edd9b-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="edd9b-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="edd9b-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="edd9b-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="edd9b-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="edd9b-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="edd9b-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="edd9b-110">Attributes and elements</span></span>

<span data-ttu-id="edd9b-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="edd9b-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="edd9b-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="edd9b-112">Attributes</span></span>

<span data-ttu-id="edd9b-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="edd9b-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="edd9b-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="edd9b-114">Child elements</span></span>

|<span data-ttu-id="edd9b-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="edd9b-115">**Element**</span></span>|<span data-ttu-id="edd9b-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="edd9b-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="edd9b-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="edd9b-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="edd9b-118">Stellt den Typ des angeforderten Frei/Gebucht-Informationen in der Antwort zurückgegeben.</span><span class="sxs-lookup"><span data-stu-id="edd9b-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="edd9b-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="edd9b-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="edd9b-120">Enthält den zusammengeführten Frei/Gebucht-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="edd9b-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="edd9b-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="edd9b-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="edd9b-122">Enthält einen Satz von eindeutigen Kalender Element vorkommen, die den angeforderten Benutzer Verfügbarkeit darstellen.</span><span class="sxs-lookup"><span data-stu-id="edd9b-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="edd9b-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="edd9b-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="edd9b-124">Stellt die Zeitzone Einstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="edd9b-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="edd9b-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="edd9b-125">Parent elements</span></span>

|<span data-ttu-id="edd9b-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="edd9b-126">**Element**</span></span>|<span data-ttu-id="edd9b-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="edd9b-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="edd9b-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="edd9b-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="edd9b-129">Die Frei/Gebucht-Informationen für ein einzelnes Postfachbenutzer enthält.</span><span class="sxs-lookup"><span data-stu-id="edd9b-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="edd9b-130">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="edd9b-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="edd9b-131">Hinweise</span><span class="sxs-lookup"><span data-stu-id="edd9b-131">Remarks</span></span>

<span data-ttu-id="edd9b-132">All die untergeordneten Elemente sind in der Reihenfolge aufgeführt, in denen sie anfallen.</span><span class="sxs-lookup"><span data-stu-id="edd9b-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="edd9b-133">Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="edd9b-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="edd9b-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="edd9b-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="edd9b-135">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="edd9b-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="edd9b-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="edd9b-136">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="edd9b-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="edd9b-137">Schema Name</span></span>  <br/> |<span data-ttu-id="edd9b-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="edd9b-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="edd9b-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="edd9b-139">Validation File</span></span>  <br/> |<span data-ttu-id="edd9b-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="edd9b-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="edd9b-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="edd9b-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="edd9b-142">False</span><span class="sxs-lookup"><span data-stu-id="edd9b-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="edd9b-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="edd9b-143">See also</span></span>



[<span data-ttu-id="edd9b-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="edd9b-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="edd9b-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="edd9b-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="edd9b-146">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="edd9b-146">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

