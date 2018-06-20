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
description: Das MeetingRequestType-Element beschreibt die Art der Besprechungsanfrage.
ms.openlocfilehash: 7269587e2fa72aeb9070a7b53ee9215829729329
ms.sourcegitcommit: 34041125dc8c5f993b21cebfc4f8b72f0fd2cb6f
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 06/11/2018
ms.locfileid: "19830432"
---
# <a name="meetingrequesttype"></a><span data-ttu-id="5cd87-103">MeetingRequestType</span><span class="sxs-lookup"><span data-stu-id="5cd87-103">MeetingRequestType</span></span>

<span data-ttu-id="5cd87-104">Das **MeetingRequestType** -Element beschreibt die Art der Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="5cd87-104">The **MeetingRequestType** element describes the type of the meeting request.</span></span> 
  
```xml
<MeetingRequestType/>
```

 <span data-ttu-id="5cd87-105">**MeetingRequestTypeType**</span><span class="sxs-lookup"><span data-stu-id="5cd87-105">**MeetingRequestTypeType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="5cd87-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="5cd87-106">Attributes and elements</span></span>

<span data-ttu-id="5cd87-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="5cd87-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="5cd87-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="5cd87-108">Attributes</span></span>

<span data-ttu-id="5cd87-109">Keine.</span><span class="sxs-lookup"><span data-stu-id="5cd87-109">None.</span></span>
  
### <a name="child-elements"></a><span data-ttu-id="5cd87-110">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cd87-110">Child elements</span></span>

<span data-ttu-id="5cd87-111">Keine.</span><span class="sxs-lookup"><span data-stu-id="5cd87-111">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="5cd87-112">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="5cd87-112">Parent elements</span></span>

|<span data-ttu-id="5cd87-113">**Element**</span><span class="sxs-lookup"><span data-stu-id="5cd87-113">**Element**</span></span>|<span data-ttu-id="5cd87-114">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5cd87-114">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="5cd87-115">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5cd87-115">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="5cd87-116">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="5cd87-116">Represents a meeting request in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="5cd87-117">Textwert</span><span class="sxs-lookup"><span data-stu-id="5cd87-117">Text value</span></span>

<span data-ttu-id="5cd87-118">Ein Textwert ist erforderlich.</span><span class="sxs-lookup"><span data-stu-id="5cd87-118">A text value is required.</span></span> <span data-ttu-id="5cd87-119">Die folgende Tabelle enthält die möglichen Textwerte für dieses Element.</span><span class="sxs-lookup"><span data-stu-id="5cd87-119">The following table lists the possible text values for this element.</span></span>
  
