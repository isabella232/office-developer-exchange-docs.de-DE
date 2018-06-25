---
title: MergedFreeBusy
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MergedFreeBusy
api_type:
- schema
ms.assetid: ea45590d-476e-4b68-9fe8-ae392feadfea
description: Das MergedFreeBusy-Element enthält den zusammengeführten Frei/Gebucht-Datenstrom.
ms.openlocfilehash: 542b9fae0c36b0236bd806e8a9117753968e812c
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/25/2018
ms.locfileid: "19830449"
---
# <a name="mergedfreebusy"></a><span data-ttu-id="5794a-103">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="5794a-103">MergedFreeBusy</span></span>

<span data-ttu-id="5794a-104">Das **MergedFreeBusy** -Element enthält den zusammengeführten Frei/Gebucht-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="5794a-104">The **MergedFreeBusy** element contains the merged free/busy stream of data.</span></span> 
  
[<span data-ttu-id="5794a-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5794a-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="5794a-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="5794a-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="5794a-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="5794a-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="5794a-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="5794a-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="5794a-109">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="5794a-109">MergedFreeBusy</span></span>](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 <span data-ttu-id="5794a-110">**string**</span><span class="sxs-lookup"><span data-stu-id="5794a-110">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5794a-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5794a-111">Attributes and elements</span></span>

<span data-ttu-id="5794a-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5794a-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5794a-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="5794a-113">Attributes</span></span>

<span data-ttu-id="5794a-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="5794a-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5794a-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5794a-115">Child elements</span></span>

<span data-ttu-id="5794a-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="5794a-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5794a-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5794a-117">Parent elements</span></span>

|<span data-ttu-id="5794a-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="5794a-118">**Element**</span></span>|<span data-ttu-id="5794a-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5794a-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5794a-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="5794a-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="5794a-121">Enthält Informationen zur Verfügbarkeit für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="5794a-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="5794a-122">Es folgt der XPath-Ausdruck, der dieses Element:</span><span class="sxs-lookup"><span data-stu-id="5794a-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5794a-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="5794a-123">Text value</span></span>

<span data-ttu-id="5794a-124">Ein Textwert wird vom Server bereitgestellt werden, wenn der Wert für das [FreeBusyViewType](freebusyviewtype.md) -Element eine der folgenden ist:</span><span class="sxs-lookup"><span data-stu-id="5794a-124">A text value is provided by the server if the value for the [FreeBusyViewType](freebusyviewtype.md) element is one of the following:</span></span> 
  
- <span data-ttu-id="5794a-125">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="5794a-125">DetailedMerged</span></span>
    
- <span data-ttu-id="5794a-126">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="5794a-126">FreeBusyMerged</span></span>
    
- <span data-ttu-id="5794a-127">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="5794a-127">MergedOnly</span></span>
    
<span data-ttu-id="5794a-128">Der Textwert ist ein Stream von Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="5794a-128">The text value is a stream of free/busy information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="5794a-129">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5794a-129">Remarks</span></span>

<span data-ttu-id="5794a-130">Der Datenstrom bereitgestellt durch dieses Element wird durch die [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) und [Zeitfenster](timewindow.md) Elemente definiert.</span><span class="sxs-lookup"><span data-stu-id="5794a-130">The stream of data provided by this element is defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) and [TimeWindow](timewindow.md) elements.</span></span> <span data-ttu-id="5794a-131">Das [Zeitfenster](timewindow.md) -Element definiert die Zeitspanne für Verfügbarkeit abgefragt.</span><span class="sxs-lookup"><span data-stu-id="5794a-131">The [TimeWindow](timewindow.md) element defines the time span queried for availability.</span></span> <span data-ttu-id="5794a-132">Das [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert, wie die Zeit aus dem Element [Zeitfenster](timewindow.md) in Intervallen im **MergedFreeBusy** Element zurückgegeben aufgeteilt wird.</span><span class="sxs-lookup"><span data-stu-id="5794a-132">The [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element defines how the time from the [TimeWindow](timewindow.md) element is broken into intervals returned in the **MergedFreeBusy** element.</span></span> <span data-ttu-id="5794a-133">Jede Nummer im **MergedFreeBusy** Stream-Objekt stellt ein einzelnes Intervall vom [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert.</span><span class="sxs-lookup"><span data-stu-id="5794a-133">Each number in the **MergedFreeBusy** stream represents a single interval defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element.</span></span> <span data-ttu-id="5794a-134">Die folgende Tabelle enthält die möglichen Werte für ein einzelnes Intervall.</span><span class="sxs-lookup"><span data-stu-id="5794a-134">The following table lists the possible values for an individual interval.</span></span> 
  
|<span data-ttu-id="5794a-135">**Ziffer**</span><span class="sxs-lookup"><span data-stu-id="5794a-135">**Digit**</span></span>|<span data-ttu-id="5794a-136">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="5794a-136">**Availability**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5794a-137">0</span><span class="sxs-lookup"><span data-stu-id="5794a-137">0</span></span>  <br/> |<span data-ttu-id="5794a-138">Kostenlos</span><span class="sxs-lookup"><span data-stu-id="5794a-138">Free</span></span>  <br/> |
|<span data-ttu-id="5794a-139">1</span><span class="sxs-lookup"><span data-stu-id="5794a-139">1</span></span>  <br/> |<span data-ttu-id="5794a-140">Mit Vorbehalt</span><span class="sxs-lookup"><span data-stu-id="5794a-140">Tentative</span></span>  <br/> |
|<span data-ttu-id="5794a-141">2</span><span class="sxs-lookup"><span data-stu-id="5794a-141">2</span></span>  <br/> |<span data-ttu-id="5794a-142">Gebucht</span><span class="sxs-lookup"><span data-stu-id="5794a-142">Busy</span></span>  <br/> |
|<span data-ttu-id="5794a-143">3</span><span class="sxs-lookup"><span data-stu-id="5794a-143">3</span></span>  <br/> |<span data-ttu-id="5794a-144">Abwesenheit (Out of Office, OOF)</span><span class="sxs-lookup"><span data-stu-id="5794a-144">Out of Office (OOF)</span></span>  <br/> |
|<span data-ttu-id="5794a-145">4</span><span class="sxs-lookup"><span data-stu-id="5794a-145">4</span></span>  <br/> |<span data-ttu-id="5794a-146">Keine Daten</span><span class="sxs-lookup"><span data-stu-id="5794a-146">No data</span></span>  <br/> |
   
<span data-ttu-id="5794a-147">Beispielsweise enthält eine Anforderung für Frei/Gebucht-Daten ein, die vier Stunden darstellt [Zeitfenster](timewindow.md) -Element als auch ein [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element, 60 Minuten darstellt.</span><span class="sxs-lookup"><span data-stu-id="5794a-147">For example, a request for free/busy data includes a [TimeWindow](timewindow.md) element that represents four hours and a [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element that represents 60 minutes.</span></span> <span data-ttu-id="5794a-148">Wenn den angeforderten Benutzer Kalender OOF für den ersten 60 Minuten ist, für die folgenden 90 Minuten beschäftigt und ungeplante für die letzten 90 Minuten in das Zeitfenster, **MergedFreeBusy** Stream 3220 werden.</span><span class="sxs-lookup"><span data-stu-id="5794a-148">If the requested user's calendar is OOF for the first 60 minutes, busy for the following 90 minutes, and unscheduled for the final 90 minutes in the time window, the **MergedFreeBusy** stream will be 3220.</span></span> <span data-ttu-id="5794a-149">Wenn ein Intervall für mehrere Verfügbarkeit Klassifizierung enthält, wird die größte Zahl dieses Intervall klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="5794a-149">If an interval contains more than one availability classification, the highest number is used to classify that interval.</span></span> 
  
<span data-ttu-id="5794a-150">Die von diesem Element bereitgestellte Detailebene, hängt von der Requestor gewährten Berechtigungen.</span><span class="sxs-lookup"><span data-stu-id="5794a-150">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="5794a-151">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="5794a-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5794a-152">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5794a-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5794a-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="5794a-153">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5794a-154">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5794a-154">Schema Name</span></span>  <br/> |<span data-ttu-id="5794a-155">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5794a-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="5794a-156">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5794a-156">Validation File</span></span>  <br/> |<span data-ttu-id="5794a-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5794a-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5794a-158">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5794a-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="5794a-159">False</span><span class="sxs-lookup"><span data-stu-id="5794a-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5794a-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5794a-160">See also</span></span>



[<span data-ttu-id="5794a-161">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="5794a-161">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="5794a-162">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="5794a-162">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="5794a-163">Erste Benutzer Verfügbarkeit</span><span class="sxs-lookup"><span data-stu-id="5794a-163">Getting User Availability</span></span>](http://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

