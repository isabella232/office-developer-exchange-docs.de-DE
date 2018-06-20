---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Die ChangeHighlights-Element gibt Änderungen zwischen zwei Versionen einer Besprechung anfordern Nachricht.
ms.openlocfilehash: 5fe7aa95f60ae95f1af24e8f7a0463ad49716f65
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19757559"
---
# <a name="changehighlights"></a><span data-ttu-id="50f8f-103">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="50f8f-103">ChangeHighlights</span></span>

<span data-ttu-id="50f8f-104">Das Element **ChangeHighlights** gibt Änderungen zwischen zwei Versionen einer Besprechung Request-Nachricht.</span><span class="sxs-lookup"><span data-stu-id="50f8f-104">The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message.</span></span> 
  
```XML
<ChangeHighlights>
    <HasLocationChanged></HasLocationChanged>
    <Location></Location>
    <HasStartTimeChanged></HasStartTimeChanged>
    <Start></Start>
    <HasEndTimeChanged></HasEndTimeChanged>
    <End></End>
</ChangeHighlights>
```

 <span data-ttu-id="50f8f-105">**ChangeHighlightsType**</span><span class="sxs-lookup"><span data-stu-id="50f8f-105">**ChangeHighlightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="50f8f-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="50f8f-106">Attributes and elements</span></span>

<span data-ttu-id="50f8f-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="50f8f-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="50f8f-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="50f8f-108">Attributes</span></span>

<span data-ttu-id="50f8f-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="50f8f-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="50f8f-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50f8f-110">Child elements</span></span>

|<span data-ttu-id="50f8f-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="50f8f-111">**Element**</span></span>|<span data-ttu-id="50f8f-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50f8f-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50f8f-113">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="50f8f-113">HasLocationChanged</span></span>](haslocationchanged.md) <br/> |<span data-ttu-id="50f8f-114">Gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="50f8f-114">Specifies whether the location property of a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="50f8f-115">Ort</span><span class="sxs-lookup"><span data-stu-id="50f8f-115">Location</span></span>](location.md) <br/> |<span data-ttu-id="50f8f-116">Stellt den Speicherort einer Besprechung oder eines Termins.</span><span class="sxs-lookup"><span data-stu-id="50f8f-116">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="50f8f-117">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="50f8f-117">HasStartTimeChanged</span></span>](hasstarttimechanged.md) <br/> |<span data-ttu-id="50f8f-118">Gibt an, ob die Startzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="50f8f-118">Specifies whether the start time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="50f8f-119">Start</span><span class="sxs-lookup"><span data-stu-id="50f8f-119">Start</span></span>](start.md) <br/> |<span data-ttu-id="50f8f-120">Stellt den Anfang des eine Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="50f8f-120">Represents the start of a duration.</span></span>  <br/> |
|[<span data-ttu-id="50f8f-121">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="50f8f-121">HasEndTimeChanged</span></span>](hasendtimechanged.md) <br/> |<span data-ttu-id="50f8f-122">Gibt an, ob die Endzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="50f8f-122">Specifies whether the end time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="50f8f-123">Ende</span><span class="sxs-lookup"><span data-stu-id="50f8f-123">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="50f8f-124">Stellt das Ende einer Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="50f8f-124">Represents the end of a duration.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="50f8f-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="50f8f-125">Parent elements</span></span>

|<span data-ttu-id="50f8f-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="50f8f-126">**Element**</span></span>|<span data-ttu-id="50f8f-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="50f8f-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="50f8f-128">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="50f8f-128">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="50f8f-129">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="50f8f-129">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="50f8f-130">Hinweise</span><span class="sxs-lookup"><span data-stu-id="50f8f-130">Remarks</span></span>

<span data-ttu-id="50f8f-131">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="50f8f-131">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="50f8f-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="50f8f-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="50f8f-133">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="50f8f-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="50f8f-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="50f8f-134">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="50f8f-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="50f8f-135">Schema Name</span></span>  <br/> |<span data-ttu-id="50f8f-136">Typschema</span><span class="sxs-lookup"><span data-stu-id="50f8f-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="50f8f-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="50f8f-137">Validation File</span></span>  <br/> |<span data-ttu-id="50f8f-138">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="50f8f-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="50f8f-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="50f8f-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="50f8f-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="50f8f-140">See also</span></span>



- [<span data-ttu-id="50f8f-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="50f8f-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

