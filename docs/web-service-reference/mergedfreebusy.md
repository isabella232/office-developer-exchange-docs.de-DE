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
description: Das MergedFreeBusy-Element enthält den zusammengeführten frei/gebucht-Datenstrom.
ms.openlocfilehash: a1483449534f0d886e3c97a23d28c5d78f865042
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/01/2020
ms.locfileid: "44468726"
---
# <a name="mergedfreebusy"></a><span data-ttu-id="aec4c-103">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="aec4c-103">MergedFreeBusy</span></span>

<span data-ttu-id="aec4c-104">Das **MergedFreeBusy** -Element enthält den zusammengeführten frei/gebucht-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="aec4c-104">The **MergedFreeBusy** element contains the merged free/busy stream of data.</span></span> 
  
[<span data-ttu-id="aec4c-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="aec4c-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="aec4c-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="aec4c-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="aec4c-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="aec4c-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="aec4c-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="aec4c-108">FreeBusyView</span></span>](freebusyview.md)
  
[<span data-ttu-id="aec4c-109">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="aec4c-109">MergedFreeBusy</span></span>](mergedfreebusy.md)
  
```xml
<MergedFreeBusy>...</MergedFreeBusy>
```

 <span data-ttu-id="aec4c-110">**Zeichenfolge**</span><span class="sxs-lookup"><span data-stu-id="aec4c-110">**string**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="aec4c-111">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="aec4c-111">Attributes and elements</span></span>

<span data-ttu-id="aec4c-112">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="aec4c-112">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="aec4c-113">Attribute</span><span class="sxs-lookup"><span data-stu-id="aec4c-113">Attributes</span></span>

<span data-ttu-id="aec4c-114">Keine.</span><span class="sxs-lookup"><span data-stu-id="aec4c-114">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="aec4c-115">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aec4c-115">Child elements</span></span>

<span data-ttu-id="aec4c-116">Keine.</span><span class="sxs-lookup"><span data-stu-id="aec4c-116">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="aec4c-117">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="aec4c-117">Parent elements</span></span>

|<span data-ttu-id="aec4c-118">**Element**</span><span class="sxs-lookup"><span data-stu-id="aec4c-118">**Element**</span></span>|<span data-ttu-id="aec4c-119">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="aec4c-119">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="aec4c-120">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="aec4c-120">FreeBusyView</span></span>](freebusyview.md) <br/> |<span data-ttu-id="aec4c-121">Enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="aec4c-121">Contains availability information for a specific user.</span></span>  <br/> <span data-ttu-id="aec4c-122">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="aec4c-122">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse/FreeBusyView` <br/> |
   
## <a name="text-value"></a><span data-ttu-id="aec4c-123">Textwert</span><span class="sxs-lookup"><span data-stu-id="aec4c-123">Text value</span></span>

<span data-ttu-id="aec4c-124">Ein Textwert wird vom Server bereitgestellt, wenn der Wert für das [FreeBusyViewType](freebusyviewtype.md) -Element einer der folgenden Werte ist:</span><span class="sxs-lookup"><span data-stu-id="aec4c-124">A text value is provided by the server if the value for the [FreeBusyViewType](freebusyviewtype.md) element is one of the following:</span></span> 
  
- <span data-ttu-id="aec4c-125">DetailedMerged</span><span class="sxs-lookup"><span data-stu-id="aec4c-125">DetailedMerged</span></span>
    
- <span data-ttu-id="aec4c-126">FreeBusyMerged</span><span class="sxs-lookup"><span data-stu-id="aec4c-126">FreeBusyMerged</span></span>
    
- <span data-ttu-id="aec4c-127">MergedOnly</span><span class="sxs-lookup"><span data-stu-id="aec4c-127">MergedOnly</span></span>
    
<span data-ttu-id="aec4c-128">Der Textwert ist ein Stream von Frei/Gebucht-Informationen.</span><span class="sxs-lookup"><span data-stu-id="aec4c-128">The text value is a stream of free/busy information.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="aec4c-129">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="aec4c-129">Remarks</span></span>

<span data-ttu-id="aec4c-130">Der Datenstrom, der von diesem Element bereitgestellt wird, wird durch die Elemente [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) und [Window](timewindow.md) definiert.</span><span class="sxs-lookup"><span data-stu-id="aec4c-130">The stream of data provided by this element is defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) and [TimeWindow](timewindow.md) elements.</span></span> <span data-ttu-id="aec4c-131">Das Time [Window](timewindow.md) -Element definiert die Zeitspanne, die für die Verfügbarkeit abgefragt wird.</span><span class="sxs-lookup"><span data-stu-id="aec4c-131">The [TimeWindow](timewindow.md) element defines the time span queried for availability.</span></span> <span data-ttu-id="aec4c-132">Das [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert, wie die Zeit aus dem Time [Window](timewindow.md) -Element in Intervalle unterteilt wird, die im **MergedFreeBusy** -Element zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="aec4c-132">The [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element defines how the time from the [TimeWindow](timewindow.md) element is broken into intervals returned in the **MergedFreeBusy** element.</span></span> <span data-ttu-id="aec4c-133">Jede Zahl im **MergedFreeBusy** -Datenstrom stellt ein einzelnes Intervall dar, das durch das [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element definiert wird.</span><span class="sxs-lookup"><span data-stu-id="aec4c-133">Each number in the **MergedFreeBusy** stream represents a single interval defined by the [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element.</span></span> <span data-ttu-id="aec4c-134">In der folgenden Tabelle sind die möglichen Werte für ein individuelles Intervall aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="aec4c-134">The following table lists the possible values for an individual interval.</span></span> 
  
|<span data-ttu-id="aec4c-135">**Ziffer**</span><span class="sxs-lookup"><span data-stu-id="aec4c-135">**Digit**</span></span>|<span data-ttu-id="aec4c-136">**Verfügbarkeit**</span><span class="sxs-lookup"><span data-stu-id="aec4c-136">**Availability**</span></span>|
|:-----|:-----|
|<span data-ttu-id="aec4c-137">0</span><span class="sxs-lookup"><span data-stu-id="aec4c-137">0</span></span>  <br/> |<span data-ttu-id="aec4c-138">Frei</span><span class="sxs-lookup"><span data-stu-id="aec4c-138">Free</span></span>  <br/> |
|<span data-ttu-id="aec4c-139">1 </span><span class="sxs-lookup"><span data-stu-id="aec4c-139">1</span></span>  <br/> |<span data-ttu-id="aec4c-140">Vorläufige</span><span class="sxs-lookup"><span data-stu-id="aec4c-140">Tentative</span></span>  <br/> |
|<span data-ttu-id="aec4c-141">2</span><span class="sxs-lookup"><span data-stu-id="aec4c-141">2</span></span>  <br/> |<span data-ttu-id="aec4c-142">Gebucht</span><span class="sxs-lookup"><span data-stu-id="aec4c-142">Busy</span></span>  <br/> |
|<span data-ttu-id="aec4c-143">3</span><span class="sxs-lookup"><span data-stu-id="aec4c-143">3</span></span>  <br/> |<span data-ttu-id="aec4c-144">Abwesend</span><span class="sxs-lookup"><span data-stu-id="aec4c-144">Out of Office (OOF)</span></span>  <br/> |
|<span data-ttu-id="aec4c-145">4 </span><span class="sxs-lookup"><span data-stu-id="aec4c-145">4</span></span>  <br/> |<span data-ttu-id="aec4c-146">Keine Daten</span><span class="sxs-lookup"><span data-stu-id="aec4c-146">No data</span></span>  <br/> |
   
<span data-ttu-id="aec4c-147">Beispielsweise enthält eine Anforderung für Frei/Gebucht-Daten ein Zeit [Fenster](timewindow.md) Element, das vier Stunden darstellt, und ein [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) -Element, das 60 Minuten darstellt.</span><span class="sxs-lookup"><span data-stu-id="aec4c-147">For example, a request for free/busy data includes a [TimeWindow](timewindow.md) element that represents four hours and a [MergedFreeBusyIntervalInMinutes](mergedfreebusyintervalinminutes.md) element that represents 60 minutes.</span></span> <span data-ttu-id="aec4c-148">Wenn der Kalender des angeforderten Benutzers OOF für die ersten 60 Minuten ist, beschäftigt für die folgenden 90 Minuten und für die letzten 90 Minuten im Zeitfenster ungeplant ist, wird der **MergedFreeBusy** -Datenstrom 3220.</span><span class="sxs-lookup"><span data-stu-id="aec4c-148">If the requested user's calendar is OOF for the first 60 minutes, busy for the following 90 minutes, and unscheduled for the final 90 minutes in the time window, the **MergedFreeBusy** stream will be 3220.</span></span> <span data-ttu-id="aec4c-149">Wenn ein Intervall mehr als eine Verfügbarkeits Klassifizierung enthält, wird die höchste Zahl verwendet, um das Intervall zu klassifizieren.</span><span class="sxs-lookup"><span data-stu-id="aec4c-149">If an interval contains more than one availability classification, the highest number is used to classify that interval.</span></span> 
  
<span data-ttu-id="aec4c-150">Die von diesem Element bereitgestellte Detailebene hängt von den Berechtigungen ab, die dem Requestor erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="aec4c-150">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="aec4c-151">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="aec4c-151">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="aec4c-152">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="aec4c-152">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="aec4c-153">Namespace</span><span class="sxs-lookup"><span data-stu-id="aec4c-153">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="aec4c-154">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="aec4c-154">Schema Name</span></span>  <br/> |<span data-ttu-id="aec4c-155">Schematypen</span><span class="sxs-lookup"><span data-stu-id="aec4c-155">Types schema</span></span>  <br/> |
|<span data-ttu-id="aec4c-156">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="aec4c-156">Validation File</span></span>  <br/> |<span data-ttu-id="aec4c-157">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="aec4c-157">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="aec4c-158">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="aec4c-158">Can be Empty</span></span>  <br/> |<span data-ttu-id="aec4c-159">False</span><span class="sxs-lookup"><span data-stu-id="aec4c-159">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="aec4c-160">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="aec4c-160">See also</span></span>



[<span data-ttu-id="aec4c-161">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="aec4c-161">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="aec4c-162">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="aec4c-162">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="aec4c-163">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="aec4c-163">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

