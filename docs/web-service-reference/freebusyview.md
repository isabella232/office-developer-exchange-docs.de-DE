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
description: Das FreeBusyView-Element enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.
ms.openlocfilehash: e5cc3bea6b57d5c400dd9be44bf9f9aaf9e43eb9
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44456101"
---
# <a name="freebusyview"></a><span data-ttu-id="de549-103">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="de549-103">FreeBusyView</span></span>

<span data-ttu-id="de549-104">Das **FreeBusyView** -Element enthält Verfügbarkeitsinformationen für einen bestimmten Benutzer.</span><span class="sxs-lookup"><span data-stu-id="de549-104">The **FreeBusyView** element contains availability information for a specific user.</span></span> 
  
[<span data-ttu-id="de549-105">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="de549-105">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)
  
[<span data-ttu-id="de549-106">FreeBusyResponseArray</span><span class="sxs-lookup"><span data-stu-id="de549-106">FreeBusyResponseArray</span></span>](freebusyresponsearray.md)
  
[<span data-ttu-id="de549-107">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="de549-107">FreeBusyResponse</span></span>](freebusyresponse.md)
  
[<span data-ttu-id="de549-108">FreeBusyView</span><span class="sxs-lookup"><span data-stu-id="de549-108">FreeBusyView</span></span>](freebusyview.md)
  
```xml
<FreeBusyView>
   <FreeBusyViewType>...</FreeBusyViewType>
   <MergedFreeBusy>...</MergedFreeBusy>
   <CalendarEventArray>...</CalendarEventArray>
   <WorkingHours>...</WorkingHours>
</FreeBusyView>
```

 <span data-ttu-id="de549-109">**FreeBusyView**</span><span class="sxs-lookup"><span data-stu-id="de549-109">**FreeBusyView**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="de549-110">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="de549-110">Attributes and elements</span></span>

<span data-ttu-id="de549-111">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="de549-111">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="de549-112">Attribute</span><span class="sxs-lookup"><span data-stu-id="de549-112">Attributes</span></span>

<span data-ttu-id="de549-113">Keine.</span><span class="sxs-lookup"><span data-stu-id="de549-113">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="de549-114">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de549-114">Child elements</span></span>

|<span data-ttu-id="de549-115">**Element**</span><span class="sxs-lookup"><span data-stu-id="de549-115">**Element**</span></span>|<span data-ttu-id="de549-116">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de549-116">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de549-117">FreeBusyViewType</span><span class="sxs-lookup"><span data-stu-id="de549-117">FreeBusyViewType</span></span>](freebusyviewtype.md) <br/> |<span data-ttu-id="de549-118">Stellt den Typ der angeforderten Frei/Gebucht-Informationen dar, die in der Antwort zurückgegeben werden.</span><span class="sxs-lookup"><span data-stu-id="de549-118">Represents the type of requested free/busy information returned in the response.</span></span>  <br/> |
|[<span data-ttu-id="de549-119">MergedFreeBusy</span><span class="sxs-lookup"><span data-stu-id="de549-119">MergedFreeBusy</span></span>](mergedfreebusy.md) <br/> |<span data-ttu-id="de549-120">Enthält den zusammengeführten frei/gebucht-Datenstrom.</span><span class="sxs-lookup"><span data-stu-id="de549-120">Contains the merged free/busy stream of data.</span></span>  <br/> |
|[<span data-ttu-id="de549-121">CalendarEventArray</span><span class="sxs-lookup"><span data-stu-id="de549-121">CalendarEventArray</span></span>](calendareventarray.md) <br/> |<span data-ttu-id="de549-122">Enthält eine Reihe von eindeutigen Kalenderelement vorkommen, die die Verfügbarkeit des angeforderten Benutzers darstellen.</span><span class="sxs-lookup"><span data-stu-id="de549-122">Contains a set of unique calendar item occurrences that represent the requested user's availability.</span></span>  <br/> |
|[<span data-ttu-id="de549-123">WorkingHours</span><span class="sxs-lookup"><span data-stu-id="de549-123">WorkingHours</span></span>](workinghours-ex15websvcsotherref.md) <br/> |<span data-ttu-id="de549-124">Stellt die Zeitzoneneinstellungen und Arbeitszeiten für den angeforderten Postfachbenutzer dar.</span><span class="sxs-lookup"><span data-stu-id="de549-124">Represents the time zone settings and working hours for the requested mailbox user.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="de549-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="de549-125">Parent elements</span></span>

