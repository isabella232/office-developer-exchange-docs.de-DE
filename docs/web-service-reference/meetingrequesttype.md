---
title: MeetingRequestType
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MeetingRequestType
api_type:
- schema
ms.assetid: bcd5c97c-19aa-4b1d-a8e8-e8c4bd473dd9
description: Das MeetingRequestType-Element beschreibt den Typ der Besprechungsanfrage.
ms.openlocfilehash: e90c44dd4124d698ca5ef7655f6429a7167673e6
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/03/2020
ms.locfileid: "44465786"
---
# <a name="meetingrequesttype"></a><span data-ttu-id="350b0-103">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="350b0-103">MeetingRequestType</span></span>

<span data-ttu-id="350b0-104">Das **MeetingRequestType** -Element beschreibt den Typ der Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="350b0-104">The **MeetingRequestType** element describes the type of the meeting request.</span></span> 
  
```xml
<MeetingRequestType/>
```

 <span data-ttu-id="350b0-105">**MeetingRequestTypeType**</span><span class="sxs-lookup"><span data-stu-id="350b0-105">**MeetingRequestTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="350b0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="350b0-106">Attributes and elements</span></span>

<span data-ttu-id="350b0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="350b0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="350b0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="350b0-108">Attributes</span></span>

<span data-ttu-id="350b0-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="350b0-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="350b0-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="350b0-110">Child elements</span></span>

<span data-ttu-id="350b0-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="350b0-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="350b0-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="350b0-112">Parent elements</span></span>

|<span data-ttu-id="350b0-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="350b0-113">**Element**</span></span>|<span data-ttu-id="350b0-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="350b0-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="350b0-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="350b0-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="350b0-116">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="350b0-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="350b0-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="350b0-117">Text value</span></span>

<span data-ttu-id="350b0-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="350b0-118">A text value is required.</span></span> <span data-ttu-id="350b0-119">In der folgenden Tabelle sind die möglichen Text Werte für dieses Element aufgeführt.</span><span class="sxs-lookup"><span data-stu-id="350b0-119">The following table lists the possible text values for this element.</span></span>
  
|<span data-ttu-id="350b0-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="350b0-120">**Value**</span></span>|<span data-ttu-id="350b0-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="350b0-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="350b0-122">FullUpdate</span><span class="sxs-lookup"><span data-stu-id="350b0-122">FullUpdate</span></span>  <br/> |<span data-ttu-id="350b0-123">Identifiziert die Besprechungsanfrage als vollständige Aktualisierung einer vorhandenen Anforderung.</span><span class="sxs-lookup"><span data-stu-id="350b0-123">Identifies the meeting request as a full update to an existing request.</span></span> <span data-ttu-id="350b0-124">Eine vollständige Aktualisierung enthält aktualisierte Zeit-und Informationsinhalte.</span><span class="sxs-lookup"><span data-stu-id="350b0-124">A full update has updated time and informational content.</span></span>  <br/> |
|<span data-ttu-id="350b0-125">InformationalUpdate</span><span class="sxs-lookup"><span data-stu-id="350b0-125">InformationalUpdate</span></span>  <br/> |<span data-ttu-id="350b0-126">Identifiziert die Besprechungsanfrage als nur mit aktualisierten Informationsinhalten.</span><span class="sxs-lookup"><span data-stu-id="350b0-126">Identifies the meeting request as only containing updated informational content.</span></span>  <br/> |
|<span data-ttu-id="350b0-127">NewMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="350b0-127">NewMeetingRequest</span></span>  <br/> |<span data-ttu-id="350b0-128">Identifiziert die Besprechungsanfrage als neue Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="350b0-128">Identifies the meeting request as a new meeting request.</span></span>  <br/> |
|<span data-ttu-id="350b0-129">Keine</span><span class="sxs-lookup"><span data-stu-id="350b0-129">None</span></span>  <br/> |<span data-ttu-id="350b0-130">Gibt an, dass der Typ der Besprechungsanfrage nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="350b0-130">Indicates that the meeting request type is not defined.</span></span>  <br/> |
|<span data-ttu-id="350b0-131">Veraltete</span><span class="sxs-lookup"><span data-stu-id="350b0-131">Outdated</span></span>  <br/> |<span data-ttu-id="350b0-132">Identifiziert die Besprechungsanfrage als veraltet.</span><span class="sxs-lookup"><span data-stu-id="350b0-132">Identifies the meeting request as outdated.</span></span>  <br/> |
|<span data-ttu-id="350b0-133">PrincipalWantsCopy</span><span class="sxs-lookup"><span data-stu-id="350b0-133">PrincipalWantsCopy</span></span>  <br/> |<span data-ttu-id="350b0-134">Gibt an, dass die Besprechungsanfrage einem Prinzipal gehört, der Besprechungsnachrichten an eine Stellvertretung weitergeleitet hat und seine Kopien als Information markiert hat.</span><span class="sxs-lookup"><span data-stu-id="350b0-134">Indicates that the meeting request belongs to a principal who has forwarded meeting messages to a delegate and has his copies marked as informational.</span></span>  <br/> |
|<span data-ttu-id="350b0-135">SilentUpdate</span><span class="sxs-lookup"><span data-stu-id="350b0-135">SilentUpdate</span></span>  <br/> |<span data-ttu-id="350b0-136">Identifiziert die Besprechungsanfrage als eine unbeaufsichtigte Aktualisierung für eine vorhandene Besprechung.</span><span class="sxs-lookup"><span data-stu-id="350b0-136">Identifies the meeting request as a silent update to an existing meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="350b0-137">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="350b0-137">Remarks</span></span>

<span data-ttu-id="350b0-138">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen EWS-Verzeichnis des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, auf dem die Client Zugriffs-Server Rolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="350b0-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="350b0-139">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="350b0-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="350b0-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="350b0-140">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="350b0-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="350b0-141">Schema Name</span></span>  <br/> |<span data-ttu-id="350b0-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="350b0-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="350b0-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="350b0-143">Validation File</span></span>  <br/> |<span data-ttu-id="350b0-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="350b0-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="350b0-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="350b0-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="350b0-146">False</span><span class="sxs-lookup"><span data-stu-id="350b0-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="350b0-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="350b0-147">See also</span></span>



- [<span data-ttu-id="350b0-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="350b0-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