|<span data-ttu-id="5cd87-120">**Wert**</span><span class="sxs-lookup"><span data-stu-id="5cd87-120">**Value**</span></span>|<span data-ttu-id="5cd87-121">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="5cd87-121">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="5cd87-122">FullUpdate</span><span class="sxs-lookup"><span data-stu-id="5cd87-122">FullUpdate</span></span>  <br/> |<span data-ttu-id="5cd87-123">Die Besprechungsanfrage identifiziert als eine vollständige Aktualisierung auf eine vorhandene Anforderung.</span><span class="sxs-lookup"><span data-stu-id="5cd87-123">Identifies the meeting request as a full update to an existing request.</span></span> <span data-ttu-id="5cd87-124">Eine vollständige Aktualisierung wurde aktualisiert, Zeit und informative Inhalte aufweisen.</span><span class="sxs-lookup"><span data-stu-id="5cd87-124">A full update has updated time and informational content.</span></span>  <br/> |
|<span data-ttu-id="5cd87-125">InformationalUpdate</span><span class="sxs-lookup"><span data-stu-id="5cd87-125">InformationalUpdate</span></span>  <br/> |<span data-ttu-id="5cd87-126">Identifiziert die Besprechungsanfrage als informative Inhalte aufweisen, enthält, die aktualisiert werden.</span><span class="sxs-lookup"><span data-stu-id="5cd87-126">Identifies the meeting request as only containing updated informational content.</span></span>  <br/> |
|<span data-ttu-id="5cd87-127">NewMeetingRequest</span><span class="sxs-lookup"><span data-stu-id="5cd87-127">NewMeetingRequest</span></span>  <br/> |<span data-ttu-id="5cd87-128">Identifiziert die Besprechungsanfrage als eine neue Besprechungsanfrage.</span><span class="sxs-lookup"><span data-stu-id="5cd87-128">Identifies the meeting request as a new meeting request.</span></span>  <br/> |
|<span data-ttu-id="5cd87-129">Keine</span><span class="sxs-lookup"><span data-stu-id="5cd87-129">None</span></span>  <br/> |<span data-ttu-id="5cd87-130">Gibt an, dass die Besprechungsanfrage Typ nicht definiert ist.</span><span class="sxs-lookup"><span data-stu-id="5cd87-130">Indicates that the meeting request type is not defined.</span></span>  <br/> |
|<span data-ttu-id="5cd87-131">Veraltet</span><span class="sxs-lookup"><span data-stu-id="5cd87-131">Outdated</span></span>  <br/> |<span data-ttu-id="5cd87-132">Die Besprechungsanfrage als veraltet identifiziert.</span><span class="sxs-lookup"><span data-stu-id="5cd87-132">Identifies the meeting request as outdated.</span></span>  <br/> |
|<span data-ttu-id="5cd87-133">PrincipalWantsCopy</span><span class="sxs-lookup"><span data-stu-id="5cd87-133">PrincipalWantsCopy</span></span>  <br/> |<span data-ttu-id="5cd87-134">Gibt an, dass die Besprechungsanfrage zu einem Prinzipal gehört, die Besprechungsnachrichten an die Stellvertretung weitergeleitet und seinen Kopien wie Informationszwecken gekennzeichnet hat.</span><span class="sxs-lookup"><span data-stu-id="5cd87-134">Indicates that the meeting request belongs to a principal who has forwarded meeting messages to a delegate and has his copies marked as informational.</span></span>  <br/> |
|<span data-ttu-id="5cd87-135">SilentUpdate</span><span class="sxs-lookup"><span data-stu-id="5cd87-135">SilentUpdate</span></span>  <br/> |<span data-ttu-id="5cd87-136">Die Besprechungsanfrage identifiziert als eine automatische Aktualisierung einer vorhandenen Besprechung.</span><span class="sxs-lookup"><span data-stu-id="5cd87-136">Identifies the meeting request as a silent update to an existing meeting.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="5cd87-137">Hinweise</span><span class="sxs-lookup"><span data-stu-id="5cd87-137">Remarks</span></span>

<span data-ttu-id="5cd87-138">Das Schema, das dieses Element beschreibt befindet sich das virtuelle Verzeichnis EWS des Computers, auf dem Microsoft Exchange Server 2010 ausgeführt wird, die die Clientzugriffs-Serverrolle installiert ist.</span><span class="sxs-lookup"><span data-stu-id="5cd87-138">The schema that describes this element is located in the EWS virtual directory of the computer that is running Microsoft Exchange Server 2010 that has the Client Access server role installed.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="5cd87-139">Informationen zum Element</span><span class="sxs-lookup"><span data-stu-id="5cd87-139">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5cd87-140">Namespace</span><span class="sxs-lookup"><span data-stu-id="5cd87-140">Namespace</span></span>  <br/> |http://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="5cd87-141">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="5cd87-141">Schema Name</span></span>  <br/> |<span data-ttu-id="5cd87-142">Schematypen</span><span class="sxs-lookup"><span data-stu-id="5cd87-142">Types schema</span></span>  <br/> |
|<span data-ttu-id="5cd87-143">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="5cd87-143">Validation File</span></span>  <br/> |<span data-ttu-id="5cd87-144">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="5cd87-144">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="5cd87-145">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="5cd87-145">Can be Empty</span></span>  <br/> |<span data-ttu-id="5cd87-146">False</span><span class="sxs-lookup"><span data-stu-id="5cd87-146">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5cd87-147">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="5cd87-147">See also</span></span>



- [<span data-ttu-id="5cd87-148">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="5cd87-148">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

