---
title: UniqueBody
manager: sethgros
ms.date: 09/17/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- UniqueBody
api_type:
- schema
ms.assetid: 06bc95d7-121c-433b-bd27-c2b0eb8c011f
description: Das UniqueBody-Element stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.
ms.openlocfilehash: 0a8d52c7d4eb8bda9fd41c4c25e448523185df93
ms.sourcegitcommit: 88ec988f2bb67c1866d06b361615f3674a24e795
ms.translationtype: MT
ms.contentlocale: de-DE
ms.lasthandoff: 05/31/2020
ms.locfileid: "44461919"
---
# <a name="uniquebody"></a><span data-ttu-id="546a0-103">UniqueBody</span><span class="sxs-lookup"><span data-stu-id="546a0-103">UniqueBody</span></span>

<span data-ttu-id="546a0-104">Das **UniqueBody** -Element stellt ein HTML-Fragment oder nur-Text dar, der den eindeutigen Textkörper dieser Unterhaltung darstellt.</span><span class="sxs-lookup"><span data-stu-id="546a0-104">The **UniqueBody** element represents an HTML fragment or plain text which represents the unique body of this conversation.</span></span> 
  
```XML
<UniqueBody BodyType=""/>
```

 <span data-ttu-id="546a0-105">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="546a0-105">**BodyType**</span></span>
## <a name="attributes-and-elements"></a><span data-ttu-id="546a0-106">Attribute und Elemente</span><span class="sxs-lookup"><span data-stu-id="546a0-106">Attributes and elements</span></span>

<span data-ttu-id="546a0-107">In den folgenden Abschnitten werden Attribute, untergeordnete und übergeordnete Elemente erläutert.</span><span class="sxs-lookup"><span data-stu-id="546a0-107">The following sections describe attributes, child elements, and parent elements.</span></span>
  
### <a name="attributes"></a><span data-ttu-id="546a0-108">Attribute</span><span class="sxs-lookup"><span data-stu-id="546a0-108">Attributes</span></span>

|<span data-ttu-id="546a0-109">**Attribut**</span><span class="sxs-lookup"><span data-stu-id="546a0-109">**Attribute**</span></span>|<span data-ttu-id="546a0-110">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="546a0-110">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="546a0-111">**BodyType**</span><span class="sxs-lookup"><span data-stu-id="546a0-111">**BodyType**</span></span> <br/> |<span data-ttu-id="546a0-112">Beschreibt, wie der Element Text im Element gespeichert wird.</span><span class="sxs-lookup"><span data-stu-id="546a0-112">Describes how the item body is stored in the item.</span></span>  <br/> |
   
#### <a name="bodytype-attribute"></a><span data-ttu-id="546a0-113">BodyType-Attribut</span><span class="sxs-lookup"><span data-stu-id="546a0-113">BodyType Attribute</span></span>

|<span data-ttu-id="546a0-114">**Wert**</span><span class="sxs-lookup"><span data-stu-id="546a0-114">**Value**</span></span>|<span data-ttu-id="546a0-115">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="546a0-115">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="546a0-116">**HTML**</span><span class="sxs-lookup"><span data-stu-id="546a0-116">**HTML**</span></span> <br/> |<span data-ttu-id="546a0-117">Wandelt alle Textkörper in HTML um.</span><span class="sxs-lookup"><span data-stu-id="546a0-117">Converts all bodies to HTML.</span></span>  <br/> |
|<span data-ttu-id="546a0-118">**Text**</span><span class="sxs-lookup"><span data-stu-id="546a0-118">**Text**</span></span> <br/> |<span data-ttu-id="546a0-119">Wandelt alle Textkörper in nur-Text um.</span><span class="sxs-lookup"><span data-stu-id="546a0-119">Converts all bodies to plain text.</span></span>  <br/> |
   
### <a name="child-elements"></a><span data-ttu-id="546a0-120">Untergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="546a0-120">Child elements</span></span>

<span data-ttu-id="546a0-121">Keine.</span><span class="sxs-lookup"><span data-stu-id="546a0-121">None.</span></span>
  
### <a name="parent-elements"></a><span data-ttu-id="546a0-122">Übergeordnete Elemente</span><span class="sxs-lookup"><span data-stu-id="546a0-122">Parent elements</span></span>

