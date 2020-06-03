---
title: ChangeHighlights
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f9bd7323-44db-4d2f-aaaa-94c2dfdeead6
description: Das ChangeHighlights-Element gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.
ms.openlocfilehash: 6c78d2c96449ee41032859f90bf51d6e0faa92ae
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44463279"
---
# <a name="changehighlights"></a><span data-ttu-id="d60d7-103">ChangeHighlights</span><span class="sxs-lookup"><span data-stu-id="d60d7-103">ChangeHighlights</span></span>

<span data-ttu-id="d60d7-104">Das **ChangeHighlights** -Element gibt an, was zwischen zwei Versionen einer Besprechungsanfrage Nachricht geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d60d7-104">The **ChangeHighlights** element specifies what has changed between two versions of a meeting request message.</span></span> 
  
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

 <span data-ttu-id="d60d7-105">**ChangeHighlightsType**</span><span class="sxs-lookup"><span data-stu-id="d60d7-105">**ChangeHighlightsType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="d60d7-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="d60d7-106">Attributes and elements</span></span>

<span data-ttu-id="d60d7-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="d60d7-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="d60d7-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="d60d7-108">Attributes</span></span>

<span data-ttu-id="d60d7-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="d60d7-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="d60d7-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d60d7-110">Child elements</span></span>

|<span data-ttu-id="d60d7-111">**Element**</span><span class="sxs-lookup"><span data-stu-id="d60d7-111">**Element**</span></span>|<span data-ttu-id="d60d7-112">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d60d7-112">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d60d7-113">HasLocationChanged</span><span class="sxs-lookup"><span data-stu-id="d60d7-113">HasLocationChanged</span></span>](haslocationchanged.md) <br/> |<span data-ttu-id="d60d7-114">Gibt an, ob die Location-Eigenschaft einer Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d60d7-114">Specifies whether the location property of a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="d60d7-115">Standort</span><span class="sxs-lookup"><span data-stu-id="d60d7-115">Location</span></span>](location.md) <br/> |<span data-ttu-id="d60d7-116">Stellt den Ort einer Besprechung oder eines Termins dar.</span><span class="sxs-lookup"><span data-stu-id="d60d7-116">Represents the location of a meeting or appointment.</span></span>  <br/> |
|[<span data-ttu-id="d60d7-117">HasStartTimeChanged</span><span class="sxs-lookup"><span data-stu-id="d60d7-117">HasStartTimeChanged</span></span>](hasstarttimechanged.md) <br/> |<span data-ttu-id="d60d7-118">Gibt an, ob die Startzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d60d7-118">Specifies whether the start time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="d60d7-119">Start</span><span class="sxs-lookup"><span data-stu-id="d60d7-119">Start</span></span>](start.md) <br/> |<span data-ttu-id="d60d7-120">Stellt den Anfang einer Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="d60d7-120">Represents the start of a duration.</span></span>  <br/> |
|[<span data-ttu-id="d60d7-121">HasEndTimeChanged</span><span class="sxs-lookup"><span data-stu-id="d60d7-121">HasEndTimeChanged</span></span>](hasendtimechanged.md) <br/> |<span data-ttu-id="d60d7-122">Gibt an, ob die Endzeit für eine Besprechung geändert wurde.</span><span class="sxs-lookup"><span data-stu-id="d60d7-122">Specifies whether the end time for a meeting has changed.</span></span>  <br/> |
|[<span data-ttu-id="d60d7-123">End</span><span class="sxs-lookup"><span data-stu-id="d60d7-123">End </span></span>](end-ex15websvcsotherref.md) <br/> |<span data-ttu-id="d60d7-124">Stellt das Ende einer Dauer dar.</span><span class="sxs-lookup"><span data-stu-id="d60d7-124">Represents the end of a duration.</span></span>  <br/> |
   
### <a name="parent-elements"></a><span data-ttu-id="d60d7-125">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="d60d7-125">Parent elements</span></span>

|<span data-ttu-id="d60d7-126">**Element**</span><span class="sxs-lookup"><span data-stu-id="d60d7-126">**Element**</span></span>|<span data-ttu-id="d60d7-127">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="d60d7-127">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="d60d7-128">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="d60d7-128">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="d60d7-129">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="d60d7-129">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="d60d7-130">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="d60d7-130">Remarks</span></span>

<span data-ttu-id="d60d7-131">Dieses Element wurde in Exchange Server 2013 eingeführt.</span><span class="sxs-lookup"><span data-stu-id="d60d7-131">This element was introduced in Exchange Server 2013.</span></span>
  
<span data-ttu-id="d60d7-132">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="d60d7-132">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="d60d7-133">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="d60d7-133">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="d60d7-134">Namespace</span><span class="sxs-lookup"><span data-stu-id="d60d7-134">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="d60d7-135">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="d60d7-135">Schema Name</span></span>  <br/> |<span data-ttu-id="d60d7-136">Typschema</span><span class="sxs-lookup"><span data-stu-id="d60d7-136">Type schema</span></span>  <br/> |
|<span data-ttu-id="d60d7-137">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="d60d7-137">Validation File</span></span>  <br/> |<span data-ttu-id="d60d7-138">Types. xsd</span><span class="sxs-lookup"><span data-stu-id="d60d7-138">types.xsd</span></span>  <br/> |
|<span data-ttu-id="d60d7-139">Kann leer sein</span><span class="sxs-lookup"><span data-stu-id="d60d7-139">Can Be Empty</span></span>  <br/> ||
   
## <a name="see-also"></a><span data-ttu-id="d60d7-140">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="d60d7-140">See also</span></span>



- [<span data-ttu-id="d60d7-141">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="d60d7-141">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