|<span data-ttu-id="de549-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="de549-126">**Element**</span></span>|<span data-ttu-id="de549-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="de549-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="de549-128">FreeBusyResponse</span><span class="sxs-lookup"><span data-stu-id="de549-128">FreeBusyResponse</span></span>](freebusyresponse.md) <br/> |<span data-ttu-id="de549-129">Enthält die Frei/Gebucht-Informationen für einen einzelnen Postfachbenutzer.</span><span class="sxs-lookup"><span data-stu-id="de549-129">Contains the free/busy information for a single mailbox user.</span></span>  <br/> <span data-ttu-id="de549-130">Für dieses Element wird folgender XPath-Ausdruck verwendet: </span><span class="sxs-lookup"><span data-stu-id="de549-130">The following is the XPath expression to this element:</span></span>  <br/>  `/GetUserAvailabilityResponse/FreeBusyResponseArray/FreeBusyResponse` <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de549-131">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="de549-131">Remarks</span></span>

<span data-ttu-id="de549-132">Alle untergeordneten Elemente werden in der Reihenfolge aufgeführt, in der Sie auftreten.</span><span class="sxs-lookup"><span data-stu-id="de549-132">All the child elements are listed in the sequence in which they occur.</span></span> <span data-ttu-id="de549-133">Die von diesem Element bereitgestellte Detailebene hängt von den Berechtigungen ab, die dem Requestor erteilt werden.</span><span class="sxs-lookup"><span data-stu-id="de549-133">The level of detail provided by this element depends on the permissions granted to the requestor.</span></span>
  
<span data-ttu-id="de549-134">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, der MicrosoftExchange Server 2007 mit installierter Clientzugriff-Serverrolle ausführt.</span><span class="sxs-lookup"><span data-stu-id="de549-134">The schema that describes this element is located in the EWS virtual directory of the computer that is running MicrosoftExchange Server 2007 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="de549-135">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="de549-135">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="de549-136">Namespace</span><span class="sxs-lookup"><span data-stu-id="de549-136">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="de549-137">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="de549-137">Schema Name</span></span>  <br/> |<span data-ttu-id="de549-138">Schematypen</span><span class="sxs-lookup"><span data-stu-id="de549-138">Types schema</span></span>  <br/> |
|<span data-ttu-id="de549-139">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="de549-139">Validation File</span></span>  <br/> |<span data-ttu-id="de549-140">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="de549-140">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="de549-141">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="de549-141">Can be Empty</span></span>  <br/> |<span data-ttu-id="de549-142">False</span><span class="sxs-lookup"><span data-stu-id="de549-142">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="de549-143">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="de549-143">See also</span></span>



[<span data-ttu-id="de549-144">GetUserAvailability-Vorgang</span><span class="sxs-lookup"><span data-stu-id="de549-144">GetUserAvailability operation</span></span>](getuseravailability-operation.md)
  
[<span data-ttu-id="de549-145">GetUserAvailabilityResponse</span><span class="sxs-lookup"><span data-stu-id="de549-145">GetUserAvailabilityResponse</span></span>](getuseravailabilityresponse.md)


[<span data-ttu-id="de549-146">Verfügbarkeit von Benutzern wird abgerufen</span><span class="sxs-lookup"><span data-stu-id="de549-146">Getting User Availability</span></span>](https://msdn.microsoft.com/library/d4133fcb-9b0f-4e6b-aadf-a389da83516a%28Office.15%29.aspx)