|<span data-ttu-id="546a0-123">**Element**</span><span class="sxs-lookup"><span data-stu-id="546a0-123">**Element**</span></span>|<span data-ttu-id="546a0-124">**Beschreibung**</span><span class="sxs-lookup"><span data-stu-id="546a0-124">**Description**</span></span>|
|:-----|:-----|
|[<span data-ttu-id="546a0-125">CalendarItem</span><span class="sxs-lookup"><span data-stu-id="546a0-125">CalendarItem</span></span>](calendaritem.md) <br/> |<span data-ttu-id="546a0-126">Stellt ein Element im Exchange-Kalender dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-126">Represents an Exchange calendar item.</span></span>  <br/> |
|[<span data-ttu-id="546a0-127">Kontaktperson</span><span class="sxs-lookup"><span data-stu-id="546a0-127">Contact</span></span>](contact.md) <br/> |<span data-ttu-id="546a0-128">Stellt ein Exchange-Kontaktelement dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-128">Represents an Exchange contact item.</span></span>  <br/> |
|[<span data-ttu-id="546a0-129">DistributionList</span><span class="sxs-lookup"><span data-stu-id="546a0-129">DistributionList</span></span>](distributionlist.md) <br/> |<span data-ttu-id="546a0-130">Stellt eine Verteilerliste dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-130">Represents a distribution list.</span></span>  <br/> |
|[<span data-ttu-id="546a0-131">Element</span><span class="sxs-lookup"><span data-stu-id="546a0-131">Item</span></span>](item.md) <br/> |<span data-ttu-id="546a0-132">Stellt ein Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-132">Represents an item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-133">MeetingCancellation</span><span class="sxs-lookup"><span data-stu-id="546a0-133">MeetingCancellation</span></span>](meetingcancellation.md) <br/> |<span data-ttu-id="546a0-134">Stellt eine Besprechungsabsage im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-134">Represents a meeting cancellation in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-135">MeetingMessage</span><span class="sxs-lookup"><span data-stu-id="546a0-135">MeetingMessage</span></span>](meetingmessage.md) <br/> |<span data-ttu-id="546a0-136">Stellt eine Besprechung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-136">Represents a meeting in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-137">MeetingRequest</span><span class="sxs-lookup"><span data-stu-id="546a0-137">MeetingRequest</span></span>](meetingrequest.md) <br/> |<span data-ttu-id="546a0-138">Stellt eine Besprechungsanforderung im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-138">Represents a meeting request in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-139">MeetingResponse</span><span class="sxs-lookup"><span data-stu-id="546a0-139">MeetingResponse</span></span>](meetingresponse.md) <br/> |<span data-ttu-id="546a0-140">Stellt eine Besprechungsantwort im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-140">Represents a meeting response in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-141">Message</span><span class="sxs-lookup"><span data-stu-id="546a0-141">Message</span></span>](message-ex15websvcsotherref.md) <br/> |<span data-ttu-id="546a0-142">Stellt eine Exchange-E-Mail-Nachricht dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-142">Represents an Exchange e-mail message.</span></span>  <br/> |
|[<span data-ttu-id="546a0-143">PostItem</span><span class="sxs-lookup"><span data-stu-id="546a0-143">PostItem</span></span>](postitem.md) <br/> |<span data-ttu-id="546a0-144">Stellt ein Post-Element im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-144">Represents a post item in the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-145">RemoveItem</span><span class="sxs-lookup"><span data-stu-id="546a0-145">RemoveItem</span></span>](removeitem.md) <br/> |<span data-ttu-id="546a0-146">Entfernt ein Element aus dem Exchange-Informationsspeicher.</span><span class="sxs-lookup"><span data-stu-id="546a0-146">Removes an item from the Exchange store.</span></span>  <br/> |
|[<span data-ttu-id="546a0-147">Aufgabe</span><span class="sxs-lookup"><span data-stu-id="546a0-147">Task</span></span>](task.md) <br/> |<span data-ttu-id="546a0-148">Stellt eine Aufgabe im Exchange-Informationsspeicher dar.</span><span class="sxs-lookup"><span data-stu-id="546a0-148">Represents a task in the Exchange store.</span></span>  <br/> |
   
## <a name="text-value"></a><span data-ttu-id="546a0-149">Textwert</span><span class="sxs-lookup"><span data-stu-id="546a0-149">Text value</span></span>

<span data-ttu-id="546a0-150">Keine.</span><span class="sxs-lookup"><span data-stu-id="546a0-150">None.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="546a0-151">Bemerkungen</span><span class="sxs-lookup"><span data-stu-id="546a0-151">Remarks</span></span>

<span data-ttu-id="546a0-152">Das Schema, das dieses Element beschreibt, befindet sich im virtuellen IIS-Verzeichnis, das Exchange-Webdienste hostet.</span><span class="sxs-lookup"><span data-stu-id="546a0-152">The schema that describes this element is located in the IIS virtual directory that hosts Exchange Web Services.</span></span>
  
## <a name="element-information"></a><span data-ttu-id="546a0-153">Informationen zu Elementen</span><span class="sxs-lookup"><span data-stu-id="546a0-153">Element information</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="546a0-154">Namespace</span><span class="sxs-lookup"><span data-stu-id="546a0-154">Namespace</span></span>  <br/> |https://schemas.microsoft.com/exchange/services/2006/types  <br/> |
|<span data-ttu-id="546a0-155">Name des Schemas</span><span class="sxs-lookup"><span data-stu-id="546a0-155">Schema Name</span></span>  <br/> |<span data-ttu-id="546a0-156">Schematypen</span><span class="sxs-lookup"><span data-stu-id="546a0-156">Types schema</span></span>  <br/> |
|<span data-ttu-id="546a0-157">Überprüfungsdatei</span><span class="sxs-lookup"><span data-stu-id="546a0-157">Validation File</span></span>  <br/> |<span data-ttu-id="546a0-158">Types.xsd</span><span class="sxs-lookup"><span data-stu-id="546a0-158">Types.xsd</span></span>  <br/> |
|<span data-ttu-id="546a0-159">Leer kann sein</span><span class="sxs-lookup"><span data-stu-id="546a0-159">Can be Empty</span></span>  <br/> |<span data-ttu-id="546a0-160">False</span><span class="sxs-lookup"><span data-stu-id="546a0-160">False</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="546a0-161">Siehe auch</span><span class="sxs-lookup"><span data-stu-id="546a0-161">See also</span></span>



- [<span data-ttu-id="546a0-162">EWS-XML-Elemente in Exchange</span><span class="sxs-lookup"><span data-stu-id="546a0-162">EWS XML elements in Exchange</span></span>](ews-xml-elements-in-exchange.md)

